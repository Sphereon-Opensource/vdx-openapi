<h1 align="center">
  <br>
  <a href="https://www.sphereon.com"><img src="https://sphereon.com/content/themes/sphereon/assets/img/logo.svg" alt="Sphereon" width="400"></a>
    <br>VDX : Verifiable Data Exchange 
    <br>IMO : Identity Management Openapi
  <br>
</h1>


## User Spec Open API

This is version 1.0.0 of Sphereon's Verifiable Data Platform (vdp for short). This Spec contains CRUD operations for the following entities:
- Realms
- Users
- Groups
- Roles

## Releasing new version
#### Step A : Recreate the SDK

```
mvn clean install
```

#### only after making sure all the changes are there you can publish into our nexus

#### Step B : Release the SDK

If you have the correct settings in your local workspace, you can easily publish a new version on Sphereon repository (`sphereon-opensource-snapshots`)
if you do, you can create and upload a new version with running:

```
mvn clean deploy
```
This will publish the jar result of this project in our nexus server.

## Operations:

### Realms:
POST

`/` Save the realm.

GET

`/{realmId}` Get the realm. It will not include nested information like User.


PUT

`/{realmId}` Update the information of the realm. Any groups, users or roles information in the representation will be ignored.

DELETE

`/{realmId}` Delete the realm

### Groups
##### GET

`/{realmId}/groups` Get groups for a specific realm.

##### POST

`/{realmId}/groups` Create a group for a specific realm.

##### GET

`/{realmId}/groups/{groupId}` Get a specific group for a specific realm.

##### PUT
`/{realmId}/groups/{groupId}` Update the information of the group. Any user information in the representation will be ignored.

##### DELETE
`/{realmId}/groups/{groupId}` Delete a specific group.

### Users:
##### GET
`/{realmId}/users` Get users for a specific realm.

##### POST
`/{realmId}/users` Create a user for a specific realm.

##### GET
`/{realmId}/users/{userId}` Get a specific user for a specific realm.

##### PUT
`/{realmId}/users/{userId}` Update the information of the user.

##### DELETE
`/{realmId}/users/{userId}` Delete a specific user.

## Roles:
##### GET
`/{realmId}/roles` Get roles for a specific realm.

##### POST
`/{realmId}/roles` Create a role for a specific realm.

##### GET
`/{realmId}/roles/{roleId}` Get a specific role for a specific realm.

##### PUT
`/{realmId}/roles/{roleId}` Update the information of the role.

##### DELETE
`/{realmId}/roles/{roleId}` Delete a specific role.

## Parameters:

| Name     | Place | Type   | Available values     | Example                                                   |
|----------|-------|--------|----------------------|-----------------------------------------------------------|
| expand   | query | enum   | groups, roles, users | users                                                     |
| realmId  | path  | string |                      | 280fe02a-4t9q                                             |
| userId   | path  | string |                      | we1fe02a-b89d                                             |
| groupId  | path  | string |                      | 562fe02a-l79l                                             |
| pageable | query | object |                      | `page=3&size=50&sort=createdAt,DESC` |

## Further info
For further information you can view the actual openapi yaml file.
