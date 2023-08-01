<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
    <br>VDX : Verifiable Data Exchange 
    <br>EDIdO : External Decentralized Identity Openapi
  <br>
</h1>

## Usage

This is a maven based project. To set it up locally for development, run following commands.

```shell
cd '<workspace>'
git clone git@github.com:Sphereon-Opensource/vdx-openapi.git
cd vdx-openapi
```
From here you can generate the models for all the models for this module and every other module. But if you want to create the models just for this module, you can first switch your directory and then follow next steps:
```shell
cd edido
```

### Generate API/Models

The following command will generate the models in `<workspace>/vdx-openapi/edido/target/sdks/java/models`.
```shell
mvn clean install -P java-api
```

After the build succeeds. Spring boot application can be run just like a java console application.

```
src/main/java/com/sphereon/vdx/edido/service/Application.java
```

Logs may show something similar to following:
```
Started Application in 2.685 seconds (JVM running for 3.769)
```

The REST API can be accessed using the following URL e.g. from the PostMan Desktop Application:
```
http://localhost:8080/api.dev/v1/universal-resolver/identifiers/12444545
```
