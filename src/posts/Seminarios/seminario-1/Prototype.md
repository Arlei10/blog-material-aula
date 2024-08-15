---
icon: edit
date: 2024-07-25 20:10:00.00 -3
tag:
  - Prototype
  - gof
category:
  - seminario-1
order: 10
excerpt: Apresentação do Padrão de Projeto Prototype
author: GabrielMreira, Redror
---

# Prototype

## Gabriel Moreira Bispo Santos (20221TADSSAJ0020)
[@GabrielMreira](https://github.com/GabrielMreira)

<!-- @include: ../../../includes/seminario-1-GabrielMreira/README.md -->


## Pedro Carlos de Gois Barros Santos (20221TADSSAJ0006)
[@Redror](https://github.com/Redror)

<!-- @include: ../../../includes/seminario-1-Redror/README.md -->


## Árlei Nóbrega 

```plantuml

@startuml
class Usuario {
  - id: Integer
  - nome: String
  - email: String
  - senha: String
}

class Cliente extends Usuario {
  - endereco: Endereco
  - telefone: String
}

class Administrador extends Usuario {
  - nivelAcesso: Integer
}

class Produto {
  - id: Integer
  - nome: String
  - descricao: String
  - preco: Double
  - categoria: Categoria
}

class Categoria {
  - id: Integer
  - nome: String
}

class Pedido {
  - id: Integer
  - data: Date
  - status: String
  - cliente: Cliente
}

class Pagamento {
  - id: Integer
  - valor: Double
  - data: Date
  - formaPagamento: String
  - pedido: Pedido
}

Pedido "1" -- "*" Produto : contém
Pedido "1" -- "*" Pagamento : possui
@enduml

```
