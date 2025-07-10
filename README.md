# dhis2-api-contracts

POC to see how a shared repo might look.  
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