<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
    <br>VDX : Verifiable Data Exchange 
    <br>EVCS : External Verifiable Credential Service Openapi
  <br>
</h1>


## Usage

This is a maven based project. To set it up locally for development, run following commands.

```
cd '<workspace>'
git clone git@github.com:Sphereon/vdx-external-vc-openapi.git
cd vdx-external-vc-openapi
```

### Generate API/Models (Future-work)

Uncomment contents of files to see project running.

```
src/main/java/com/sphereon/vdx/evco/api/*.java
```

The following command will generate the api/models in `<workspace>/vdx-external-vc-openapi/target/generated-sources/java/api/src/main/java/com/sphereon/vdx/evco`.
```
mvn clean install -P rest-api
```

Once the new openapi plugin is released (expected in few days/weeks), follow next steps.

Update the maven pom plugin. After the build succeeds. Spring boot application can be run just like a java console application.

```
com.sphereon.vdx.evco.VDXSwagger2SpringBoot
```

Logs may show something similar to following:
```
Started Application in 2.685 seconds (JVM running for 3.769)
```

The REST API can be accessed using the following URL e.g. from the PostMan Desktop Application:
```
http://localhost:8080/credentials/status
```

### Deploy

```commandline
mvn -P rest-api deploy
```

### Deploy

```commandline
mvn clean deploy -DaltDeploymentRepository=releases::default::http://nexus.qa.sphereon.com/nexus/content/repositories/sphereon-opensource-snapshot/
```