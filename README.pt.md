# Visão Geral

Este projeto é uma prova de conceito com o objetivo de implementar a arquitetura microfrontend utilizando o framework Flutter.

A arquitetura microfrontend permite a criação de aplicativos móveis flexíveis, dividindo a aplicação em pequenos módulos independentes.

Cada módulo, ou "microapp", é desenvolvido de maneira isolada, o que resulta em um alto grau de desacoplamento e manutenção eficiente.

**Principais benefícios:**

- Modularidade: as funcionalidades são desenvolvidas de forma independentes
- Escalabilidade: atualização e adição de módulos sem impactar o aplicativo como um todo.
- Flexibilidade: utilize tecnologias diversas para diferentes partes da interface.
- Performance: carregamento sob demanda para uma experiência de usuário ágil.
- Gestão de Bugs e side-effects: com microapps independentes e desacoplados, dificilmente a correção de um bug ou
alteração de alguma funcionalidade gerará side-effects.

**Pontos a serem considerados:**

- Complexidade inicial: configurar uma arquitetura Microfrontend pode ser complexo e desafiador.
- Gerenciamento de estado: gerenciar estados compartilhado entre microfrontends se torna mais complexo.
- Potencial para desempenho: se não for bem gerenciado, o carregamento sob demanda pode impactar o desempenho.
- Padrões de comunicação: é necessário estabelecer padrões de comunicação entre microfrontends.

**Quando é adequado?**

A arquitetura Microfrontend é adequada em cenários onde:

- A aplicação é grande e complexa, o que dificulta a evolução e manutenção.
- Equipes diferentes precisam trabalhar em partes diferentes da aplicação.
- É necessário escalar ou adicionar novas funcionalidades de forma ágil, reduzindo os conflitos dentro do projeto.
- A modularidade, desacopalamento e a reutilização de componentes são importantes.
- A experiência do usuário e o desempenho são prioridades.

obs: A adoção deve ser considerada com base nas necessidades específicas do projeto, para projetos menores ou simples, a complexidade inicial não justificaria a utilização desta arquitetura.

**Componentes**

Nesta arquitetura, temos 4 componentes principais: Base App, Core, Microapps e Microcommons.

<img width="680" alt="Screenshot 2023-09-03 at 16 33 56" src="https://github.com/vaanessamota/micro_frontend/assets/20022113/35762df8-5c48-4911-9d1b-79d55d7e48da">


**Base App**
- Responsável por inicializar a aplicação como um todo e todos os microfrontends.
- Desconhece os detalhes de implementação do core e dos microapps.

**Micro Core**
- Micro core possui os contratos de inicialização do base app e dos microapps.
- Possui os mecanismos necessários para o registro de rotas e navegação.

**Micro App**
- Um módulo do app, possui poucas responsabilidades e é onde fica a implementação das funcionalidades do app.
- Desconhece outros microapps, e caso necessário, acessa funcionalidades compartilhadas através do micro-commons.

**Micro Commons**
- É o único módulo compartilhável, formenta outros microapps com funcionalidades reutilizáveis, como o DS da aplicação.


Referências:

[Toshi Ossada - Flutterando](https://blog.flutterando.com.br/micro-frontends-criando-aplicativos-mais-profissionais-com-o-modular-43eba2264dbe)

[Deivid Willyam](https://github.com/DeividWillyan/Curso-Flutter-Advanced/tree/master)