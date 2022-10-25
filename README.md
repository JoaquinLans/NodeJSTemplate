# NodeJSTemplate

project template for structuring folders and files in a nodeJS api

## Core Folder structure

- .circle
- scripts
- src
  - api
  - config
  - services
  - models
  - infrastructure
  - tests
  - utils

## src (source)

It shall contain the **entire code base of the application**. Separate from any scripts for external or internal use. At this level we will store the startup files of the application itself (index.ts, index.consumer.ts, index.api.ts...).

### src/api

Any code related to the **entry or exit point of the application** shall be stored in this folder. Understanding as input or output technologies such as HTTP REST, Graphql, GRPC, Kafka...etc.

### src/config

This folder will store any code **related to the configuration needed to start the application**. For example the use and storage of environment variables.

### src/services

This folder will contain the code **related to the internal business logic** to which the API in question will be dedicated. For example, installStatusService.ts with methods such as GetInstallStatus() or UpdateInstallStatus().

### src/models

This folder will contain the **pure typescript objects that we will handle throughout the application or interfaces**. For example, InstallStatusObject.ts

### src/infrastructure

In this folder shall be stored the code related to any type of **client or connector with a persistence system** used by the application itself. For example, mongoDB clients, redis, postgreSQL... etc.

### src/utils

This folder will contain the **code that is used more generally throughout the application**, such as type converters, text parsers, encryption...etc.

### src/tests

Folder containing the **test code of the application**, containing both unit and integration tests.
