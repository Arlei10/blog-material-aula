---
icon: edit
date: 2024-07-25 20:10:00.00 -3
tag:
  - 'Object Pool'
  - gof
category:
  - seminario-1
order: 10
excerpt: Apresentação do Padrão de Projeto Object Pool
author: JoaoAugustoMPdJ, SalvadorCerqueiraJr
---

# Object Pool

## João Augusto Moura Peixoto de Jesus (20211TADSSAJ0004)
[@JoaoAugustoMPdJ](https://github.com/JoaoAugustoMPdJ)

<!-- @include: ../../../includes/seminario-1-JoaoAugustoMPdJ/README.md -->


## Salvador Cerqueira Júnior (20212TADSSAJ0020)
[@SalvadorCerqueiraJr](https://github.com/SalvadorCerqueiraJr)

<!-- @include: ../../../includes/seminario-1-SalvadorCerqueiraJr/README.md -->

## Árlei Nóbrega
```plantum1
@startuml
title Diagrama de Classes: Pool de Salas de Aula

class PoolDeSalas {
    - salasDisponiveis: List<Sala>
    - numeroMaximoDeSalas: int
    + obterSala(): Sala
    + liberarSala(Sala)
    - criarSalasIniciais()
}

class Sala {
    - numero: int
    - capacidade: int
    - equipamentos: List<String>
    + estaDisponivel(): boolean
}

class SistemaDeGerenciamento {
    - poolDeSalas: PoolDeSalas
    + alocarSala(Disciplina disciplina): Sala
}

PoolDeSalas o-- Sala
SistemaDeGerenciamento o-- PoolDeSalas

@enduml
```
