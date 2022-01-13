# Web Engineering 2021-2022 / microservices

**In this assignment your PR must only modify the `README.md` file**. Please, go to
the [Wiki](https://github.com/UNIZAR-30246-WebEngineering/lab6-services/wiki) in order to get the instructions for this
assignment.

## Primary goal

The code is based on the post [microservices with Spring](https://spring.io/blog/2015/07/14/microservices-with-spring)
developed by [Paul Chapman](https://github.com/paulc4). The laboratory shows a simple example of setting up
a [microservices](http://martinfowler.com/articles/microservices.html) system using Spring Boot and Eureka. This project
contains three apps:

* **Service discovery** (`registration` written in Kotlin):
  It launches an open source discovery server called [Eureka](https://github.com/Netflix/eureka) that will use the port
  1111. The dashboard of the registration server is exposed in `http://localhost:1111`.
* **Account service** (`accounts` written in Kotlin):
  It is a standalone process that provides a RESTful server to a repository of accounts that will use the port 2222.
  What it makes special is that it registers itself to Eureka with the name `ACCOUNTS-SERVICE`. After launching this
  service you can see in the dashboard of Eureka that after a few seconds (10-20 secs) the `ACCOUNTS-SERVICE` service
  appears.
* **Web service** (`web` written in Java):
  It is a standalone process that provides an MVC front-end to the application of accounts that will use the port 3333.
  What it makes special is that it registers itself to the Eureka with the name `WEB-SERVICE` and asks the Eureka where
  is the `ACCOUNTS-SERVICE`. Spring configures automatically an instance of `RestTemplate` for using the discovery
  service transparently!!!

This is a *NOT* a speed competition. The objective is to show that the following activities have been accomplished:

* The two services `accounts (2222)` and `web` are running and registered (two terminals, logs screenshots).
* The service registration service has these two services registered (a third terminal, dashboard screenshots)
* A second `accounts` service instance is started and will use the port 4444. This second `accounts (4444)` is also
  registered (a fourth terminal, log screenshots).
* What happens when you kill the service `accounts (2222)` and do requests to `web`?  
  Can the web service provide information about the accounts again? Why?

The above must be documented in a brief report (`report.md`) with screenshots describing what happens.

## Secondary goal (:gift:)

Proposed:

* [Circuit breaker for the requests from web to accounts that avoids a 500 error](https://spring.io/guides/gs/circuit-breaker/)
  .
* [API gateway for web and registration](https://spring.io/guides/gs/routing-and-filtering/).
* [Centralized configuration for all services](https://spring.io/guides/gs/routing-and-filtering/).
* [Dockerize the three services](https://spring.io/guides/topicals/spring-boot-docker).
* [Docker compose with scale by command line](https://thepracticaldeveloper.com/dockerize-spring-boot/).

Manifest your intention first by a PR updating this `README.md` with your goal. If you desist of your goal, release it
by a PR so other fellow can try it.

| NIA | User name | Report | Improvement | Score |
|-----|-----------|------|-------------|-------|
| 757166 | Pablo Jordan | [Primary Goal](https://github.com/pabloJordan24/lab6-microservices/blob/test/PrimaryGoal/PrimaryGoal.md) |             |       |
| 755232 | Diego Marco | [report](https://github.com/dmarcob/lab6-microservices/blob/test/report.md) |
| 778097 | Héctor Bara |  [Solution](https://github.com/dolansete/lab6-microservices/blob/test/report.md)    |             |       |
| 778148 | José Marín | [report](https://github.com/jmarindiez/lab6-microservices/blob/test/docs/report.md) |             |       |
| 774840 | [Fernando Serrano](https://github.com/Feer93/lab6-microservices) | [report](https://github.com/Feer93/lab6-microservices/blob/test/documentation.md) |             |       |
| 755848 | Guillermo Cánovas González | [Report](https://github.com/guillecanovas/lab6-microservices/blob/test/report.md)
| 785649 | [Andoni Salcedo](https://github.com/AndoniSalcedo/lab6-microservices) | [report.md](https://github.com/AndoniSalcedo/lab6-microservices/blob/test/report.md) | | |
| 767870 | Diego García Muro | [report](https://github.com/thdgm/lab6-microservices/blob/test/ReportMD/ReportMD.md)  |             |       |
| 780448 | María Peña | [Report](https://github.com/Keyleth8/lab6-microservices/blob/test/Solution.md) |             |       |
| 779354 | Alejandro Magallón Soler|[Report](https://github.com/alecron/lab6-microservices/blob/test/Report.md)      |             |       |
| 780378 | Óscar Pueyo | [report](https://github.com/iksopo/lab6-microservices/blob/test/doc/report.md) |             |       |
| 774335 | Ángela Rojo | [Report](https://github.com/angela-rs/lab6-microservices/blob/work/report.md) |             |       |
| 780454 | Marta Morales Sabroso|[Solution](https://github.com/780454-unizar/lab6-microservices/blob/test/solution.md)      |             |       |
| 734941 | Felipe Nonay|[LAB6_Solution](https://github.com/fnonay/lab6-microservices/blob/test/SOLUTION.md)|
| 720162 | Salomé Rea| [report](https://github.com/SalomeReav/lab6-microservices/blob/test/report.md)  |             |       |
| 780180 | [Carlos Navarro](https://github.com/Lulay7/lab6-microservices) | [report](https://github.com/Lulay7/lab6-microservices/blob/c295e1f8973ff123815377bd1588a0e2f23034c0/report/report.md) |             |       |
| 775929 | [Alejandro Artal](https://github.com/Alejandro-Artal/lab6-microservices/tree/test)| [Report](https://github.com/Alejandro-Artal/lab6-microservices/blob/test/report.md) |      |             |
| 776012 | Jaime Conchello | [report](https://github.com/jaimecb/lab6-microservices/blob/test/report.md) |             |       |
| 755787 | Sergio Benítez Mombiela | [report](https://github.com/SergioBenitez755787/lab6-microservices/blob/test/Solution/report.md) |             |       |
| 771069 | [Alejandro Terron](https://github.com/Alex28499/lab6-microservices/tree/work) |[Report](https://github.com/Alex28499/lab6-microservices/blob/work/report.md)|             |       |
| 776453 | Jorge Serrano Ibañez | [Report](https://github.com/zgzserrano/lab6-microservices/blob/test/report.md)
| 757024 | Germán Garcés| [report.md](https://github.com/fntkg/lab6-microservices/blob/work/report.md)     | |       |
| 721520 | Sergio García-Campero Hernández | [solution.md](https://github.com/SergioGCH/lab6-microservices/blob/test/solution.md)     | |       |
| 779691 | [Tomás Pelayo](https://github.com/Tomenos18/lab6-microservices)|[Report](https://github.com/Tomenos18/lab6-microservices/blob/test/report.md)| | |
| 780029 | [Mateo Vallejo](https://github.com/CursedR3N/lab6-microservices/tree/test) | [report](https://github.com/CursedR3N/lab6-microservices/blob/test/report/report.md) | | |
| 722292 | [Adrián García](https://github.com/adrigaarcia/lab6-microservices)|[Primary Goal](https://github.com/adrigaarcia/lab6-microservices/blob/test/primary_goal.md)| | |
| 764914 | [Víctor Pérez](https://github.com/vitolo99/lab6-microservices)|[Primary Goal](https://github.com/vitolo99/lab6-microservices/blob/test/PRIMARY_GOAL.md)| |
