# SOLID

## Introdução ao SOLID

  - Boas práticas no mundo de desenvolvimento OO

  - Agile Software Development, Principles, Patterns, and Practices, Robert C. Martin

## Single Responsibility Principle (SRP)

  - Princípio da responsabilidade única
  
  - 1 classe => 1 responsabilidade
  
  - A classe deve ter somente um motivo para mudar/fazer alteração

## Open Closed Principle (OCP)

  - Princípio do aberto fechado
  
  - Toda classe deve ser ABERTA para EXTENSÃO, mas FECHADA para MODIFICAÇÃO
  
  - [BAD] Necessidade de criar diversas condições na classe para suportar novos comportamentos
    - Muitos ifs
  
  - [GOOD] Usar classe base, estender a classe
    - classe abstract, métodos abstract
	- classes que estendem e implementam métodos abstratos

## Liskov Substitution Principle (LSP)

  - Princípio de substituição de Liskov
  
  - Subclasses podem ser substituídas por sua classe pai
  
  - Ou seja, deve ser possível utilizar a classe pai no lugar da classe filha
  
  - [LSP: Princípio da Substituição de Liskov](https://www.ramonsilva.net/post/lsp-princ%C3%ADpio-da-substitui%C3%A7%C3%A3o-de-liskov)
  
  
## Interface Segregation Principle (ISP)

  - Princípio da segregação das interfaces
  
  - A classe não deve ser obrigada a implementar interfaces que não utilizará
  
    - [GOOD] Segregar em interfaces que façam sentido, então a classe que implementa, só irá implementar as interfaces que façam sentido a ela (que tenham métodos que de fato precisa)
  
  
## Dependency Inversion Principle (DIP)

  - Princípio da inversão de dependência
  
  - A classe deve depender de abstrações e não de implementações (classe concreta)
  
  - Inverter as dependências -> não ocorre new (não instancia) dentro da classe. Passar o objeto via construtor ou via setter
  
    - [BAD] Dependência de implementação -> depender de uma classe concreta -> gera alto acoplamento
	- [GOOD] Trabalhar com interface ou classe abstrata. Pode ser utilizado container de injeção de dependência (fica responsável de criar os objetos, passando as dependências, evitando alto acoplamento com new)