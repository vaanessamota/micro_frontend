# Microfrontend Architecture with Flutter

This project is a proof of concept for implementing the micro frontend architecture using the Flutter framework.

## Overview

The micro frontend architecture allows for the creation of flexible mobile applications by dividing the application into small independent modules.

Each module, or "microapp," is developed in isolation, resulting in a high degree of decoupling and efficient maintenance.

### Key Benefits

- **Modularity:** Functionalities are developed independently.
- **Scalability:** Updates and addition of modules without impacting the overall application.
- **Flexibility:** Use various technologies for different parts of the application.
- **Performance:** On-demand dependencies loading for an agile user experience.
- **Bug and Side-effect Management:** With independent and decoupled micro apps, fixing a bug or making changes to a feature is less likely to generate side-effects.

### Points to Consider

- **Initial Complexity:** Setting up a Microfrontend architecture can be complex and challenging.
- **State Management:** Managing shared states between micro frontends becomes more complex.
- **Potential for Performance Issues:** If not managed well, on-demand dependencies loading can impact performance.
- **Communication Patterns:** It is necessary to establish communication patterns between microfrontends.

## When is it Suitable?

The Microfrontend architecture is suitable in scenarios where:

- The application is large and complex, which makes the project evolution and maintenance difficult.
- Different teams need to work on different parts of the application.
- Agile scaling or continuous addition of new features is required
- Modularity, decoupling, and component reuse are important.
- User experience and performance are priorities.

**Note:** Adoption should be considered based on the specific project needs. For smaller or simpler projects, the initial complexity may not justify the use of this architecture.

## Components

In this architecture, we have four main components:

<img width="680" alt="Screenshot 2023-09-03 at 16 33 56" src="https://github.com/vaanessamota/micro_frontend/assets/20022113/35762df8-5c48-4911-9d1b-79d55d7e48da">


- **Base App:** Responsible for initializing the entire application and all micro frontends. Unaware of the implementation details of the core module and microapps.

- **Micro Core:** Micro Core has the initialization contracts of the base app and micro apps. It has the necessary mechanisms for route registration and navigation.

- **Micro App:** A module of the app, responsible for a few functionalities and where the implementation of the app's features resides. Unaware of other microapps, and if necessary, accesses shared functionalities through micro-commons.

- **Micro Commons:** The shareable module, provides other microapps with reusable functionalities, such as the application's design system.

## References

- [Toshi Ossada - Flutterando](https://blog.flutterando.com.br/micro-frontends-criando-aplicativos-mais-profissionais-com-o-modular-43eba2264dbe)
- [Deivid Willyam](https://github.com/DeividWillyan/Curso-Flutter-Advanced/tree/master)
