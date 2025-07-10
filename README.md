# dhis2-api-contracts

POC to see how a shared repo, storing API contracts, might look.  
The project has 3 main directories: 
- contracts
  - this is where the shared contracts live
- backend
  - any backend specific code to be able to retrieve the assets as a dependency
  - contains a minimal `pom.xml` that includes the root contracts in the packaging of resources
- frontend
  - any frontend specific code to be able to retrieve the assets as a dependency (if needed)

The project is published as a GitHub release. Backend projects can add the contracts as a dependency using JitPack. e.g. 
```xml
<dependency>
  <groupId>com.github.david-mackessy</groupId>
  <artifactId>dhis2-api-contracts</artifactId>
  <version>3.0.0</version>
</dependency>
```

The POC includes sample contracts and JSON schemas for `Category` & `CategoryOption` to start.

## Goals
Some brief info about the main goals of this setup: 
- Enable running tests without requiring network calls
  - Ideally we'd like to run tests without having to make network calls to get the contracts
  - With the GitHub release approach, we can release an artefact and allow dependency management tools to package them in projects
- Defining our own contracts & how they would work best for us
  - We have the flexibility to define what we want
  - Aim to keep them simple while still providing value 