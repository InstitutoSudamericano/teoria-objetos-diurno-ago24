Este CRUD será creado con un resource de una API REST con el nombre de "creatures".
### Pasos para crear tu primer CRUD de criaturas mitológicas

1. Para crear tu primer CRUD vamos a dar acceso a PrismaClient de la siguiente manera:

```typescript
import { Module } from '@nestjs/common';
import { CreaturesService } from './creatures.service';
import { CreaturesController } from './creatures.controller';
import { PrismaModule } from 'src/prisma/prisma.module';
import { PrismaService } from 'src/prisma/prisma.service';

@Module({
  controllers: [CreaturesController],
  providers: [CreaturesService, PrismaService],
  imports: [PrismaModule],
})
export class CreaturesModule {}
```

2. Crear los métodos CRUD dentro de `creatures.services.ts`:

```typescript
import { Injectable } from '@nestjs/common';
import { CreateCreatureDto } from './dto/create-creature.dto';
import { UpdateCreatureDto } from './dto/update-creature.dto';
import { PrismaService } from 'src/prisma/prisma.service';

@Injectable()
export class CreaturesService {
  constructor(private prisma: PrismaService) {}
  create(createCreatureDto: CreateCreatureDto) {
    return this.prisma.creature.create({
      data: createCreatureDto,
    });
  }

  findAllAlive() {
    return this.prisma.creature.findMany({
      where: {
        extinct: false,
      },
    });
  }

  findExtinct() {
    return this.prisma.creature.findMany({
      where: {
        extinct: true,
      },
    });
  }

  findOne(id: number) {
    return this.prisma.creature.findUnique({
      where: {
        id,
      },
    });
  }

  update(id: number, updateCreatureDto: UpdateCreatureDto){
    return this.prisma.creature.update({
      where: { id },
      data: updateCreatureDto,
    });
  }

  remove(id: number) {
    return this.prisma.creature.delete({
      where: { id },
    });
  }
}
```

3. Realiza las solicitudes HTTP en el controlador `creatures.controller.ts`:

```typescript
import {
  Controller,
  Get,
  Post,
  Body,
  Patch,
  Param,
  Delete,
} from '@nestjs/common';
import { CreaturesService } from './creatures.service';
import { CreateCreatureDto } from './dto/create-creature.dto';
import { UpdateCreatureDto } from './dto/update-creature.dto';

@Controller('creatures')
export class CreaturesController {
  constructor(private readonly creaturesService: CreaturesService) {}

  @Post()
  create(@Body() createCreatureDto: CreateCreatureDto) {
    return this.creaturesService.create(createCreatureDto);
  }

  @Get()
  findAllAlive() {
    return this.creaturesService.findAllAlive();
  }

  @Get('extinct')
  findExtinct() {
    return this.creaturesService.findExtinct();
  }

  @Get(':id')
  findOne(@Param('id') id: string) {
    return this.creaturesService.findOne(+id);
  }

  @Patch(':id')
  update(
    @Param('id') id: string,
    @Body() updateCreatureDto: UpdateCreatureDto,
  ) {
    return this.creaturesService.update(+id, updateCreatureDto);
  }

  @Delete(':id')
  remove(@Param('id') id: string) {
    return this.creaturesService.remove(+id);
  }
}
```

4. Maneja el POST dentro del dto create:

```typescript
import { ApiProperty } from "@nestjs/swagger";
export class CreateCreatureDto {
    @ApiProperty()
    name: string;

    @ApiProperty({required: false})
    description?: string;

    @ApiProperty()
    lastSee: string;

    @ApiProperty()
    countLastSee: number;

    @ApiProperty({required: false, default: false})
    extinct?: boolean= false;
}
```

