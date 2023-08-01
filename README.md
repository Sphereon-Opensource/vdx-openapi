<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
    <br>VDX : Verifiable Data Exchange 
    <br>Openapi parent project
  <br>
</h1>

## Usage

This is a maven based project. To set it up locally for development, run following commands.

```
cd '<workspace>'
git clone git@github.com:Sphereon-Opensource/vdx-openapi.git
cd vdx-openapi
```

From here you can generate the models for all the submodules here. Below you can find an account of the modules that you can see in this project.


## Submodules
This project has multiple module for our VDX platform:
- edido: External Decentralized Identifier (did) Openapi
- eimo: External Identity Management Openapi
- evco: External Verifiable Credential (vc) Openapi

### EDIDO
This module contains openapi file for generating models related to our projects handling the DID documents. For more information you can look at specific [README](./edido/README.md) of this module
### EIMO
This module contains openapi file for generating models related to our projects handling the Identity Management part of the platform. For more information you can look at specific [README](./eimo/README.md) of this module
### EVCO
This module contains openapi file for generating models related to our projects handling the Verifiable Credentials. For more information you can look at specific [README](./evco/README.md) of this module

### Generate API/Models

The following command will generate the models in `<workspace>/vdx-openapi/target`.
```
mvn -U clean install
```

## For developers
We put the openapi files inside the swagger directory of each module. These openapi files are self-sufficient and don't have any references to any outside object/entity.
all the dependencies are handled in the parent maven project and special configuration are handled in the submodules.