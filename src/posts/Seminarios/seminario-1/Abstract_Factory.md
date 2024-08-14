---
icon: edit
date: 2024-07-25 20:10:00.00 -3
tag:
  - 'Abstract Factory'
  - gof
category:
  - seminario-1
order: 10
excerpt: Apresentação do Padrão de Projeto Abstract Factory
author: Brenda-Martinez
---
# Abstract Factory


## Brenda Gabriela Martinez Araújo (20221TADSSAJ0001) 

[@Brenda-Martinez](https://github.com/Brenda-Martinez)

<!-- @include: ../../../includes/seminario-1-Brenda-Martinez/README.md -->





## João Augusto

<figure>
  
```plantuml

@startuml
interface Personagem {
    +descricao(): String
}

interface Equipamento {
    +usar(): void
}

interface RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

class Cavaleiro implements Personagem {
    +descricao(): String
}

class Espada implements Equipamento {
    +usar(): void
}

class Mago implements Personagem {
    +descricao(): String
}

class Cajado implements Equipamento {
    +usar(): void
}

class CavaleiroFactory implements RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

class MagoFactory implements RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

RPGFactory <|-- CavaleiroFactory
RPGFactory <|-- MagoFactory
CavaleiroFactory --> Cavaleiro : cria >
CavaleiroFactory --> Espada : cria >
MagoFactory --> Mago : cria >
MagoFactory --> Cajado : cria >
@enduml

```

## Árlei Nóbrega
<figure>
  
```plantuml

@startuml
interface Aluno {
    +matricular(): void
}

interface Professor {
    +ministrarAula(): void
}

interface FaculdadeFactory {
    +criarAluno(): Aluno
    +criarProfessor(): Professor
}

class AlunoGraduacao implements Aluno {
    +matricular(): void
}

class ProfessorMestrado implements Professor {
    +ministrarAula(): void
}

class AlunoGraduacaoFactory implements FaculdadeFactory {
    +criarAluno(): Aluno
    +criarProfessor(): Professor
}

class ProfessorMestradoFactory implements FaculdadeFactory {
    +criarAluno(): Aluno
    +criarProfessor(): Professor
}

FaculdadeFactory <|-- AlunoGraduacaoFactory
FaculdadeFactory <|-- ProfessorMestradoFactory
AlunoGraduacaoFactory --> AlunoGraduacao : cria >
ProfessorMestradoFactory --> ProfessorMestrado : cria >
@enduml

```
</figure>
