<!DOCTYPE html>
<html>
<title>API Document</title>

<xmp theme="united" style="display:none;">
# Ordercloud API


## HTTPS://staging-api.ordercloud.com/resource


Api for Commerce.


[**Contact the developer**](mailto:wessel@ordercloud.com)


**Version** v1

[**Terms of Service**]()










# Security Definitions


### api_key



<table>
<tr>
<th>type</th>
<th colspan="2">apiKey</th>
</tr>


<tr>
<th>name</th>
<th colspan="2">X-Ordercloud-Organisation</th>
</tr>


<tr>
<th>in</th>
<th colspan="2">HEADER</th>
</tr>

</table>




### basicAuth




<table>
<tr>
<th>type</th>
<th colspan="2">basic</th>
</tr>

</table>




# APIs


## /authorization/oauth_token_redirect_url


### GET

<a id="getOauthTokenRedirectUrl">Register an OAuth Token Redirect URL for an Organisation</a>

OAuth terms &#x27;client_id&#x27; or &#x27;api_key&#x27; applies to &#x27;X-Ordercloud-Header&#x27;







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>X-Ordercloud-Organisation</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>URLs</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="registerOauthTokenRedirectUrl">Register an OAuth Token Redirect URL for an Organisation</a>

OAuth terms &#x27;client_id&#x27; or &#x27;api_key&#x27; equals &#x27;X-Ordercloud-Header&#x27;







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>X-Ordercloud-Organisation</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>URLs</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /authorization/organisation/group






### POST


<a id="assignOrganisationGroup">Create or assign groups to the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The list of groups to create or assign</td>
<td> - </td>

<td>
Array[<a href="#/definitions/GroupDto">GroupDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /authorization/organisation/group/{groupId}








### DELETE

<a id="removeOrganisationGroup">Remove a group from the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/group/{groupId}/members






### POST


<a id="addOrganisationGroupMembers">Add members to a group at the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>User ids</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="removeOrganisationGroupMembers">Remove members from a group at the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>User ids</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/group/{groupId}/role






### POST


<a id="assignOrganisationGroupRoles">Assign roles to a group of the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Roles</td>
<td> - </td>

<td>
Array[<a href="#/definitions/RoleDto">RoleDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="revokeOrganisationGroupRoles">Revoke roles from a group of the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Roles</td>
<td> - </td>

<td>
Array[<a href="#/definitions/RoleDto">RoleDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/groups


### GET

<a id="getOrganisationGroups">Get all groups of the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/organisation/members


### GET

<a id="getOrganisationGroupMembers">Get all group members of the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>query</td>
<td>yes</td>
<td>Group id</td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/organisation/{organisationId}/group






### POST


<a id="assignCrossOrganisationGroup">Create or assign groups to any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The list of groups to create or assign</td>
<td> - </td>

<td>
Array[<a href="#/definitions/GroupDto">GroupDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /authorization/organisation/{organisationId}/group/{groupId}








### DELETE

<a id="removeCrossOrganisationGroup">Remove a group from any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/{organisationId}/group/{groupId}/invitation






### POST


<a id="createCrossOrganisationGroupInvitation">Send an invitation email to someone to sign up and automatically join the given group at the given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>The group the user will be added to upon registration (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the invitation to send</td>
<td> - </td>

<td>

<a href="#/definitions/InvitationCreationDto">InvitationCreationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /authorization/organisation/{organisationId}/group/{groupId}/members






### POST


<a id="addCrossOrganisationGroupMembers">Add members to a group at any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>User ids</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="removeCrossOrganisationGroupMembers">Remove members from a group at any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>User ids</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/{organisationId}/group/{groupId}/role






### POST


<a id="assignCrossOrganisationGroupRoles">Assign roles to a group of any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Roles</td>
<td> - </td>

<td>
Array[<a href="#/definitions/RoleDto">RoleDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="revokeCrossOrganisationGroupRoles">Revoke roles from a group of any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>path</td>
<td>yes</td>
<td>Group id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Roles</td>
<td> - </td>

<td>
Array[<a href="#/definitions/RoleDto">RoleDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/organisation/{organisationId}/groups


### GET

<a id="getCrossOrganisationGroups">Get all groups of another organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/organisation/{organisationId}/members


### GET

<a id="getCrossOrganisationGroupMembers">Get all group members of any organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>query</td>
<td>yes</td>
<td>Group id</td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/permissions


### GET

<a id="getPermissions">Get all permissions provided by ordercloud</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPermissions">Give permission to a role</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Permissions</td>
<td> - </td>

<td>
Array[<a href="#/definitions/PermissionDto">PermissionDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="deletePermissions">Delete a permission</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Permissions</td>
<td> - </td>

<td>
Array[<a href="#/definitions/PermissionDto">PermissionDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/role


### GET

<a id="getRoles">Get all roles provided by Ordercloud</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/role/{roleId}/permission


### GET

<a id="getRolePermissions">Get all permissions of a role</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>roleId</th>
<td>path</td>
<td>yes</td>
<td>Role where permissions will be revoked (**Pattern**: `\+d`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="assignRolePermissions">Give permission to a role</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>roleId</th>
<td>path</td>
<td>yes</td>
<td>Role to assign permissions to (**Pattern**: `\+d`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Permissions</td>
<td> - </td>

<td>
Array[<a href="#/definitions/PermissionDto">PermissionDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |





### DELETE

<a id="revokeRolePermissions">Revoke permission from a role</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>roleId</th>
<td>path</td>
<td>yes</td>
<td>Role where permissions will be revoked (**Pattern**: `\+d`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Permissions</td>
<td> - </td>

<td>
Array[<a href="#/definitions/PermissionDto">PermissionDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /authorization/user/organisation/granted/{permission}


### GET

<a id="checkAuthorization">Check if the current user has a permission granted at the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>permission</th>
<td>path</td>
<td>yes</td>
<td>Base64url encoded permission string to search organisations by</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/organisation/groups


### GET

<a id="findUserOrganisationGroups">Get the groups which the current user belongs to, in the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/organisation/permissions


### GET

<a id="findUserOrganisationPermissions">Get all permissions the current user has at the current organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/organisation/roles


### GET

<a id="getUserOrganisationRoles">Get all roles the current user has at the current organisation (Depricated! Code against permissions.)</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/organisation/{organisationId}/roles


### GET

<a id="getUserCrossOrganisationRoles">Get all roles the current user has at any organisation (Depricated! Code against permissions.)</a>









#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/permission/{permission}/organisations


### GET

<a id="findPermissionOrganisations">Get the organisations where the current user has a permission granted</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>permission</th>
<td>path</td>
<td>yes</td>
<td>Base64url encoded permission string to search organisations by</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/{userId}/organisation/{organisationId}/granted/{permission}


### GET

<a id="checkAuthorization">Check if any given user has a permission granted at any given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>User id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>permission</th>
<td>path</td>
<td>yes</td>
<td>Base64url encoded permission string to search organisations by</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/{userId}/organisation/{organisationId}/groups


### GET

<a id="findUserOrganisationGroups">Get the groups any given user belongs to, in any given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>User id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /authorization/user/{userId}/organisation/{organisationId}/permissions


### GET

<a id="findUserOrganisationPermissions">Get all permissions any given user has at any given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>User id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections


### GET

<a id="findAll">returns all the Connection</a>

returns all the Connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ConnectionDto">ConnectionDto</a>]|






### POST


<a id="createConnection">Create a new Connection object</a>

Creates a new Connection entry in the database







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>ID of Connection DTO that needs to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateConnectionDto">CreateConnectionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 404    | type not found |  - |
| 409    | connection allready exists |  - |














## /connections/fee/active/rules


### GET

<a id="findAllActiveRules">returns all the active fee splitting rules currently listed in the system</a>

returns all active the fee splitting rules currently listed in the system







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FeeStructure">FeeStructure</a>]|

















## /connections/fee/metrics


### GET

<a id="findMetrics">Return available metrics for fees</a>

E.g. One fee for all, Volume Based or Price Range Based







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Return connection fee Metrics | <a href="#/definitions/FeeTypeDto">FeeTypeDto</a>|

















## /connections/fee/rules


### GET

<a id="findAllRules">returns all the fee splitting rules currently listed in the system</a>

returns all the fee splitting rules currently listed in the system







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FeeStructure">FeeStructure</a>]|

















## /connections/fee/structures


### GET

<a id="findStructures">Return available structures for fees</a>

E.g. flat fee, percentage fee or combination of the







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Return connection fee Structured | <a href="#/definitions/FeeTypeDto">FeeTypeDto</a>|

















## /connections/fee/types


### GET

<a id="findTypes">Return available types for fees</a>

Will return list of available types of fees







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Return connection Type fees | <a href="#/definitions/FeeTypeDto">FeeTypeDto</a>|

















## /connections/fees


### GET

<a id="listOrganisationConnectionsWithFees">Returns all connections for an organisation with all relevant fees and settings</a>

Returns all connections for an organisation with all relevant fees and settings







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ConnectionShortDetailDto">ConnectionShortDetailDto</a>]|

















## /connections/organisation/{organisationId}/balance


### GET

<a id="findBalancesForConnections">Balance per connection</a>

Returns the balances for a time period of connected organisations







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of organisation to find balances for connections (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>Start date to use for calculating balance of connection</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>End date to use for calculating balance of connection</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>connectiontypes</th>
<td>query</td>
<td>no</td>
<td>Type of connection to filter by</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/organisation/{organisationId}/status


### GET

<a id="getOrganisationConnectionsPerStatus">Get all connections for the organisation by status</a>

Status available : PENDING, CONNECTED, DECLINED







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID the organisation to get Connections for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionStatus</th>
<td>query</td>
<td>yes</td>
<td>connection status to be updated too</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>sort results by : fromOrganisation, toOrganisation, type, prepend + for ASC, - for DSC</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>type</th>
<td>query</td>
<td>no</td>
<td>The connection type, id or code </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/possible


### GET

<a id="listPossibleConnectionsToMake">Returns all possible connections an organisation can make to other organisations</a>

Returns all possible connections an organisation can make to other organisations







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>radius</th>
<td>query</td>
<td>no</td>
<td>radius in meters of which to check for organisations</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionType</th>
<td>query</td>
<td>no</td>
<td>The connection type id</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrganisationDto">OrganisationDto</a>]|

















## /connections/transactions/statement


### GET

<a id="getConnectionTransactionStatement">Download a pdf statement with all transaction for the specified connection</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>fromOrganisation</th>
<td>query</td>
<td>yes</td>
<td>From Organisation Id</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>toOrganisation</th>
<td>query</td>
<td>yes</td>
<td>To Organisation Id</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>From Date</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>To Date</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>format</th>
<td>query</td>
<td>no</td>
<td>Format of the report. Either pdf or csv</td>
<td>pdf</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/transactions/statement/send




### PUT

<a id="emailConnectionTransactionStatement">Send a pdf statement as an attachment to an email address</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>fromOrganisation</th>
<td>query</td>
<td>yes</td>
<td>From Organisation Id</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>toOrganisation</th>
<td>query</td>
<td>yes</td>
<td>To Organisation Id</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>From Date (yyyy-MM-dd)</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>To Date (yyyy-MM-dd)</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>email</th>
<td>query</td>
<td>yes</td>
<td>Receiver email address</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/types


### GET

<a id="findConnectionTypes">returns all the Connection Types</a>

returns all the Connection Types







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ConnectionTypeDto">ConnectionTypeDto</a>]|

















## /connections/{connectionId}/balance


### GET

<a id="findBalanceForConnection">Get connection balance</a>

Return balance of connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>ID of the connection (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>Start date to use for calculating balance of connection</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>End date to use for calculating balance of connection</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/{connectionId}/fee/draft


### GET

<a id="getConnectionFeeDrafts">Get all connection fees that are currently in draft state</a>

All fee structures that have not been accpeted







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>Id of connection to Add fee structure for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/{connectionId}/fee/organisation/{organisationId}




### PUT

<a id="addConnectionFeeDraft">Propose new fee structure for connection</a>

Fee structure will become active when other organisation approves, drafts are unique per FeeType







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>ID of connection to Add fee structure for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of organisation proposing new fee structure (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The proposed fee for a connection</td>
<td> - </td>

<td>

<a href="#/definitions/CreateConnectionOrganisationFeeDto">CreateConnectionOrganisationFeeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{connectionId}/fee/type/{feeType}/accept/organisation/{organisationId}




### PUT

<a id="acceptConnectionFeeDraft">Accept the proposed fee structure for the connection</a>

Proposed fee structure will become active on the connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>Id of connection to Add fee structure for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>feeType</th>
<td>path</td>
<td>yes</td>
<td>Id or code of the fee type being accepted</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of organisation accepting the new fee structure (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{connectionId}/transactions


### GET

<a id="findTransactionsForConnection">Get transactions for a connection</a>

Get transactions for a connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>ID of connection to find transactions for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td>Transaction Types to filter on</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /connections/{id}


### GET

<a id="findOneConnection">Find Connection with specific ID</a>

Find Connection with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be retreived (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|




### PUT

<a id="updateConnection">Update Connection</a>

Update a Connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>ID of Connection DTO containing the data that needs to be updated</td>
<td> - </td>

<td>

<a href="#/definitions/CreateConnectionDto">CreateConnectionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|
| 304    | connection update failed |  - |
| 404    | type not found |  - |






### DELETE

<a id="deleteConnection">Delete Connection with specific ID</a>

Delete Connection with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be deleted (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /connections/{id}/disable




### PUT

<a id="disableConnection">Disable Connection with specific ID</a>

Disable Connection with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be Disabled (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{id}/enable




### PUT

<a id="enableConnection">Enable Connection with specific ID</a>

Enable Connection with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be enable (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{id}/fee/remove/{feeId}








### DELETE

<a id="removeFeeFromConnection">Remove a fee from a Connection in the database</a>

Remove a fee from a Connection in the database







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The fee ID to remove from the Connection</td>
<td> - </td>

<td>


</td>

</tr>

<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection that needs to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 304    | connection update failed |  - |
| 404    | type not found |  - |
| 422    | fee data constraint violation |  - |











## /connections/{id}/organisation/{organisationId}/accept




### PUT

<a id="organisationAcceptConnection">Accept incoming connection.</a>

Update connection status from PENDING to CONNECTED







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The connection to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation accepting the connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{id}/organisation/{organisationId}/decline




### PUT

<a id="organisationDeclineConnection">Accept incoming connection.</a>

Update connection status from PENDING to REJECTED







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The connection to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation rejecting the connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{id}/product/discount


### GET

<a id="viewConnectionProductDiscount">Returns the discounts per product for connection</a>

Returns the discounts per product for connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Connection to add discount (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ProductDiscountDto">ProductDiscountDto</a>]|

















## /connections/{id}/product/{productId}/discount




### PUT

<a id="addConnectionProductDiscount">Add discount in percentage on product for connection</a>

Adds new discount if not set. Updates discount if all ready set







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Connection to add discount (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product to add discount (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>dto</th>
<td>body</td>
<td>yes</td>
<td>Details of the discount</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /connections/{id}/settings


### GET

<a id="findAllSettingsForConnection">returns all settings for a connection</a>

returns all settings for a connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/SettingDto">SettingDto</a>]|




### PUT

<a id="updateSettingForConnection">update the settings for the connection</a>

update the settings for the connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateConnectionSettingDto">CreateConnectionSettingDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/SettingDto">SettingDto</a>]|




### POST


<a id="createSettingsForConnection">create a setting for a connection</a>

creates a setting for the connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection for settings to be added (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateConnectionSettingDto">CreateConnectionSettingDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|














## /connections/{id}/settings/markup




### PUT

<a id="updateMarkupSettingForConnection">update the markup settings for the connection</a>

update the markup settings for the connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/CreateMarkupSettingDto">CreateMarkupSettingDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/SettingDto">SettingDto</a>]|




### POST


<a id="createMarkupSettingsForConnection">create a markup setting for a connection</a>

creates a markup setting for the connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection for markup settings to be added (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateMarkupSettingDto">CreateMarkupSettingDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|














## /connections/{id}/settings/markup/{settingKeyId}


### GET

<a id="findMarkupSettingForConnection">return the value of a specific markup setting key</a>

return the value of a specific markup setting key







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settingKeyId</th>
<td>path</td>
<td>yes</td>
<td>ID of Setting Key for which to find value (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/SettingDto">SettingDto</a>]|

















## /connections/{id}/settings/{settingKeyId}


### GET

<a id="findSettingForConnection">return the value of a specific setting key</a>

return the value of a specific setting key







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Connection (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settingKeyId</th>
<td>path</td>
<td>yes</td>
<td>ID of Setting Key for which to find value (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/SettingDto">SettingDto</a>]|

















## /delivery_agent/balance


### GET

<a id="getAllDeliveryAgentsBalance">Gets a list of balances for all delivery agents for an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/invite/user/{userId}


### GET

<a id="listUserDeliveryAgentInvites">Links a user to an organisation as a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user to get list of invites for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/invite/{inviteId}


### GET

<a id="getDeliveryAgentInvite">Get the invite for the user to be a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>inviteId</th>
<td>path</td>
<td>yes</td>
<td>Id of the delivery agent invite (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |








### DELETE

<a id="deleteDeliveryAgentInvite">Delete an delivery agent invite</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>inviteId</th>
<td>path</td>
<td>yes</td>
<td>Id of the delivery agent invite (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /delivery_agent/organisation/{orgId}


### GET

<a id="findDeliveryAgentsForOrganisation">Returns all delivery agents for an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation to list delivery agents for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>status</th>
<td>query</td>
<td>no</td>
<td>Comma separated list of status id&#x27;s to filter on</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/organisation/{orgId}/delivery_queue


### GET

<a id="getDeliveryAgentQueue">Returns the delivery queue for the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/organisation/{orgId}/float


### GET

<a id="getOrganisationDeliveryAgentFloat">Get the sum of all delivery agents current balance.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/organisation/{orgId}/invite/user/{userId}






### POST


<a id="inviteUserToBeDeliveryAgent">Invites user to be a delivery agent for an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation to link a delivery agents to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>ID of the user to link as a delivery agents to the organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /delivery_agent/organisation/{orgId}/user/{userId}


### GET

<a id="getDeliveryAgentFromOrganisationAndUser">Get Delivery Agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation to of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>ID of the user of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/organisation/{orgId}/user/{userId}/enable




### PUT

<a id="enableDeliveryAgent">Enables a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>ID of the user (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/organisation/{organisationId}/invite/accept




### PUT

<a id="acceptDeliveryAgentInvite">Currently logged in users accepts invitation to be delivery agent for organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation to accept invite for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/balance


### GET

<a id="getDeliveryAgentBalance">Retrieves the balance for a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/directions


### GET

<a id="getDeliveryAgentRouteForCurrentOrder">Get driving directions for a delivery agent, for the currently assigned order</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>latitude</th>
<td>query</td>
<td>yes</td>
<td>Current latitude of the delivery agent</td>
<td> - </td>


<td>number (double)</td>


</tr>

<tr>
<th>longitude</th>
<td>query</td>
<td>yes</td>
<td>Current longitude of the delivery agent</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/history


### GET

<a id="getDeliveryAgentOrderHistory">Get List of orders completed by the delivery agent.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get orders</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get orders</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/order


### GET

<a id="getDeliveryAgentCurrentOrder">Get the current order for the delivery agent.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/orders


### GET

<a id="getDeliveryAgentAllCurrentOrders">Get all current orders for the delivery agent.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/accounts




### PUT

<a id="updateDeliveryAgentAccounts">Update a delivery agents accounts.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>bankAccNo</th>
<td>query</td>
<td>no</td>
<td>The linked bank account. Only last 6 digits will be saved</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>cardNo</th>
<td>query</td>
<td>no</td>
<td>The linked credit card. Only last 4 digits will be saved</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/cashup/{amount}




### PUT

<a id="deliveryAgentCashup">Credit delivery agent with specified amount</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>amount</th>
<td>path</td>
<td>yes</td>
<td>Amount to credit the delivery agent with</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/disable




### PUT

<a id="disableDeliveryAgent">Disables a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/limits




### PUT

<a id="updateDeliveryAgentLimits">Update a delivery agents balance limits on which notifications fire.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>min</th>
<td>query</td>
<td>no</td>
<td>Minimum balance for a delivery agent before notification fires</td>
<td> - </td>


<td>number (double)</td>


</tr>

<tr>
<th>max</th>
<td>query</td>
<td>no</td>
<td>Maximum balance for a delivery agent before notification fires</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/status/{statusId}




### PUT

<a id="updateDeliveryAgentStatus">Update a delivery agents status</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>statusId</th>
<td>path</td>
<td>yes</td>
<td>ID of the status to link to the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/topup/{amount}




### PUT

<a id="deliveryAgentTopup">Debit delivery agent with specified amount</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>amount</th>
<td>path</td>
<td>yes</td>
<td>Amount to debit the delivery agent with</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /delivery_agent/{deliveryAgentId}/organisation/{orgId}/transactions


### GET

<a id="getDeliveryAgentTransactions">Retrieve transactions for a delivery agent, with the given parameters</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the Organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{deliveryAgentId}/report/cashup


### GET

<a id="getDeliveryAgentCashupReport">Links a user to an organisation as a delivery agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>Id of the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /delivery_agent/{id}


### GET

<a id="getDeliveryAgent">Get Delivery Agent</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of the delivery Agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /invitations/organisation/{organisationId}






### POST


<a id="createInvitation">Create an invitation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>groupId</th>
<td>query</td>
<td>yes</td>
<td>The group the user will join upon accepting the invitation</td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the invitation to send</td>
<td> - </td>

<td>

<a href="#/definitions/InvitationCreationDto">InvitationCreationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /invitations/{hash}


### GET

<a id="findByHash">Get an invitation by hash code</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>hash</th>
<td>path</td>
<td>yes</td>
<td>Invitation Hash</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /invitations/{hash}/accept




### PUT

<a id="acceptInvitation">Accept an invitation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>hash</th>
<td>path</td>
<td>yes</td>
<td>Invitation Hash</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /invitations/{hash}/decline




### PUT

<a id="declineInvitation">Decline an invitation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>hash</th>
<td>path</td>
<td>yes</td>
<td>Invitation Hash</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /loyalty/{providerCode}/register/user/{userId}/password/{password}






### POST


<a id="register">Register a loyalty account on the loyalty System</a>

Register a loyalty account on the loyalty System







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>providerCode</th>
<td>path</td>
<td>yes</td>
<td>Code of the loyalty provier</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>password</th>
<td>path</td>
<td>yes</td>
<td>Password used for the user to access loyalty</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /loyalty/{providerCode}/update/user/{userId}/password/{password}




### PUT

<a id="update">Update user details on the loyalty System</a>

Update user details on the loyalty System







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>providerCode</th>
<td>path</td>
<td>yes</td>
<td>Code of the loyalty provider</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>password</th>
<td>path</td>
<td>yes</td>
<td>Password used for the user to access loyalty</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /loyalty/{providerCode}/user/{userId}/balance


### GET

<a id="balance">returns the loyalty account balance</a>

returns the loyalty account balance







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>providerCode</th>
<td>path</td>
<td>yes</td>
<td>Code of the loyalty provier</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /loyalty/{providerCode}/user/{userId}/status


### GET

<a id="status">returns loyalty account status</a>

returns loyalty account status







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>providerCode</th>
<td>path</td>
<td>yes</td>
<td>Code of the loyalty provier</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /loyalty/{providerCode}/user/{userId}/vouchers


### GET

<a id="vouchers">returns list of loyalty vouchers</a>

returns list of loyalty vouchers







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>providerCode</th>
<td>path</td>
<td>yes</td>
<td>Code of the loyalty provier</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /messagegroup


### GET

<a id="findAll">Returns all the Message Groups</a>

Returns all the Message Groups







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/MessageGroupDto">MessageGroupDto</a>]|

















## /messagegroup/active


### GET

<a id="findActive">Find active Message Groups</a>

Find active Message Groups







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | Array[<a href="#/definitions/MessageGroupDto">MessageGroupDto</a>]|
| 404    | No Active Message Groups found |  - |

















## /messagegroup/messagegroup




### PUT

<a id="createMessagegroup">Create a new Message Group</a>

Creates a new Message Group







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Group that needs to be created</td>
<td> - </td>

<td>

<a href="#/definitions/MessageGroupDto">MessageGroupDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Created |  - |
| 400    | Message Group Body malformed |  - |
| 409    | Record Exists |  - |















## /messagegroup/{id}


### GET

<a id="findOneMessageGroup">Find Message Group with specific ID</a>

Find Message Group with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Group that needs to be retrieved (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | <a href="#/definitions/MessageGroupDto">MessageGroupDto</a>|
| 404    | Message Group[id=Long] not found |  - |






### POST


<a id="updateMessageGroup">Update a Message Group in the database</a>

Update a Message Group entry in the database







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Group that needs to be updated (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Group Data</td>
<td> - </td>

<td>

<a href="#/definitions/MessageGroupDto">MessageGroupDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Group was updated |  - |
| 400    | Message Group Body malformed |  - |
| 404    | Message Group[id=Long] not found |  - |





### DELETE

<a id="deleteMessageGroup">Delete Message Group with specific ID</a>

Delete Message Group with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of MessageGroup that needs to be deleted (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 404    | Message Group[id=Long] not found |  - |











## /messagegroup/{name}


### GET

<a id="findMessageGroupByName">Find Message Group with specific Name</a>

Find Message Group with specific @Name







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>name</th>
<td>path</td>
<td>yes</td>
<td>Name of MessageGroup that needs to be retrieved</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | <a href="#/definitions/MessageGroupDto">MessageGroupDto</a>|
| 404    | Message Group[name=String] not found |  - |

















## /messagetemplate


### GET

<a id="findAll">Returns all the Message Templates</a>

Returns all the Message Templates







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Template Data | Array[<a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>]|

















## /messagetemplate/active


### GET

<a id="findActive">Find active MessageTemplate</a>

Find active MessageTemplate







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Template Data | <a href="#/definitions/MessageTemplate">MessageTemplate</a>|
| 404    | Organisation[id=Long] not found |  - |

















## /messagetemplate/messagetemplate




### PUT

<a id="create">Create a new Message Template</a>

Creates a new Message Template







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Template Data</td>
<td> - </td>

<td>

<a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Message Template Created |  - |
| 400    | Message Template Body not valid |  - |
| 409    | Message Template already exists |  - |















## /messagetemplate/organisation/{organisation_id}


### GET

<a id="findAllByOrganisation">Returns all the Message Templates for Organisation</a>

Returns all the Message Templates for Organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisation_id</th>
<td>path</td>
<td>yes</td>
<td>the ID for the organisation</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of recoreds per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Template Data | Array[<a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>]|
| 404    | Organisation[id=Long] not found |  - |

















## /messagetemplate/{id}


### GET

<a id="findOneMessageTemplate">Find Message Template with specific ID</a>

Find Message Template with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Template that needs to be retrieved (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Template Data | <a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>|
| 404    | Message Template[id=Long] not found |  - |






### POST


<a id="updateMessageTemplate">Update a MessageTemplate in the database</a>

Update a MessageTemplate entry in the database







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Template that needs to be updated (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Template Body</td>
<td> - </td>

<td>

<a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Message Template Created |  - |
| 400    | Message Template Body not valid |  - |





### DELETE

<a id="deleteMessageTemplate">Delete MessageTemplate with specific ID</a>

Delete MessageTemplate with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Template that needs to be deleted (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Template Deleted |  - |
| 404    | Organisation[id=Long] not found |  - |











## /messagetype


### GET

<a id="findAll">Returns all the Message Type</a>

returns all the Message Type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Types Data | Array[<a href="#/definitions/MessageTypeDto">MessageTypeDto</a>]|

















## /messagetype/active


### GET

<a id="findActive">Find active Message Type</a>

Find active Message Type







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Type Data | <a href="#/definitions/MessageType">MessageType</a>|
| 404    | No Active Message Type found |  - |

















## /messagetype/messagetype




### PUT

<a id="create">Create a new Message Type</a>

Create a new Message Type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Type Data</td>
<td> - </td>

<td>

<a href="#/definitions/MessageTypeDto">MessageTypeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Message Type Data |  - |
| 400    | Message Type body not Valid |  - |
| 409    | Message Type already exists |  - |















## /messagetype/{id}


### GET

<a id="findOneMessageType">Find Message Type with specific ID</a>

Find Message Type with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of MessageType that needs to be retreived (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Type Data | <a href="#/definitions/MessageType">MessageType</a>|
| 404    | Message Type[id=Long] not found |  - |






### POST


<a id="updateMessageType">Update a Message Type</a>

Update a Message Type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Type that needs to be updated (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message Type data to be updated</td>
<td> - </td>

<td>

<a href="#/definitions/MessageTypeDto">MessageTypeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Type Data |  - |
| 400    | Message Type Body not Valid |  - |
| 404    | Message Type[id=Long] not found |  - |





### DELETE

<a id="deleteMessageType">Delete MessageType with specific ID</a>

Delete MessageType with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Message Type that needs to be deleted (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Type Data |  - |
| 404    | Message Type[id=Long] not found |  - |











## /messagetype/{name}


### GET

<a id="findMessageTypeByName">Find Message Type with specific name</a>

Find Message Type with specific name







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>name</th>
<td>path</td>
<td>yes</td>
<td>Name of Message Type that needs to be retrieved</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Message Type Data | <a href="#/definitions/MessageType">MessageType</a>|
| 404    | Message Type[name=String] not found |  - |

















## /notifications/event_types


### GET

<a id="getNotificationEventTypes">Get list of events available for subscription</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /notifications/organisation/{organisationId}


### GET

<a id="getNotificationSubscriptions">Get list of event subscriptions for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>channel</th>
<td>query</td>
<td>no</td>
<td>Channel to get subscriptions for</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>eventType</th>
<td>query</td>
<td>no</td>
<td>Event type to get subscriptions for</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>recipient</th>
<td>query</td>
<td>no</td>
<td>Custom recipient</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createNotificationSubscription">Create new notification subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of notification subscription</td>
<td> - </td>

<td>

<a href="#/definitions/CreateNotificationSubscriptionDto">CreateNotificationSubscriptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /notifications/{id}


### GET

<a id="getNotificationSubscription">Get list of events available for subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the notification subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateNotificationSubscription">Update notification subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the notification subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of notification subscription</td>
<td> - </td>

<td>

<a href="#/definitions/CreateNotificationSubscriptionDto">CreateNotificationSubscriptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteNotificationSubscription">Delete notification subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the notification subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /notifications/{id}/disable




### PUT

<a id="disableNotificationSubscription">Disable notification subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the notification subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /notifications/{id}/enable




### PUT

<a id="enableNotificationSubscription">Enable notification subscription</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the notification subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders


### GET

<a id="findByOrganisation">returns all the Orders</a>

returns all the Orders







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orders-hash</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>Date from which to begin getting results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>Date up until which to get results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>orderstatus</th>
<td>query</td>
<td>no</td>
<td>List of Order Status id&#x27;s of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>List of payment Statuses of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|






### POST


<a id="CreateOrders">Create an order</a>

Create an order







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Order Details</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderDto">CreateOrderDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|














## /orders/find/{orderRef}


### GET

<a id="findOrderByRef">Returns orders for id</a>

returns order for reference or ID. Reference is matched to the short reference for the order.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderRef</th>
<td>path</td>
<td>yes</td>
<td>Reference/ID of order to find</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/Orders">Orders</a>|

















## /orders/item/extra/{id}


### GET

<a id="findOneOrderItemExtra">Find OrderItemExtra with specific ID</a>

Find OrderItemExtra with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of OrderItemExtra that needs to be fetched (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orders/item/{id}


### GET

<a id="findOneOrderItem">Find OrderItem with specific ID</a>

Find OrderItem with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of OrderItem that needs to be fetched (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrderItem">OrderItem</a>]|

















## /orders/item/{id}/status/self_picked_up




### PUT

<a id="self_picked_upOrders">Mark order with specific ID as Self Picked Up</a>

Mark order with specific @id as Self Picked Up







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/organisation/{id}


### GET

<a id="findByOrganisation">returns organisation orders</a>

returns all the Orders,  that have to be delivered, are owned or which the product belongs too







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orders-hash</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation to fetch orders for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>Date from which to begin getting results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>Date up until which to get results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>orderstatus</th>
<td>query</td>
<td>no</td>
<td>List of Order Status id&#x27;s of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>List of payment Statuses of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|






### POST


<a id="CreateOrderByOrganisation">returns all the Orders</a>

returns all the Orders







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to be used (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Order Details</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderDto">CreateOrderDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|














## /orders/organisation/{organisationId}/delivery/geo/{geoId}




### PUT

<a id="estimateDeliveryCost">Estimate cost of delivery from multiple organisations</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation placing the order (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>geoId</th>
<td>path</td>
<td>yes</td>
<td>Id of the geo location where the order is to be delivered (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Id&#x27;s of organisations from where the order should be collected (Only Id field needs to be populated)</td>
<td> - </td>

<td>
Array[<a href="#/definitions/OrganisationDto">OrganisationDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/paid/{paymentMethod}






### POST


<a id="createPaidOrder">Create a order</a>

Create a order







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>paymentMethod</th>
<td>path</td>
<td>yes</td>
<td>EXTERNAL_CREDITCARD, EXTERNAL_COD OR EXTERNAL_PAYMENT</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Order Details</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderDto">CreateOrderDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|














## /orders/pos/organisation/mapping/{posOrganisationId}


### GET

<a id="findCurrentOrdersForOrganisation">Find current Orders for Organisation in POS format</a>

The header:orders-hash must be passed. This is used to check if any new orders have been placed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orders-hash</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>OrganisationID</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>orderstatus</th>
<td>query</td>
<td>no</td>
<td>List of Order Status id&#x27;s of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>List of payment Statuses of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>The begin date to fetch orders from</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>The end date to fetch orders for</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orders/pos/organisation/{organisationId}


### GET

<a id="findCurrentOrdersForOrganisationByID">Find current Orders for Organisation in POS format</a>

The header:orders-hash must be passed. This is used to check if any new orders have been placed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orders-hash</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>OrganisationID</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>orderstatus</th>
<td>query</td>
<td>no</td>
<td>List of Order Status id&#x27;s of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>List of payment Statuses of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>fromDate</th>
<td>query</td>
<td>no</td>
<td>The begin date to fetch orders from</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>toDate</th>
<td>query</td>
<td>no</td>
<td>The end date to fetch orders for</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orders/schedule/options




### PUT

<a id="getOrderScheduleOptions">Get options for scheduling an order</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/GetOrderScheduleDto">GetOrderScheduleDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/user/{id}


### GET

<a id="findByUser">Finds User&#x27;s Orders</a>

Finds all Orders for a user, can be filtered by status







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of user to fetch orders for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>

<tr>
<th>orderstatus</th>
<td>query</td>
<td>no</td>
<td>List of Order Status id&#x27;s of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>List of payment Statuses of orders to fetch</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Orders">Orders</a>]|

















## /orders/{id}


### GET

<a id="findOrder">Returns orders for id</a>

returns order for id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of orders (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/Orders">Orders</a>|

















## /orders/{id}/add/item




### PUT

<a id="addItemToOrder">Add a item to an order</a>

Add a item to an order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The Item to add to the order</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderItemDto">CreateOrderItemDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/accepted




### PUT

<a id="acceptedProduct">Update product status with specific ID to Accepted</a>

Update product status with specific @id to Accepted







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/canceled




### PUT

<a id="cancelProduct">Update product status with specific ID to cancelled</a>

Update product status with specific @id to cancelled







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/collected




### PUT

<a id="collectedProduct">Update product status with specific ID to Collected</a>

Update product status with specific @id to Collected







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/complete




### PUT

<a id="completeProduct">Update product status with specific ID to Completed</a>

Update product status with specific @id to Completed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/delivered




### PUT

<a id="deliveredProduct">Update product status with specific ID to Delivered</a>

Update product status with specific @id to Delivered







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/ready




### PUT

<a id="readyProduct">Update product status with specific ID to Ready</a>

Update product status with specific @id to Ready







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/rejected




### PUT

<a id="rejectedProduct">Update product status with specific ID to Declined</a>

Update product status with specific @id to Declined







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{orderItemId}/status/self_picked_up




### PUT

<a id="self_picked_upProduct">Update product status with specific ID to Self Picked Up</a>

Update product status with specific @id to Self Picked Up







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The OrderItem Id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/item/{productId}/status/pending




### PUT

<a id="pendingProduct">Update product status with specific ID to pending</a>

Update product status with specific @id to pending







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>the product id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/pay/cod






### POST


<a id="payViaCOD">Pay for an order via Cash</a>

The amount for the payment. Equals the order total and does not get passed along.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Order Id thats being paid</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/CODPaymentShortDto">CODPaymentShortDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 400    | Failed to return data |  - |
| 404    | Order not found |  - |














## /orders/{id}/pay/creditcard/{paymentGateway}






### POST


<a id="payViaCreditCard">Pay for an order via Credit Card</a>

The amount for the payment. Equals the order total and does not get passed along.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Order Id thats being paid</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/CreditCardPaymentShortDto">CreditCardPaymentShortDto</a>
</td>

</tr>

<tr>
<th>paymentGateway</th>
<td>path</td>
<td>yes</td>
<td>The Payment Gateway</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 400    | Failed to return data |  - |
| 404    | Order not found |  - |














## /orders/{id}/pay/eft/{paymentGateway}






### POST


<a id="payViaEFT">Pay for an order via EFT</a>

The amount for the payment. Equals the order total and does not get passed along.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Order Id thats being paid</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/EftPaymentDto">EftPaymentDto</a>
</td>

</tr>

<tr>
<th>paymentGateway</th>
<td>path</td>
<td>yes</td>
<td>The Payment Gateway</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 400    | Failed to return data |  - |
| 404    | Order not found |  - |














## /orders/{id}/remove/item/{orderItemId}








### DELETE

<a id="removeOrderItemFromOrder">Update an item on the order</a>

Call will update all values passed for the order item @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The id of the order item to remove from the order (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /orders/{id}/reverse/payment






### POST


<a id="reversePayment">Reverse a payment for an order</a>

Reverse a payment for an order







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Order Id who&#x27;s payments must be reversed</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 400    | Failed to return data |  - |
| 404    | Order not found |  - |














## /orders/{id}/status/canceled




### PUT

<a id="cancelOrders">Cancel order with specific ID</a>

Cancel order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be cancelled (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/status/completed




### PUT

<a id="completeOrders">Mark order with specific ID as completed</a>

Mark order with specific @id as completed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{id}/update/item/{orderItemId}




### PUT

<a id="updateOrderItem">Update an item on the order</a>

Call will update all values passed for the order item @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orderItemId</th>
<td>path</td>
<td>yes</td>
<td>The id of the order item to remove from the order (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The Item to update on the order</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderItemDto">CreateOrderItemDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/agent/{deliveryAgentId}




### PUT

<a id="assignDeliveryAgentToOrder">Assign an delivery agent to the order</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be assigned to the delivery agent (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>deliveryAgentId</th>
<td>path</td>
<td>yes</td>
<td>Id of the delivery agent that will be assigned to the order (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/estimate


### GET

<a id="getOrderDeliveryEstimateTime">Get the estimated time for delivery of an order</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order to get an estimate for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orders/{orderId}/invoice




### PUT

<a id="emailOrderInvoice">Send email to the order client containing an invoice as an attachment</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>email</th>
<td>query</td>
<td>yes</td>
<td>Email address to send invoice to</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/organisation/{orgId}/status/accept




### PUT

<a id="acceptOrders">Reject order with specific ID</a>

Reject order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be rejected (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation doing the rejection (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message and estimated time to complete order</td>
<td> - </td>

<td>

<a href="#/definitions/AcceptOrderStatusDto">AcceptOrderStatusDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/organisation/{orgId}/status/collected




### PUT

<a id="collectOrders">Reject order with specific ID</a>

Reject order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be rejected (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation doing the rejection (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Reason why it is ready</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/organisation/{orgId}/status/declined




### PUT

<a id="rejectedOrders">Reject order with specific ID</a>

Reject order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be rejected (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation doing the rejection (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Reason why it is beeing rejected</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/organisation/{orgId}/status/ready




### PUT

<a id="readyOrders">Reject order with specific ID</a>

Reject order with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be rejected (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation doing the rejection (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Reason why it is ready</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/organisation/{orgId}/status/self_picked_up




### PUT

<a id="selfPickedUpOrders">Self Pick up  items at certain organisation with specific ID</a>

Self Pick up  items at certain organisation with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>ID of Order that needs to be set as self picked up (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation that user is picking up from (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/mapping/{posOrganisationId}/status/accept




### PUT

<a id="acceptOrderViaPointOfSale">Change order items status to accepted for items associated with the organisation.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/mapping/{posOrganisationId}/status/collected




### PUT

<a id="collectedOrderViaPointOfSale">Change order items status to collected for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/mapping/{posOrganisationId}/status/customer_collected




### PUT

<a id="customerCollectedOrderViaPointOfSale">Change order items status to customer collected for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/mapping/{posOrganisationId}/status/ready




### PUT

<a id="readyOrderViaPointOfSale">Change order items status to ready for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/mapping/{posOrganisationId}/status/reject




### PUT

<a id="rejectOrderViaPointOfSale">Change order items status to rejected for items associated with the organisation.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>posOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/{organisationId}/status/accept




### PUT

<a id="acceptOrderViaPointOfSaleByID">Change order items status to accepted for items associated with the organisation.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/{organisationId}/status/collected




### PUT

<a id="collectedOrderViaPointOfSaleByID">Change order items status to collected for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/{organisationId}/status/customer_collected




### PUT

<a id="customerCollectedOrderViaPointOfSaleByID">Change order items status to customer collected for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/{organisationId}/status/ready




### PUT

<a id="readyOrderViaPointOfSaleByID">Change order items status to ready for items associated with the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/pos/organisation/{organisationId}/status/reject




### PUT

<a id="rejectOrderViaPointOfSaleByID">Change order items status to rejected for items associated with the organisation.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>Id of the order that will be updated (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation Id the POS uses to identify organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Message associated with the status change.</td>
<td> - </td>

<td>

<a href="#/definitions/StatusMessageDto">StatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderId}/status/delivered




### PUT

<a id="deliverOrders">Mark order with specific ID as delivered</a>

Mark order with specific @id as delivered







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orderId</th>
<td>path</td>
<td>yes</td>
<td>the order id (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderid}/item/extra


### GET

<a id="findItemExtras">returns all the OrderItems</a>

returns all the OrderItems







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrderItemExtra">OrderItemExtra</a>]|




### PUT

<a id="addOrderItemExtra">Create OrderItemExtra</a>

Create OrderItemExtra







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>OrderItemExtraDto containing all the data</td>
<td> - </td>

<td>

<a href="#/definitions/OrderItemExtraDto">OrderItemExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderid}/item/option


### GET

<a id="findOrderItemOptions">returns all the OrderItemOption</a>

returns all the OrderItemOption







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of recoreds per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrderItemOption">OrderItemOption</a>]|




### PUT

<a id="addOrderItemOption">Create OrderItemOption</a>

Create OrderItemOption







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>OrderItemOptionDto containing all the data</td>
<td> - </td>

<td>

<a href="#/definitions/OrderItemOptionDto">OrderItemOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders/{orderid}/item/option/{id}


### GET

<a id="findOrderItemOption">Find OrderItemOption with specific ID</a>

Find OrderItemOption with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of OrderItemOption that needs to be fetched (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orders_source


### GET

<a id="listAllSources">Returns all possible order sources</a>

Returns all possible order sources







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="create">Create new source</a>

Create new source







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the new source</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderSourceChannelDto">CreateOrderSourceChannelDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /orders_source/{sourceId}


### GET

<a id="findById">Searches for match of source id</a>

Returns source that matches the id provided







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>sourceId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Order Source (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="update">Update source</a>

Update source







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>sourceId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Order Source (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the source</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrderSourceChannelDto">CreateOrderSourceChannelDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /orders_source/{sourceName}


### GET

<a id="findByName">Searches for match of source name</a>

Returns source that matches the name provided







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>sourceName</th>
<td>path</td>
<td>yes</td>
<td>Name of the Order Source</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /orderstatusmessage


### GET

<a id="findAll">Returns all the Order Status Message</a>

Returns all the Order Status Message







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Messages Data | Array[<a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>]|

















## /orderstatusmessage/active


### GET

<a id="findActive">Find active Order Status Messages</a>

Find active Order Status Messages







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Messages Data | <a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>|
| 404    | Order Status Messages not found |  - |
| 409    | Message Type already exists |  - |

















## /orderstatusmessage/for/organisation/{organisation_id}


### GET

<a id="findByOrganisation">Returns all the Order Status Messages for Organisation</a>

Returns all the Order Status Messages for Organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisation_id</th>
<td>path</td>
<td>yes</td>
<td>the ID for the organisation</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of recoreds per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message Data | Array[<a href="#/definitions/MessageTemplateDto">MessageTemplateDto</a>]|
| 404    | Order Status Message[id=Long] not found |  - |

















## /orderstatusmessage/orderstatusmessage




### PUT

<a id="create">Create a new Order Status Message</a>

Creates a new Order Status Message







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Order Status Message Data</td>
<td> - </td>

<td>

<a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Order Status Message created |  - |
| 400    | Order Status Message body not valid |  - |
| 409    | Order Status Message already exists |  - |















## /orderstatusmessage/send/{organisation}/{status}


### GET

<a id="sendMessageForOrganisationStatus">Send Order Status Message from specific organisation for a status</a>

Send Order Status Message from specific organisation for a status







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisation</th>
<td>path</td>
<td>yes</td>
<td>ID of the organisation linked to the Order Status Message that needs to be send</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>status</th>
<td>path</td>
<td>yes</td>
<td>ID of the status linked to the Order Status Message that needs to be send</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message Sent |  - |
| 404    | Order Status[id=Long] not found |  - |

















## /orderstatusmessage/template/{template}/organisation/{organisation}


### GET

<a id="findByTemplateOrganisation">Find Order Status Message with specific template and organisation</a>

Find Order Status Message with specific template and organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>template</th>
<td>path</td>
<td>yes</td>
<td>ID of the template linked to the Order Status Message that needs to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisation</th>
<td>path</td>
<td>yes</td>
<td>ID of the organisation linked to the Order Status Message that needs to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message data | <a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>|
| 404    | Organisation[id=Long] not found |  - |

















## /orderstatusmessage/template/{template}/organisation/{organisation}/status/{status}


### GET

<a id="findByTemplateOrganisationStatus">Find Order Status Message with specific template and organisation and status</a>

Find Order Status Message with specific template and organisation and status







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>template</th>
<td>path</td>
<td>yes</td>
<td>ID of the template linked to the Order Status Message that needs to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisation</th>
<td>path</td>
<td>yes</td>
<td>ID of the organisation linked to the Order Status Message that needs to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>status</th>
<td>path</td>
<td>yes</td>
<td>ID of the status linked to the Order Status Message that needs to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message data | <a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>|
| 404    | Order Status[id=Long] not found |  - |

















## /orderstatusmessage/{id}


### GET

<a id="findOneOrderStatusMessage">Find Order Status Message with specific ID</a>

Find Order Status Message with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Order Status Message that needs to be retrieved (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Messages Data | <a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>|
| 404    | Order Status Message[id=Long] not found |  - |
| 409    | Message Type already exists |  - |






### POST


<a id="updateOrderStatusMessage">Update a Order Status Message</a>

Update a Order Status Message







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of OrderStatusMessage that needs to be updated (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>ID of OrderStatusMessage DTO containing the data that needs to be updated</td>
<td> - </td>

<td>

<a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message updated |  - |
| 400    | Order Status Message body not valid |  - |
| 404    | Order Status Message[id=Long] not found |  - |





### DELETE

<a id="deleteOrderStatusMessage">Delete Order Status Message with specific ID</a>

Delete Order Status Message with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Order Status Message that needs to be deleted (**Pattern**: `[0..9]+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Order Status Message deleted |  - |
| 404    | Order Status Message[id=Long] not found |  - |











## /organisations






### POST


<a id="createOrganisation">Create an Organisation</a>

Create a Organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Organisation to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationDto">CreateOrganisationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Organisation Created |  - |
| 400    | Could not create Organisation |  - |
| 404    | Could not find Organisation Type |  - |














## /organisations/address


### GET

<a id="viewGeo">view all Organisation geos</a>

view all Organisation geos







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>|
| 404    | Organisation not found |  - |






### POST


<a id="createGEOLocation">create a new OrganisationGeo</a>

returns the created OrganisationGeo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the OrganisationGeo information</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationGeoDto">CreateOrganisationGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>|
| 201    | Geo Created |  - |
| 400    | Geo body is not valid |  - |
| 404    | User not found |  - |














## /organisations/address/{id}




### PUT

<a id="updateGEO">update a OrganisationGeo</a>

returns the updated OrganisationGeo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the user id who the OrganisationGeo beLongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the OrganisationGeo information</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationGeoDto">CreateOrganisationGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>|
| 404    | Geo not found |  - |















## /organisations/balance


### GET

<a id="getOrganisationBalance">Get transactions for a organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to calculate balance</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to calucate balance</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | OrganisationNotFound |  - |

















## /organisations/busy






### POST


<a id="setShopToBusy">Set the organisations status as Busy.</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/children


### GET

<a id="findChildOrganisationConnection">Find linked child organisations</a>

Find organisations that are linked as children to Organisation. This will be franchisees etc







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>page to display </td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>number of records per page </td>
<td>1</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/close






### POST


<a id="setShopToClose">Set the organisations status as as closed.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to close</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to close</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of bussiness hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/connections


### GET

<a id="findConnectionByOrganisation">Find All Connections linked to organisation</a>

Find Connections that beLong to the organisation with @id







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>type</th>
<td>query</td>
<td>no</td>
<td>The connection type, id or code </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>status</th>
<td>query</td>
<td>yes</td>
<td>connection status to be updated too</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>radius</th>
<td>query</td>
<td>no</td>
<td>The radius in meters of organisations at the other end of an connection</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>lat</th>
<td>query</td>
<td>no</td>
<td>Explicit latitude to search in range of</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>lon</th>
<td>query</td>
<td>no</td>
<td>Explicit longitude to search in range of</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>industry</th>
<td>query</td>
<td>no</td>
<td>Filter for industries the organisations form part of</td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|






### POST


<a id="createOrganisationConnection">Create a new Connection object</a>

Creates a new Connection







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>Connection Details</th>
<td>body</td>
<td>yes</td>
<td>Connectiond etails for connection</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationConnectionDto">CreateOrganisationConnectionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/connections/type/{typeCode}


### GET

<a id="findOrganisationConnectionByType">Find organisation connections by type</a>

Find organisations connection of a certain type. This will be franchisees etc







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>typeCode</th>
<td>path</td>
<td>yes</td>
<td>Organisation type </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>page to display </td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>number of records per page </td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/delivering






### POST


<a id="setShopToDelivering">Set that the organisation is delivering orders.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of business hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/delivery/area


### GET

<a id="getDeliveryAreas">Get Delivery Areas linked to an organisation</a>

Get List of Delivery areas linked to an organisation







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="createDeliveryArea">Add a delivery area for an organisation</a>

Creates a new delivery area for an organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>The details of the delivery area</td>
<td> - </td>

<td>

<a href="#/definitions/CreateDeliveryAreaDto">CreateDeliveryAreaDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/delivery/area/available


### GET

<a id="getIsDeliveryAvailable">Get if delivery is available at location</a>

Get if location falls within the delivery range.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>lat</th>
<td>query</td>
<td>no</td>
<td>The latitude of the location</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>lon</th>
<td>query</td>
<td>no</td>
<td>The longitude of the location</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/delivery/area/{areaId}




### PUT

<a id="updateDeliveryArea">Update a area from an organisations delivery areas</a>

Update an area from an organisations delivery areas







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>areaId</th>
<td>path</td>
<td>yes</td>
<td>The id of the delivery area (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>The details of the delivery area</td>
<td> - </td>

<td>

<a href="#/definitions/CreateDeliveryAreaDto">CreateDeliveryAreaDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteDeliveryArea">Remove an area from an organisations delivery areas</a>

Remove an area from an organisations delivery areas







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>areaId</th>
<td>path</td>
<td>yes</td>
<td>The id of the delivery area (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /organisations/detail




### PUT

<a id="updateOrganisationDetail">Update a new profile details for the given organisation</a>

Create a new profile details for the given organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>Profile Details</th>
<td>body</td>
<td>yes</td>
<td>Profile details for Organisation</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationProfileDto">CreateOrganisationProfileDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/fee/split


### GET

<a id="getFeeSplitJson">Get organisations fee split rules on an order</a>

Get organisation fee split rules on an order







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateFeeSplitJson">Update fee split rules on an order</a>

Update fee split rules on an order







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The details of the feeSplit</td>
<td> - </td>

<td>

<a href="#/definitions/FeeSplitStructureDto">FeeSplitStructureDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/float


### GET

<a id="getOrganisationFloat">Current float for organisation</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/fraud


### GET

<a id="findAll">returns all the fraud entries</a>

returns all the fraud entries







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>The sorting order of the records returned. date+ newest first, date- oldest first</td>
<td>date+</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FraudDto">FraudDto</a>]|

















## /organisations/fraud/deliveryagent/{id}


### GET

<a id="findByDeliveryAgent">returns all the fraud by delivery agent</a>

returns all the fraud by delivery agent







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of delivery agent to fetch fraud for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FraudDto">FraudDto</a>]|

















## /organisations/fraud/fraudlevel/{id}


### GET

<a id="findByFraudLevel">returns all the fraud by fraud level</a>

returns all the fraud by fraud level







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>fraud level (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int32)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FraudDto">FraudDto</a>]|

















## /organisations/fraud/organisation/{id}


### GET

<a id="findByOrganisation">returns all the fraud by organisation</a>

returns all the fraud by organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation to fetch fraud for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/FraudDto">FraudDto</a>]|

















## /organisations/fraud/{id}


### GET

<a id="findFraud">Returns fraud for id</a>

returns fraud for id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of fraud entry (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/Orders">Orders</a>|

















## /organisations/hours


### GET

<a id="getOrganisationOperatingHours">Get operating hours for the given organisation</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrganisationOperatingHoursDto">OrganisationOperatingHoursDto</a>]|




### PUT

<a id="createOrganisationOperatingHours">Create/update operating hours for the given organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>Operating hours</th>
<td>body</td>
<td>yes</td>
<td>List of operating hours for specific days</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateOrganisationOperatingHoursDto">CreateOrganisationOperatingHoursDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/import




### PUT

<a id="importOrganisations">Import organisations from csv</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Csv file containing import data</td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/inventory/product/organisation/{productOrganisationId}






### POST


<a id="createOrganisationProduct">Create an inventory item for another organisation your organisation manages</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the product is linked to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The details of the product to create.</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/inventory/product/{productId}




### PUT

<a id="updateOrganisationProduct">Update an inventory item for another organisation your organisation manages</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>The id of the product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The details of the product to update.</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/inventory/{organisationId}/product/organisation/{productOrganisationId}






### POST


<a id="createOrganisationProduct">Create an inventory item for another organisation your organisation manages</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the product is linked to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The details of the product to create.</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/inventory/{organisationId}/product/{productId}




### PUT

<a id="updateOrganisationProduct">Update an inventory item for another organisation your organisation manages</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>The id of the product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The details of the product to update.</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/not_delivering






### POST


<a id="setShopToNotDelivering">Set that the organisation is not delivering orders.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of business hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/offline






### POST


<a id="setShopToOffline">Set the organisations status as Offline.</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/open






### POST


<a id="setShopToOpen">Set the organisations status as open.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to open</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to open</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of bussiness hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/radius/{meters}


### GET

<a id="findSurroundingOrganisations">Find other organisations within a specified meter radius</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>meters</th>
<td>path</td>
<td>yes</td>
<td>Distance of which to check for other organisations (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/settings


### GET

<a id="getOrganisationSettings">Return all settings for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="addOrganisationSetting">Add a setting for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The key and the value of the setting to be created</td>
<td> - </td>

<td>

<a href="#/definitions/SettingDto">SettingDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/settings/bulk




### PUT

<a id="addOrganisationSettingInBulk">Add a settings for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The key and the value of the settings to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/SettingDto">SettingDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/settings/tag/{tagId}


### GET

<a id="getOrganisationSettingsForTag">Get all settings for an organisation, grouped by a certain tag.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>tagId</th>
<td>path</td>
<td>yes</td>
<td>The id of the tag the settings are grouped under. (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>0</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/settings/{settingId}


### GET

<a id="getOrganisationSetting">Return a specific setting for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>settingId</th>
<td>path</td>
<td>yes</td>
<td>The id of the setting for the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/settlements


### GET

<a id="getAllSettlements">Get a list of all settlements made by organisation, if no dates are passed the last 30 days settlements are returned</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>0</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/setup/typeindustry




### PUT

<a id="setupTypeIndustry">Update the organisation type and industry</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Type and Industry details</td>
<td> - </td>

<td>

<a href="#/definitions/TypeIndustryDto">TypeIndustryDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/shift_manager_on_duty


### GET

<a id="getShiftManagerOnDuty">Get first contact person&#x27;s details</a>

Get the active floor manager contact, for the current shift, responsible for orders at this organisation







#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateShiftManagerOnDuty">Update first contact person&#x27;s details</a>

Update the active floor manager contact, for the current shift, responsible for orders at this organisation







#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/transactions


### GET

<a id="getOrganisationTransactions">Get transactions for a organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | OrganisationIdNotFound |  - |

















## /organisations/types


### GET

<a id="findTypes">Organisations types</a>

Returns availbale types for organisations







#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrganisationTypeDto">OrganisationTypeDto</a>]|

















## /organisations/user/{userId}


### GET

<a id="findByUser">Find all Organisations For a User</a>

Find organisation(s) that beLong to the user with @userId







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>User ID</th>
<td>path</td>
<td>yes</td>
<td>ID of the user</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrganisationDto">OrganisationDto</a>]|

















## /organisations/{id}/address


### GET

<a id="viewGeo">view all Organisation geos</a>

view all Organisation geos







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the Organisation id who the OrganisationGeo beLongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>|
| 404    | Organisation not found |  - |






### POST


<a id="createGEOLocation">create a new OrganisationGeo</a>

returns the created OrganisationGeo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the Organisation id who the OrganisationGeo beLongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the OrganisationGeo information</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationGeoDto">CreateOrganisationGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>|
| 201    | Geo Created |  - |
| 400    | Geo body is not valid |  - |
| 404    | User not found |  - |














## /organisations/{id}/busy






### POST


<a id="setShopToBusy">Set the organisations status as Busy.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{id}/close






### POST


<a id="setShopToClose">Set the organisations status as as closed.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to close</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to close</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of bussiness hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{id}/delivering






### POST


<a id="setShopToDelivering">Set that the organisation is delivering orders.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of business hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{id}/detail


### GET

<a id="findActiveDetailWithId">View Organisation Detail</a>

View details for the given organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/OrganisationProfileDto">OrganisationProfileDto</a>|

















## /organisations/{id}/not_delivering






### POST


<a id="setShopToNotDelivering">Set that the organisation is not delivering orders.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to delivering</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of business hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{id}/offline






### POST


<a id="setShopToOffline">Set the organisations status as Offline.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{id}/open






### POST


<a id="setShopToOpen">Set the organisations status as open.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>startDate</th>
<td>query</td>
<td>no</td>
<td>From date and time to set shop to open</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>endDate</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get set the shop to open</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>message</th>
<td>query</td>
<td>no</td>
<td>Message to clarify the anomaly of bussiness hours</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{organisationId1}/connections/organisation/{organisationId2}


### GET

<a id="findConnectionsBetweenOrganisations">Find All Connections between 2 organisatoins</a>

Is used to find all connections between two organisations. This will display more than one connection if different ypes of connections are present







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId1</th>
<td>path</td>
<td>yes</td>
<td>ID of an organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId2</th>
<td>path</td>
<td>yes</td>
<td>ID of an organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>type</th>
<td>query</td>
<td>no</td>
<td>The connection type, id or code </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|

















## /organisations/{organisationId}




### PUT

<a id="updateOrganisation">Update an Organisation</a>

Update a Organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id if the organisation to update (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details to update Organisation with</td>
<td> - </td>

<td>

<a href="#/definitions/UpdateOrganisationDto">UpdateOrganisationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Organisation updated |  - |
| 400    | Could not create Order |  - |
| 404    | Could not find Organisation |  - |















## /organisations/{organisationId}/accesstoken


### GET

<a id="getAccessToken">Get the OAuth access token for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="resetAccessToken">Reset the OAuth access token for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/balance


### GET

<a id="getOrganisationBalance">View teh balance of an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to calculate balance</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to calucate balance</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | OrganisationNotFound |  - |

















## /organisations/{organisationId}/children


### GET

<a id="findChildOrganisationConnection">Find linked child organisations</a>

Find organisations that are linked as children to Organisation. This will be franchisees etc







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation id </td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>page to display </td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>number of records per page </td>
<td>1</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/connections


### GET

<a id="findConnectionByOrganisation">Find All Connections linked to organisation</a>

Find Connections that beLong to the organisation with @id







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation that needs its connections to be retrieved</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>Comma separated list of fields to sort on. Prepend + or - for ascending and descending Fields:fromOrganisation, toOrganisation, type</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>type</th>
<td>query</td>
<td>no</td>
<td>The connection type, id or code </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>status</th>
<td>query</td>
<td>yes</td>
<td>connection status to be updated too</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>radius</th>
<td>query</td>
<td>no</td>
<td>The radius in meters of organisations at the other end of an connection</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>lat</th>
<td>query</td>
<td>no</td>
<td>Explicit latitude to search in range of</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>lon</th>
<td>query</td>
<td>no</td>
<td>Explicit longitude to search in range of</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>industry</th>
<td>query</td>
<td>no</td>
<td>Filter for industries the organisations form part of</td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ConnectionDto">ConnectionDto</a>|






### POST


<a id="createOrganisationConnection">Create a new Connection object</a>

Creates a new Connection







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation from the connection is created</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>Connection Details</th>
<td>body</td>
<td>yes</td>
<td>Connectiond etails for connection</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationConnectionDto">CreateOrganisationConnectionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{organisationId}/connections/type/{typeCode}


### GET

<a id="findOrganisationConnectionByType">Find organisation connections by type</a>

Find organisations connection of a certain type. This will be franchisees etc







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation id </td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>typeCode</th>
<td>path</td>
<td>yes</td>
<td>Organisation type </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>show disabled connections</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td>the sorting string </td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>page to display </td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>number of records per page </td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/delivery/methods


### GET

<a id="getDeliveryMethods">Get available delivery methods for an organisation</a>

Get available delivery methods for an organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation to get delivery methods for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/detail




### PUT

<a id="updateOrganisationDetail">Update a new profile details for the given organisation</a>

Create a new profile details for the given organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation from the details is created (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>Profile Details</th>
<td>body</td>
<td>yes</td>
<td>Profile details for Organisation</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOrganisationProfileDto">CreateOrganisationProfileDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/float


### GET

<a id="getOrganisationFloat">Current float for organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/hours


### GET

<a id="getOrganisationOperatingHours">Get operating hours for the given organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation for the operating hours (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/OrganisationOperatingHoursDto">OrganisationOperatingHoursDto</a>]|




### PUT

<a id="createOrganisationOperatingHours">Create/update operating hours for the given organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation for the operating hours (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>Operating hours</th>
<td>body</td>
<td>yes</td>
<td>List of operating hours for specific days</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateOrganisationOperatingHoursDto">CreateOrganisationOperatingHoursDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/radius/{meters}


### GET

<a id="findSurroundingOrganisations">Find other organisations within a specified meter radius</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>meters</th>
<td>path</td>
<td>yes</td>
<td>Distance of which to check for other organisations (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/resthooks


### GET

<a id="getRestHooks">List all of my organisation&#x27;s rest hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>eventType</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>atOrganisationId</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>Array[integer] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="register">Register a new ReST hook</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>ReST hook registration info</td>
<td> - </td>

<td>

<a href="#/definitions/RestHookCreationDto">RestHookCreationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /organisations/{organisationId}/resthooks/eventTypes


### GET

<a id="getEventTypes">List the events that I can register for</a>









#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/resthooks/{resthookId}


### GET

<a id="getRestHook">Get one of my ReST hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="update">Update one of my ReST hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>ReST hook registration to update</td>
<td> - </td>

<td>

<a href="#/definitions/RestHookCreationDto">RestHookCreationDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="delete">Unregister one of my ReST hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /organisations/{organisationId}/resthooks/{resthookId}/activate




### PUT

<a id="activate">Activate one of my ReST hooks</a>

A call will be made to the registered url with a secret key. The hook must respond 200 - Ok with the same key before any events will be served.







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/resthooks/{resthookId}/deactivate




### PUT

<a id="deactivate">Deactivate one of my ReST hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/resthooks/{resthookId}/test


### GET

<a id="test">Test one of my ReST hooks</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>resthookId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/settings


### GET

<a id="getOrganisationSettings">Return all settings for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the settings are for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="addOrganisationSetting">Add a setting for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the setting is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The key and the value of the setting to be created</td>
<td> - </td>

<td>

<a href="#/definitions/SettingDto">SettingDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/settings/bulk




### PUT

<a id="addOrganisationSettingInBulk">Add a settings for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the setting is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The key and the value of the settings to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/SettingDto">SettingDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/settings/tag/{tagId}


### GET

<a id="getOrganisationSettingsForTag">Get all settings for an organisation, grouped by a certain tag.</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the setting is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>tagId</th>
<td>path</td>
<td>yes</td>
<td>The id of the tag the settings are grouped under. (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>0</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/settings/{settingId}


### GET

<a id="getOrganisationSetting">Return a specific setting for an organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation that the setting is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settingId</th>
<td>path</td>
<td>yes</td>
<td>The id of the setting for the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/settlements


### GET

<a id="getAllSettlements">Get a list of all settlements made by organisation, if no dates are passed the last 30 days settlements are returned</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td></td>
<td>0</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td></td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/setup/typeindustry




### PUT

<a id="setupTypeIndustry">Update the organisation type and industry</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Type and Industry details</td>
<td> - </td>

<td>

<a href="#/definitions/TypeIndustryDto">TypeIndustryDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/shift_manager_on_duty


### GET

<a id="getShiftManagerOnDuty">Get first contact person&#x27;s details</a>

Get the active floor manager contact, for the current shift, responsible for orders at this organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /organisations/{organisationId}/shift_manager_on_duty/{userId}




### PUT

<a id="updateShiftManagerOnDutyCrossOrganisation">Update first contact person&#x27;s details</a>

Update the active floor manager contact, for the current shift, responsible for orders at this organisation







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /organisations/{organisationId}/transactions


### GET

<a id="getOrganisationTransactions">Get transactions for a organisation</a>









#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the organisation (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td>Transaction Types to filter on</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | OrganisationIdNotFound |  - |

















## /payments


### GET

<a id="findAll">returns all the Payments</a>

returns all the Payments







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | Array[<a href="#/definitions/Payment">Payment</a>]|

















## /payments/gateway/{gatewayid}


### GET

<a id="findByGatewayId">Search for Payment by PaymentGateway ID</a>

Search for Payment by @PaymentGatewayID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>gatewayid</th>
<td>path</td>
<td>yes</td>
<td>Search of Payment by PaymentGateway ID</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 404    | Payment Gateway[value=Long] not found |  - |

















## /payments/organisation/{id}


### GET

<a id="findByOrganisation">Search for Payment by Organisation</a>

Search for Payment by @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Search of Payment by Organisation</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>Date from which to begin getting results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>to</th>
<td>query</td>
<td>no</td>
<td>Date up until which to get results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>paymentmethod</th>
<td>query</td>
<td>no</td>
<td>Payment methods to include in the results</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>

<tr>
<th>paymentstatus</th>
<td>query</td>
<td>no</td>
<td>Payment with Statuses to include in the results</td>
<td> - </td>


<td>Array[string] (csv)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data |  - |
| 400    | Failed to return data |  - |
| 404    | Organisation[id=Long] not found |  - |

















## /payments/user/{userId}/organisation/{organisationId}


### GET

<a id="getUserOrganisationPayments">Get Payments a user made to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>Id of the user to who made the payments (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation the user made payments to (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>Date from which to begin getting results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>to</th>
<td>query</td>
<td>no</td>
<td>Date up until which to get results</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /payments/{id}


### GET

<a id="findWithId">returns a single Payment</a>

X-Ordercloud-organisation determines if the payment can be viewsed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | <a href="#/definitions/PaymentDto">PaymentDto</a>|
| 403    | Not Allowed to view Payment |  - |
| 404    | Payment Not Found |  - |

















## /payments/{id}/three_d_secure


### GET

<a id="findThreeDSecure">returns 3dSecure form on payment</a>

X-Ordercloud-organisation determines if the payment can be viewed







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns Data | <a href="#/definitions/PaymentDto">PaymentDto</a>|
| 403    | Not Allowed to view Payment |  - |
| 404    | Payment Not Found |  - |

















## /plu/extras/organisation/{orgId}


### GET

<a id="getCSVPluForExtraByOrganisation">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which extras belongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/library/extra/organisation/{organisationId}


### GET

<a id="downloadProductLibraryExtraPluMappingAtOrganisation">Download PLU mapping of product library extras for the given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="batchCreateProductLibraryExtraPlus">Batch create PLUs and map it to product library extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/extra/{libraryExtraId}


### GET

<a id="getProductLibraryExtraPlu">Get PLU for the given product library extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryExtraId</th>
<td>path</td>
<td>yes</td>
<td>The product library extra ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryExtraPlu">Create a PLU and map it to a product library extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryExtraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/extra/{libraryExtraId}/organisation/{organisationId}


### GET

<a id="getProductLibraryExtraPlu">Get PLU for the given product library extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryExtraId</th>
<td>path</td>
<td>yes</td>
<td>The product library extra ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryExtraPlu">Create a PLU and map it to a product library extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryExtraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/item/organisation/{atOrganisationId}


### GET

<a id="downloadProductLibraryItemPluMappingAtOrganisation">Download PLU mapping of product library items for the given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>atOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>The host organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/library/item/organisation/{organisationId}






### POST


<a id="batchCreateProductLibraryItemPlus">Batch create PLUs and map it to product library items</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the PLUs are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLUs to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/item/{libraryItemId}


### GET

<a id="getProductLibraryItemPlu">Get the PLU for the given product library item</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>The product library item ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryItemPlu">Create a PLU and map it to a product library item</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/item/{libraryItemId}/organisation/{organisationId}


### GET

<a id="getProductLibraryItemPlu">Get the PLU for the given product library item</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>The product library item ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the PLU are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryItemPlu">Create a PLU and map it to a product library item</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the PLU is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/option/organisation/{organisationId}


### GET

<a id="downloadProductLibraryOptionPluMappingAtOrganisation">Download PLU mapping of product library options for the given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="batchCreateProductLibraryOptionPlus">Batch create PLUs and map it to product library options</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/option/{libraryOptionId}


### GET

<a id="getProductLibraryOptionPlu">Get PLU for the given product library option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryOptionId</th>
<td>path</td>
<td>yes</td>
<td>The product library option ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryOptionPlu">Create a PLU and map it to a product library option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryOptionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/option/{libraryOptionId}/organisation/{organisationId}


### GET

<a id="getProductLibraryOptionPlu">Get the PLU for the given product library option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryOptionId</th>
<td>path</td>
<td>yes</td>
<td>The product library option ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryOptionPlu">Create a PLU and map it to a product library option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryOptionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/organisation/{atOrganisationId}


### GET

<a id="downloadProductLibraryContentPluMappingAtOrganisation">Download all PLU mappings of product library content for the given organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>atOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>The organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="uploadProductLibraryContentPluMapping">Upload a CSV file with your new PLU mappings</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Form data with CSV file&#x27;s key = &#x27;csvfile&#x27;</td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>

<tr>
<th>atOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which the PLUs belong to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/library/{plu}


### GET

<a id="lookupProductLibraryContent">Lookup library item, option or extra by PLU</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>plu</th>
<td>path</td>
<td>yes</td>
<td>The PLU lookup value</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/library/{plu}/organisation/{organisationId}


### GET

<a id="lookupProductLibraryContent">Lookup library items, options or extras by PLU</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>plu</th>
<td>path</td>
<td>yes</td>
<td>The PLU lookup value</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/options/organisation/{orgId}


### GET

<a id="getCSVPluForOptionByOrganisation">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which options belongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/organisation/{orgId}


### GET

<a id="getCSVPluByOrganisation">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which plus belongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/organisation/{orgId}/upload






### POST


<a id="uploadPluMappingCSVFile">Upload a CSV file with your new PLU mappings</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Form data with CSV file&#x27;s key = &#x27;csvfile&#x27;</td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which the PLUs belong to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/extra/organisation/{organisationId}






### POST


<a id="batchCreatePluForProductExtra">Create external plus and map it to an product extras. This is a batch operation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/extra/{extraId}


### GET

<a id="getPluForProductExtra">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product Extra that you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductExtra">Create external plu and map it to an product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product extra the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/extra/{extraId}/organisation/{organisationId}


### GET

<a id="getPluForProductExtra">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product Extra that you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductExtra">Create external plu and map it to an product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product extra the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/organisation/{orgId}


### GET

<a id="getCSVPluForProductByOrganisation">Get Plu for the given product extra</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to which product belongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** text/plain


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/product/organisation/{organisationId}






### POST


<a id="batchCreatePluForProductItem">Create external plu&#x27;s and map it to an products. </a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU&#x27;s to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/{productId}


### GET

<a id="getPluForProduct">Get Plu for the given product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product the you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductItem">Create external plu and map it to an product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/product/{productId}/organisation/{organisationId}


### GET

<a id="getPluForProduct">Get Plu for the given product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product the you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductItem">Create external plu and map it to an product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/productoption/organisation/{organisationId}






### POST


<a id="batchCreatePluForProductOption">Create external plus and map it to an product options. This is a batch operation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>
Array[<a href="#/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/productoption/{optionId}


### GET

<a id="getPluForProductOption">Get Plu for the given product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product  option that you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductOption">Create external plu and map it to an product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/productoption/{optionId}/organisation/{organisationId}


### GET

<a id="getPluForProductOption">Get Plu for the given product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product  option that you want to find the plu for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu are for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createPluForProductOption">Create external plu and map it to an product option</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option the PLU maps to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for the PLU to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExternalPluDto">CreateExternalPluDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /plu/{plu}


### GET

<a id="getForPlu">Get Item or Option or Extra that is linked to the given plu</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>plu</th>
<td>path</td>
<td>yes</td>
<td>The plu you want to look up</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /plu/{plu}/organisation/{organisationId}


### GET

<a id="getForPlu">Get Item or Option or Extra that is linked to the given plu</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>plu</th>
<td>path</td>
<td>yes</td>
<td>The plu you want to look up</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID that the plu is for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /product


### GET

<a id="findByCurrentOrganisation">returns all the Product</a>

returns all the Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showdisabled</th>
<td>query</td>
<td>yes</td>
<td>display disabled products</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Product">Product</a>]|
| 404    | Organisation[id=Long] not found |  - |






### POST


<a id="createProductByOrganisation">Create Product</a>

Create Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for Product to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Created |  - |
| 400    | Product body is not valid |  - |
| 404    | Organisation[id=Long] not found |  - |
| 409    | Product already exists |  - |














## /product/attributes


### GET

<a id="findByOrganisation">returns all the product attribute</a>

Find all Product Attributes for an Organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>amount of records per page</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled products</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes Data | <a href="#/definitions/ProductAttributeDto">ProductAttributeDto</a>|
| 404    | Organisation[id=@orgId] not found |  - |






### POST


<a id="createProductAttribute">create product attribute</a>

Creates a Product Attribute with a name, description and price. It has to be unique per organisation. A attribute can be assigned to more than one product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information of the Product Attribute to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateAttributeDto">CreateAttributeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Attribute Created |  - |
| 400    | Product Attribute body is not valid |  - |
| 404    | Organisation[id=Long] not found |  - |
| 409    | Product Attribute already exists |  - |














## /product/attributes/organisation/{orgId}


### GET

<a id="findByOrganisation">returns all the product attribute</a>

Find all Product Attributes for an Organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Id of the organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>no</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>no</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled products</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes Data | <a href="#/definitions/ProductAttributeDto">ProductAttributeDto</a>|
| 404    | Organisation[id=@orgId] not found |  - |






### POST


<a id="createProductAttribute">create product attribute</a>

Creates a Product Attribute with a name, description and price. It has to be unique per organisation. A attribute can be assigned to more than one product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>ID of the organisation to crate the attribute for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information of the Product Attribute to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateAttributeDto">CreateAttributeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Attribute Created |  - |
| 400    | Product Attribute body is not valid |  - |
| 404    | Organisation[id=Long] not found |  - |
| 409    | Product Attribute already exists |  - |














## /product/attributes/{id}


### GET

<a id="findOneProductAttribute">Find Product Attribute with specific ID</a>

Product Attribute with the requested ID is returned.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Find for Product Attribute with ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attribute data | <a href="#/definitions/ProductAttributeDto">ProductAttributeDto</a>|
| 404    | Product Attribute[id=Long] not found |  - |




### PUT

<a id="updateProductAttribute">Update Product Attribute with specific ID</a>

Update the Product Attribute







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Product Attribute that needs to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information of the Product Attribute</td>
<td> - </td>

<td>

<a href="#/definitions/CreateAttributeDto">CreateAttributeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Attribute Updated |  - |
| 400    | Attribute body is not valid |  - |
| 404    | Product Attribute[id=Long] not found |  - |






### DELETE

<a id="deleteProductAttribute">Delete Product Attribute with specific ID</a>

Remove a Product Attribute. This is the same as disable







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Attribute to delete (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes removed successful |  - |
| 400    | Failed to remove Product Attribute |  - |
| 404    | Product Attribute[id=Long] not found |  - |











## /product/attributes/{id}/disable




### PUT

<a id="disableProductAttribute">Disable Product Attribute with specific ID</a>

Disables the product attribute. Disabled product attributes will not be visible in finds







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Attribute to disable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes disabled successful |  - |
| 400    | Failed to disable Product Attribute |  - |
| 404    | Product Attribute[id=Long] not found |  - |















## /product/attributes/{id}/enable




### PUT

<a id="enableProductAttribute">Enable Product Attribute with specific ID</a>

Enabled Product Attributes will be available in finds.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Attribute to enable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes enabled successful |  - |
| 400    | Failed to enable Product Attribute |  - |
| 404    | Product Attribute[id=Long] not found |  - |















## /product/connection/{id}


### GET

<a id="findByConnection">Get all Products through a Connection</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Connection ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>The current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>Amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showdisabled</th>
<td>query</td>
<td>yes</td>
<td>Show/Hide disabled Products</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Product">Product</a>]|
| 404    | Connection[id=Long] not found |  - |

















## /product/criteria




### PUT

<a id="findAllByCriteria">returns all the Products for Criteria</a>

returns all the Products for Criteria







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the criteria</td>
<td> - </td>

<td>

<a href="#/definitions/ProductSearchCriteriaDto">ProductSearchCriteriaDto</a>
</td>

</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showdisabled</th>
<td>query</td>
<td>yes</td>
<td>display disabled products</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ProductDto">ProductDto</a>]|















## /product/discount/brand/{organisationBrandId}


### GET

<a id="getDiscountForBrand">Get discounts for a brand</a>

Get product discounts for a brand







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationBrandId</th>
<td>path</td>
<td>yes</td>
<td>organisationBrandId the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled discounts</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createDiscountForBrand">Create discount for a specific brand</a>

Discount for a specific brand







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationBrandId</th>
<td>path</td>
<td>yes</td>
<td>Brand organisation Id the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>Details of Discount</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/discount/connection/{connectionId}


### GET

<a id="getDiscountForConnection">Get discounts for a connection</a>

Get product discounts for a connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>Connection the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled discounts</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createDiscountForConnection">Create discount for a specific Connection</a>

Discount for a specific Connection







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>productId the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>Details of Discount</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/discount/organisation/{organisationId}


### GET

<a id="getDiscountForOrganisation">Get discounts for an organisation</a>

Get product discounts for an organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled discounts</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createDiscountForOrganisation">Create discount for organisation</a>

Discount for all products in that organisation







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>Details of Discount</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/discount/product/{productId}


### GET

<a id="getDiscountForProduct">Get discounts for a product</a>

Get product discounts for a product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>no</td>
<td>Show disabled discounts</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createDiscountForProduct">Create discount for a specific product </a>

Discount for a specific product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>productId the discount is for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>Details of Discount</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/discount/{id}


### GET

<a id="findProductDiscount">Find ProductDiscount Details</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the discount (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |








### DELETE

<a id="disableDiscount">Disable a specific discount </a>

Disable a specific discount







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the discount (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/extras






### POST


<a id="createProductExtra">create a product extra</a>

Create a product extra for a specified organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>product extra information to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExtraDto">CreateExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Extra created successful |  - |
| 400    | Failed to create Product Extra |  - |
| 404    | Organisation[id=Long] not found |  - |














## /product/extras/organisation/{orgId}






### POST


<a id="createProductExtra">create a product extra</a>

Create a product extra for a specified organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>organisation id to link product extras too (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>product extra information to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExtraDto">CreateExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Extra created successful |  - |
| 400    | Failed to create Product Extra |  - |
| 404    | Organisation[id=Long] not found |  - |














## /product/extras/set


### GET

<a id="findAllExtraSet">Gets all sets for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createExtraSet">Create a set for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/extras/set/{extraSetId}


### GET

<a id="findExtraSet">Get a set for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateExtraSet">Update a set for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Extra Set Id (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="disableExtraSet">Disable a set for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/extras/set/{extraSetId}/enable




### PUT

<a id="enableExtraSet">Enable a set for extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/extras/{extraId}/set/{extraSetId}




### PUT

<a id="linkExtraToExtraSet">Link an extra to a set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkExtraFromExtraSet">Link an extra to a set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/extras/{id}


### GET

<a id="findOneProductExtra">return product extra</a>

returns product extra with specified id.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Search for ProductExtra with ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Extra found successful | <a href="#/definitions/Product Extra">Product Extra</a>|
| 404    | Product Extra[id=Long] not found |  - |




### PUT

<a id="updateProductExtra">update specific product extra</a>

Update product extra details. Cannot be moved from organisation it is assigned too.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product extra to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information of the ProductExtra</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExtraDto">CreateExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Extra updated successful |  - |
| 400    | Failed to create Product Extra |  - |
| 404    | Product Extra[id=Long] not found |  - |






### DELETE

<a id="deleteProductExtra">remove product extra</a>

Remove product extra. Has the same functionality as disable.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product extra  to be deleted (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Extra deleted successful |  - |
| 400    | Failed to delete Product Extra |  - |
| 404    | Product Extra[id=Long] not found |  - |











## /product/extras/{id}/disable




### PUT

<a id="disableProductExtra">disable product extras</a>

Disables all product extras. Disabled products will not be available in searches or be able to be added on Products.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product extra to be disabled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Extra disabled successful |  - |
| 400    | Failed to disable Product Extra |  - |
| 404    | Product Extra[id=Long] not found |  - |















## /product/extras/{id}/enable




### PUT

<a id="enableProductExtra">enable product extra</a>

Enable product extra. Once enabled the product it will be available to searches and to add on Products.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product extra to be enabled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Extra enabled successful |  - |
| 400    | Failed to enabled Product Extra |  - |
| 404    | Product Extra[id=Long] not found |  - |















## /product/library/attributes


### GET

<a id="findAll">Return list of attributes from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled attributes. Defaults to false</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryAttribute">Create attribute in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library attribute to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductLibraryAttributeDto">CreateProductLibraryAttributeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/attributes/organisation/{orgId}


### GET

<a id="findAllForOrganisation">Return list of attributes from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Organisation (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled attributes</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryAttributeByOrganisation">Create attribute in the product library for organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library attribute to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductLibraryAttributeDto">CreateProductLibraryAttributeDto</a>
</td>

</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Organisation. Defaults to false (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/attributes/{attributeId}


### GET

<a id="findProductLibraryAttribute">Return attribute from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>attributeId</th>
<td>path</td>
<td>yes</td>
<td>Product library attributeId ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateProductLibraryAttribute">Update attribute in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>attributeId</th>
<td>path</td>
<td>yes</td>
<td>Product library attribute ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library attribute to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductLibraryAttributeDto">CreateProductLibraryAttributeDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteProductLibraryAttribute">Delete attribute in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>attributeId</th>
<td>path</td>
<td>yes</td>
<td>Product library attribute ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/attributes/{id}/disable




### PUT

<a id="disableProductAttribute">Disable Product Attribute with specific ID</a>

Disables the product attribute. Disabled product attributes will not be visible in finds







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Attribute to disable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Library Attributes disabled successful |  - |
| 400    | Failed to disable Product Attribute |  - |
| 404    | Product Attribute[id=Long] not found |  - |















## /product/library/attributes/{id}/enable




### PUT

<a id="enableProductAttribute">Enable Product Attribute with specific ID</a>

Enabled Product Attributes will be available in finds.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Library Attribute to enable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Library Attributes enabled successful |  - |
| 400    | Failed to enable Product Library Attribute |  - |
| 404    | Product Attribute[id=Long] not found |  - |















## /product/library/extras


### GET

<a id="findAllForOrganisation">Return list of extras from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryExtra">Create extra in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library extra to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExtraDto">CreateExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/extras/set


### GET

<a id="findAllLibraryExtraSet">Gets all sets for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createLibraryExtraSet">Create a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/extras/set/{extraSetId}


### GET

<a id="findLibraryExtraSet">Get a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateLibraryExtraSet">Update a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="disableLibraryExtraSet">Disable a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/extras/set/{extraSetId}/copy/{newSetName}




### PUT

<a id="copyLibraryExtraSet">Copy a set for extras in the product library including extras</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>newSetName</th>
<td>path</td>
<td>yes</td>
<td>Name of the new extra set</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/extras/set/{extraSetId}/enable




### PUT

<a id="enableLibraryExtraSet">Disable a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/extras/{extraId}


### GET

<a id="findProductLibraryExtra">Return extra from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateProductLibraryExtra">update an extra in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library extra to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateExtraDto">CreateExtraDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteProductLibraryExtra">delete extra in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/extras/{extraId}/set/{extraSetId}




### PUT

<a id="linkLibraryExtraToLibraryExtraSet">Link an extra to a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkLibraryExtraFromLibraryExtraSet">unlink an extra from a set for extras in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>extraId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options


### GET

<a id="findAllForOrganisation">Return list of options from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryOption">Create option in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library option to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOptionDto">CreateOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/options/set


### GET

<a id="findAllLibraryOptionSet">Gets all sets for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createLibraryOptionSet">Create a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/options/set/{optionSetId}


### GET

<a id="findLibraryOptionSet">Get a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateLibraryOptionSet">Update a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="disableLibraryOptionSet">Disable a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options/set/{optionSetId}/copy/{newSetName}




### PUT

<a id="copyLibraryOptionSet">Copy a set for options in the product library including options</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>newSetName</th>
<td>path</td>
<td>yes</td>
<td>Name of the new option set</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/options/set/{optionSetId}/enable




### PUT

<a id="enableLibraryOptionSet">Enable a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/options/{optionId}


### GET

<a id="findProductLibraryOption">Return option from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateProductLibraryOption">update an option in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library option to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOptionDto">CreateOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteProductLibraryOption">delete option in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options/{optionId}/disable








### DELETE

<a id="disableProductLibraryOption">Disable option in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options/{optionId}/enable




### PUT

<a id="enableProductLibraryOption">Enable option in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/options/{optionId}/set/{optionSetId}




### PUT

<a id="linkLibraryOptionToLibraryOptionSet">Link an option to a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkLibraryOptionFromLibraryOptionSet">remove an option from a set for options in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options/{optionId}/unlock/extras/set/{extraSetId}




### PUT

<a id="addExtraUnlockExtraSet">Set the extra set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="removeExtraSetFromExtraUnlock">Remove the extra set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/options/{optionId}/unlock/options/set/{optionSetId}




### PUT

<a id="addOptionUnlockOptionSet">Set the option set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="removeOptionSetFromOptionUnlock">Set the option set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products


### GET

<a id="findAllForOrganisation">Return list of products from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createProductLibraryItem">Create item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library item to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductLibraryItemDto">CreateProductLibraryItemDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/library/products/brand_owner/{organisationId}


### GET

<a id="findAllForBrandOwner">Return list of products from the product library that is a brand of the organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to be used (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /product/library/products/copy/organisation/{fromOrganisationId}/organisation/{toOrganisationId}




### PUT

<a id="copyProductLibraryToProduct">Copy products from an organisations product library to another organisations products</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>fromOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID from who&#x27;s library the products will be copied (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>toOrganisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to who&#x27;s library the products will be copied (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>List of product library ID&#x27;s to be copied, if empty entire library will be copied the products will be copied</td>
<td> - </td>

<td>
Array[<a href=""></a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/organisation/{organisationId}/export


### GET

<a id="exportProductLibrary">Export organisation product library to csv</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID from who&#x27;s library will be exported (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /product/library/products/organisation/{organisationId}/import




### PUT

<a id="importProductLibrary">Import organisation product library from csv</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID for who the product library will be imported (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Csv file containing import data</td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/{libraryItemId}


### GET

<a id="findProductLibraryItem">Return product from the product library linked to an organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateProductLibraryItem">Update item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Product library item details</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductLibraryItemDto">CreateProductLibraryItemDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteProductLibraryItem">Delete item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products/{libraryItemId}/attribute


### GET

<a id="viewProductAttribute">View attributes</a>

Returns the attributes on specific library product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute View call was successfull |  - |




### PUT

<a id="addProductAttribute">Add Attribute</a>

Adds a attribute with a value to a product. Updates the attribute if all ready present on the product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Name of the attribute</td>
<td> - </td>

<td>
Array[<a href="#/definitions/AddAttributeDto">AddAttributeDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute  added successfully |  - |
| 404    | Product[id=Long] not found |  - |















## /product/library/products/{libraryItemId}/attribute/{attributeName}








### DELETE

<a id="removeProductAttribute">Remove an attribute set</a>

Remove a specific attribute set from Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>attributeName</th>
<td>path</td>
<td>yes</td>
<td>Name of the attribute</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute set removed successfully |  - |
| 404    | Attribute[name=String] not found |  - |











## /product/library/products/{libraryItemId}/available_online/{isAvailable}




### PUT

<a id="updateIsAvailableOnline">Set whether an product library item is available online.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>isAvailable</th>
<td>path</td>
<td>yes</td>
<td>True or False, whether product is available Online</td>
<td> - </td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/{libraryItemId}/disable








### DELETE

<a id="disableProductLibraryItem">Disable item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products/{libraryItemId}/enable




### PUT

<a id="enableProductLibraryItem">Enable item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/{libraryItemId}/extras/set/{extraSetId}




### PUT

<a id="linkItemToExtraSet">Link an product library extra set to an item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkExtraSetFromItem">Unlink an product library extra set from an item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products/{libraryItemId}/grouping/{libraryGroupItemId}




### PUT

<a id="addItemToGrouping">Add a item to a group type product library item.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product to be linked to group (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>libraryGroupItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product that is a grouping (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="removeItemFromGrouping">Remove an item from the grouping product library item.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product to be unlinked from the group (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>libraryGroupItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product that is a grouping (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products/{libraryItemId}/image




### PUT

<a id="uploadImage">Upload image associated with the product.</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Image Data in image key </td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>

<tr>
<th>format</th>
<td>query</td>
<td>no</td>
<td>Format for result</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>default</th>
<td>query</td>
<td>no</td>
<td>Is the this image the default for the product</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/{libraryItemId}/image/{imageName}








### DELETE

<a id="deleteImage">Delete image from the product.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>imageName</th>
<td>path</td>
<td>yes</td>
<td>Name of the image to delete</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/library/products/{libraryItemId}/image/{imageName}/default




### PUT

<a id="setImageAsDefault">Set Image as default</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID of product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>imageName</th>
<td>path</td>
<td>yes</td>
<td>Name of the image to make the default</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/library/products/{libraryItemId}/images


### GET

<a id="viewImages">Returns image associated with the product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>ID of the product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>format</th>
<td>query</td>
<td>no</td>
<td>Format for result</td>
<td> - </td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /product/library/products/{libraryItemId}/options/set/{optionSetId}




### PUT

<a id="linkItemToOptionSet">Link an product library option set to an item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkOptionSetFromItem">Unlink an product library option set from an item in the product library</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>libraryItemId</th>
<td>path</td>
<td>yes</td>
<td>Product library item ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product library option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/options


### GET

<a id="findByCurrentOrganisation">returns all the product options for organisation</a>

Returns all the product options. This call has paging enabled.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes Data | Array[<a href="#/definitions/ProductOptionDto">ProductOptionDto</a>]|






### POST


<a id="createProductOption">create a product option</a>

Create a product option for a specified organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>product option information to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOptionDto">CreateOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Option created successful |  - |
| 400    | Failed to create Product Option |  - |
| 404    | Organisation[id=Long] not found |  - |














## /product/options/organisation/{orgId}


### GET

<a id="findByOrganisation">returns all the product options for organisation</a>

Returns all the product options. This call has paging enabled.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>organisation id linked to product options (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Attributes Data | Array[<a href="#/definitions/ProductOptionDto">ProductOptionDto</a>]|






### POST


<a id="createProductOption">create a product option</a>

Create a product option for a specified organisation.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>organisation id to link product options too (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>product option information to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOptionDto">CreateOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Option created successful |  - |
| 400    | Failed to create Product Option |  - |
| 404    | Organisation[id=Long] not found |  - |














## /product/options/set


### GET

<a id="findAllOptionSet">Gets all Option Sets</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="createOptionSet">Create a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /product/options/set/{optionSetId}


### GET

<a id="findOptionSet">Get a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateOptionSet">Update a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the set to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSetDto">CreateSetDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="disableOptionSet">Disable a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/options/set/{optionSetId}/enable




### PUT

<a id="enableOptionSet">Enable a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/options/{id}


### GET

<a id="findOneProductOption">return product option</a>

returns product option with specified id.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Search for ProductOption with ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Option found successful | <a href="#/definitions/ProductOptionDto">ProductOptionDto</a>|
| 404    | Product Option[id=Long] not found |  - |




### PUT

<a id="updateProductOption">update specific product option</a>

Update product option details. Cannot be moved from organisation it is assigned too.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product option to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information of the ProductOption</td>
<td> - </td>

<td>

<a href="#/definitions/CreateOptionDto">CreateOptionDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Option updated successful |  - |
| 400    | Failed to create Product Option |  - |
| 404    | Product Option[id=Long] not found |  - |






### DELETE

<a id="deleteProductOption">remove product option</a>

Remove product option. Has the same functionality as disable.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product option  to be deleted (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Option deleted successful |  - |
| 400    | Failed to delete Product Option |  - |
| 404    | Product Option[id=Long] not found |  - |











## /product/options/{id}/disable




### PUT

<a id="disableProductOption">disable product options</a>

Disables all product options. Disabled products will not be available in searches or be able to be added on Products.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product option to be disabled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Option disabled successful |  - |
| 400    | Failed to disable Product Option |  - |
| 404    | Product Option[id=Long] not found |  - |















## /product/options/{id}/enable




### PUT

<a id="enableProductOption">enable product option</a>

Enable product option. Once enabled the product it will be available to searches and to add on Products.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>id of product option to be enabled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Option enabled successful |  - |
| 400    | Failed to enabled Product Option |  - |
| 404    | Product Option[id=Long] not found |  - |















## /product/options/{optionId}/set/{optionSetId}




### PUT

<a id="linkOptionToOptionSet">Link an option to a Option Set</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="unlinkOptionFromOptionSet">Link an option to a set for options</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/options/{optionId}/unlock/extras/set/{extraSetId}




### PUT

<a id="addExtraUnlockExtraSet">Set the extra set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="removeExtraSetFromExtraUnlock">Remove the extra set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Product extra set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/options/{optionId}/unlock/options/set/{optionSetId}




### PUT

<a id="addOptionUnlockOptionSet">Set the option set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="removeOptionSetFromOptionUnlock">Set the option set an option unlocks when selected</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>optionId</th>
<td>path</td>
<td>yes</td>
<td>Product option ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Product option set ID (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/organisation/{id}


### GET

<a id="findByOrganisation">Get all Products for an Organisation</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>The current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>Amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>showdisabled</th>
<td>query</td>
<td>yes</td>
<td>Show/Hide disabled products</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/Product">Product</a>]|
| 404    | Organisation[id=Long] not found |  - |






### POST


<a id="createProductByOrganisation">Create Product</a>

Create Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Organisation ID to be used (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for Product to be created</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Product Created |  - |
| 400    | Product body is not valid |  - |
| 404    | Organisation[id=Long] not found |  - |
| 409    | Product already exists |  - |














## /product/tag


### GET

<a id="findProductTagForOrganisation">returns all the Product Tag</a>

returns all the Product Tag







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/ProductTag">ProductTag</a>]|
| 404    | Product [id=Long] not found |  - |






### POST


<a id="createTag">Create a product tag</a>

Create a product tag







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>The tag to create</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductTagDto">CreateProductTagDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ProductTag">ProductTag</a>|
| 201    | Product Tag Created |  - |
| 400    | Product Tag create failed |  - |
| 404    | Product Tag Type not found |  - |
| 409    | Product Tag allreadt exists |  - |














## /product/tag/organisation/{id}


### GET

<a id="findProductTagForOrganisation">returns all the Product Tag</a>

returns all the Product Tag







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation that needs to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/ProductTag">ProductTag</a>]|
| 404    | Product [id=Long] not found |  - |

















## /product/tag/organisation/{id}/type/{name}


### GET

<a id="findTagsForOrganisationByTagTypeName">returns all the Product Tags for a Type</a>

returns all the Product Tags fo a type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation that needs to be used (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>name</th>
<td>path</td>
<td>yes</td>
<td>Name of Tag type</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/Product Tag">Product Tag</a>]|
| 404    | TagType [id=Long] not found |  - |

















## /product/tag/organisation/{id}/type/{type_id}


### GET

<a id="findTagsForOrganisationByTagId">returns all the Product Tags for a Type</a>

returns all the Product Tags for a Type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>ID of Organisation that needs to be used (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>type_id</th>
<td>path</td>
<td>yes</td>
<td>ID of Tag type (**Pattern**: `  \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/ProductTagType">ProductTagType</a>]|
| 404    | TagType [id=Long] not found |  - |

















## /product/tag/type/{name}


### GET

<a id="findTagsForOrganisationByTagTypeName">returns all the Product Tags for a Type</a>

returns all the Product Tags fo a type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>name</th>
<td>path</td>
<td>yes</td>
<td>Name of Tag type</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/Product Tag">Product Tag</a>]|
| 404    | TagType [id=Long] not found |  - |

















## /product/tag/type/{type_id}


### GET

<a id="findTagsForOrganisationByTagId">returns all the Product Tags for a Type</a>

returns all the Product Tags for a Type







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>type_id</th>
<td>path</td>
<td>yes</td>
<td>ID of Tag type (**Pattern**: `  \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>showDisabled</th>
<td>query</td>
<td>yes</td>
<td>Show disabled tags</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Data | Array[<a href="#/definitions/ProductTagType">ProductTagType</a>]|
| 404    | TagType [id=Long] not found |  - |

















## /product/tag/types


### GET

<a id="findAllTagTypes">returns all the Product Tag Types</a>

returns all the Product Tag Types







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Type Data | Array[<a href="#/definitions/ProductTagType">ProductTagType</a>]|

















## /product/tag/{id}


### GET

<a id="findOneProductTag">Search for Product Tags with specific ID</a>

Search for Product Tags with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found |  - |




### PUT

<a id="updateTag">Update a product tag</a>

Update a product tag







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tag update (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the tag to update</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductTagDto">CreateProductTagDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Updated | <a href="#/definitions/ProductTag">ProductTag</a>|
| 400    | Product Tag update failed |  - |
| 404    | Product Tag Type not found |  - |






### DELETE

<a id="deleteProductTag">Delete Product Tags with specific ID</a>

Delete Product Tags with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to delete (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag removed successful |  - |
| 400    | Failed to remove Product Tag |  - |
| 404    | Product Tag[id=Long] not found |  - |











## /product/tag/{id}/change/disable




### PUT

<a id="disableProductTag">Disable Product Tags with specific ID</a>

Disable Product Tags with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to disable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag disable successful |  - |
| 400    | Failed to disable Product Tag |  - |
| 404    | Product Tag[id=Long] not found |  - |















## /product/tag/{id}/change/enable




### PUT

<a id="enableProductTag">Enable Product Tags with specific ID</a>

Enable Product Tags with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to enable (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag enabled successful |  - |
| 400    | Failed to enable Product Tag |  - |
| 404    | Product Tag[id=Long] not found |  - |















## /product/tag/{id}/child/{childId}




### PUT

<a id="addChildProductTag">Add a child Tag to a Product Tags with specific ID</a>

Add a child Tag to a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>childId</th>
<td>path</td>
<td>yes</td>
<td>Child Product Tags ta add (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found or Child Tag[childId=Long] not found |  - |






### DELETE

<a id="removeChildProductTag">Remove a child Tag from a Product Tags with specific ID</a>

Remove a child Tag from a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>childId</th>
<td>path</td>
<td>yes</td>
<td>Child Product Tags ta remove (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found |  - |











## /product/tag/{id}/children


### GET

<a id="findChildrenProductTag">Search for the children of Product Tags with specific ID</a>

Search for the children of a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found |  - |








### DELETE

<a id="removeAllChildrenProductTag">Remove all children Tags from a Product Tags with specific ID</a>

Remove a children Tags from a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found |  - |











## /product/tag/{id}/parent








### DELETE

<a id="removeParentProductTag">Remove a parent Tag from a Product Tags with specific ID</a>

Remove a parent Tag from a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found |  - |











## /product/tag/{id}/parent/{parentId}




### PUT

<a id="setParentProductTag">Add a parent Tag to a Product Tags with specific ID</a>

Add a parent Tag to a Product Tags with specific ID







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product Tags to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>parentId</th>
<td>path</td>
<td>yes</td>
<td>Parent Product Tags ta add (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag data |  - |
| 404    | Product Tag[id=Long] not found or Parent Tag[parentId=Long] not found |  - |















## /product/tag/{tagId}/type/{typeId}




### PUT

<a id="assignTagType">Update a tag type</a>

assigns a type to a tag







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>tagId</th>
<td>path</td>
<td>yes</td>
<td>ID of Tag that needs to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>typeId</th>
<td>path</td>
<td>yes</td>
<td>ID of Tag Type that needs to be assigned to tag (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Product Tag Type updated |  - |
| 404    | Tag type id not found |  - |















## /product/{id}


### GET

<a id="findOneProduct">Search for Product with specific ID</a>

Search for Product with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product to search for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="updateProduct">Update Product with specific ID</a>

Update Product with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product to update (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Information for Product to be updated</td>
<td> - </td>

<td>

<a href="#/definitions/CreateProductDto">CreateProductDto</a>
</td>

</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### DELETE

<a id="deleteProduct">Remove Product with specific ID</a>

Remove Product with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id Product to search for (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/{productId}/attribute


### GET

<a id="viewProductAttribute">View attributes</a>

Returns the attributes on specifici product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute View call was successfull |  - |




### PUT

<a id="addProductAttribute">Add Attribute</a>

Adds a attribute with a value to a product. Updates the attribute if all ready present on the product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Name of the attribute</td>
<td> - </td>

<td>
Array[<a href="#/definitions/AddAttributeDto">AddAttributeDto</a>]

</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute  added successfully |  - |
| 404    | Product[id=Long] not found |  - |















## /product/{productId}/attribute/{attributeName}








### DELETE

<a id="removeProductAttribute">Remove an attribute set</a>

Remove a specific attribute set from Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>attributeName</th>
<td>path</td>
<td>yes</td>
<td>Name of the attribute</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Attribute set removed successfully |  - |
| 404    | Attribute[name=String] not found |  - |











## /product/{productId}/available_online/{isAvailable}




### PUT

<a id="updateIsAvailableOnline">Set whether an product item is available online.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product ID of product to be updated (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>isAvailable</th>
<td>path</td>
<td>yes</td>
<td>True or False, whether product is available Online</td>
<td> - </td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/{productId}/extras/set


### GET

<a id="findAllProductExtraSets">returns all the Product Extra Sets</a>

returns all the Product Extra sets







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ProductExtra">ProductExtra</a>]|

















## /product/{productId}/extras/set/{extraSetId}


### GET

<a id="findOneProductExtraSet">Search for Product Extra set with specific ID</a>

Search for Product Extra set with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Id Product Extra to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="addProductExtraSetById">Add Extra</a>

Adds a extra set to a product. Extra set must be present in the system.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Extra Set (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Extra(s) added successfully |  - |
| 404    | ExtraSet[id=Long] not found |  - |






### DELETE

<a id="removeProductExtraSetById">Remove an option</a>

Remove a specific option from Product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>extraSetId</th>
<td>path</td>
<td>yes</td>
<td>Id of the extra set (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Extra set removed successfully |  - |
| 404    | ExtraSet[id=Long] not found |  - |











## /product/{productId}/grouping/{productGroupId}




### PUT

<a id="addProductToGroup">Add product to a grouping of products</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product item ID of product to be linked to group (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productGroupId</th>
<td>path</td>
<td>yes</td>
<td>Product item ID of product that is a grouping (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ProductDto">ProductDto</a>|






### DELETE

<a id="removeProductFromGroup">Add product to a grouping of products</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Product item ID of product to be unlinked from the group (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>productGroupId</th>
<td>path</td>
<td>yes</td>
<td>Product item ID of product that is a grouping (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/ProductDto">ProductDto</a>|











## /product/{productId}/image




### PUT

<a id="uploadImage">Upload image associated with the product.</a>









#### Request


**Content-Type: ** multipart/form-data

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>ID of the product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Image Data in image key </td>
<td> - </td>

<td>

<a href="#/definitions/MultipartFormDataInput">MultipartFormDataInput</a>
</td>

</tr>

<tr>
<th>format</th>
<td>query</td>
<td>no</td>
<td>Format for result</td>
<td>false</td>


<td>boolean </td>


</tr>

<tr>
<th>default</th>
<td>query</td>
<td>no</td>
<td>Is the this image the default for the product</td>
<td>false</td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/{productId}/image/{imageName}








### DELETE

<a id="deleteImage">Delete image from the product.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>ID of the product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>imageName</th>
<td>path</td>
<td>yes</td>
<td>Name of the image to delete</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/{productId}/image/{imageName}/default




### PUT

<a id="setImageAsDefault">Set Image as default</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>imageName</th>
<td>path</td>
<td>yes</td>
<td>Name of the image to make the default</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /product/{productId}/images


### GET

<a id="viewImages">Upload image associated with the product.</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>ID of the product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>format</th>
<td>query</td>
<td>no</td>
<td>Format for result</td>
<td> - </td>


<td>boolean </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /product/{productId}/options/set


### GET

<a id="findAllProductOptionSets">returns all the Product Option</a>

returns all the Product Option







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | Array[<a href="#/definitions/ProductOption">ProductOption</a>]|

















## /product/{productId}/options/set/{optionSetId}


### GET

<a id="findOneProductOptionSet">Search for Product Option Set with specific ID</a>

Search for Product Option with specific @id







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Id Product Option set to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionTypeCode</th>
<td>query</td>
<td>no</td>
<td>Specify the connection relationship you have with this organisation</td>
<td>Marketplace</td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |




### PUT

<a id="addProductOptionSetById">Add Option Set</a>

Adds a option Set to a product. Option Set must be present in the system.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Product (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Option (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Option(s) added successfully |  - |
| 404    | OptionSet[id=Long] not found |  - |






### DELETE

<a id="deleteProductOptionSet">removes a product option set from a product</a>

Search for Product Option with specific @id and remove link to product







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>id of the product option (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>optionSetId</th>
<td>path</td>
<td>yes</td>
<td>id product option set to search for (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /product/{productId}/stock/{quantity}




### PUT

<a id="setProductStockLevel">Set the amount of stock available for a product</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>productId</th>
<td>path</td>
<td>yes</td>
<td>Id of product (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>quantity</th>
<td>path</td>
<td>yes</td>
<td>Amount of items in stock (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /reports/schedule


### GET

<a id="getScheduledReportsForOrganisation">Get a list of scheduled report subscriptions for and organisation</a>

Get a list of scheduled report subscriptions for and organisation







#### Request



##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |






### POST


<a id="subscribeToReport">Subscribe to receive an report via email</a>

Subscribe to receive an report via email







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Details of the report to subscribe to</td>
<td> - </td>

<td>

<a href="#/definitions/SubscribeScheduleReportDto">SubscribeScheduleReportDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /reports/schedule/{id}


### GET

<a id="getScheduledReport">Get a scheduled report subscription</a>

Get a scheduled report subscription







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the scheduled report subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |








### DELETE

<a id="deleteScheduledReport">Remove a scheduled report subscription</a>

Remove a scheduled report subscription







#### Request



##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>Id of the scheduled report subscription (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |











## /settlements/manual/eft/{account}/organisation/{orgId}




### PUT

<a id="manualEFT">Create a call to do manual eft</a>

Create a call to do manual eft.







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>account</th>
<td>path</td>
<td>yes</td>
<td>The account number to be settled</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>orgId</th>
<td>path</td>
<td>yes</td>
<td>Id of the Organisation requesting the settlement</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>Settlement Details</td>
<td> - </td>

<td>

<a href="#/definitions/CreateSettlementDto">CreateSettlementDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /settlements/organisation/{organisationId}/connection/{connectionId}




### PUT

<a id="settleConnectionToBank">Call for an organisation to settle the outstanding amount the organisation at the other end of the connection</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation wishing to settle. (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>The id of the connection to be settled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settleAmount</th>
<td>query</td>
<td>no</td>
<td>The amount to settle, if left it will be the total amount</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /settlements/organisation/{organisationId}/connection/{connectionId}/interval/{settlementInterval}




### PUT

<a id="setSettlementInterval">Call for an organisation to set when they would like the connection to be settled</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation to be settled. (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>The id of the connection to be settled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settlementInterval</th>
<td>path</td>
<td>yes</td>
<td>The interval by when to connection is to be settled. Values: MONTLY, WEEKLY, BI_WEEKLY, DAILY</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /settlements/organisation/{organisationId}/connection/{connectionId}/wallet




### PUT

<a id="settleConnectionToWallet">Call for an organisation to settle the outstanding amount the organisation at the other end of the connection</a>









#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>organisationId</th>
<td>path</td>
<td>yes</td>
<td>The id of the organisation wishing to settle. (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>connectionId</th>
<td>path</td>
<td>yes</td>
<td>The id of the connection to be settled (**Pattern**: ` \d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>settleAmount</th>
<td>query</td>
<td>no</td>
<td>The amount to settle, if left it will be the total amount</td>
<td> - </td>


<td>number (double)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |















## /users






### POST


<a id="createUser">Create a new user</a>

Create a new user for the given organisation.







#### Request


**Content-Type: ** application/json, application/xml

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>X-Ordercloud-Organisation</th>
<td>header</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/CreateUserDto">CreateUserDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |














## /users/agency


### GET

<a id="viewDeliveryAgencies">Returns all delivery agencies linked to the user</a>

Retrieves user from the authentication sent along. This call will return a empty list if the user is not registered to any agencies.







#### Request


**Content-Type: ** application/xml, application/json

##### Parameters






#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | UserNotFound |  - |
| 500    | Failed to find authenticated user |  - |

















## /users/geocode




### PUT

<a id="geocodeUserAddress">Returns userGeoDto with Latitude and Longitude populated</a>









#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td>The Geo information to get Geocode for</td>
<td> - </td>

<td>

<a href="#/definitions/UserGeoDto">UserGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | Geocode not found for address |  - |















## /users/geos/{geoId}




### PUT

<a id="updateGEO">update a UserGeo</a>

returns the updated UserGeo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>geoId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the UserGEO to Update (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the UserGeo information</td>
<td> - </td>

<td>

<a href="#/definitions/UserGeoDto">UserGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|
| 404    | Geo not found |  - |















## /users/geos/{id}


### GET

<a id="ViewGeo">view user geo</a>

view user geo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>The user geo to view (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|
| 404    | Geo not found |  - |

















## /users/geos/{id}/disable




### PUT

<a id="disableGEO">Disable given UserGeo</a>

returns updated UserGeo







#### Request


**Content-Type: ** application/json, application/xml

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the UserGeo to disable (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json, application/xml


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|
| 404    | Geo not found |  - |















## /users/geos/{id}/enable




### PUT

<a id="enableGEO">Enable given UserGeo</a>

returns enabled UserGeo







#### Request


**Content-Type: ** application/json, application/xml

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the UserGeo to enable (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json, application/xml


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|
| 404    | Geo not found |  - |















## /users/logged_in


### GET

<a id="findLoggedIn">Find the authenticated user&#x27;s details</a>









#### Request


**Content-Type: ** application/json, application/xml

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | successful operation | <a href="#/definitions/UserDto">UserDto</a>|

















## /users/search


### GET

<a id="findBy">Find users</a>

Find users by email or cellphone. Either email or mobile is required







#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>email</th>
<td>query</td>
<td>no</td>
<td>email of the user</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>mobile</th>
<td>query</td>
<td>no</td>
<td>mobile of the user</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Users Found | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|

















## /users/{id}/geos


### GET

<a id="ViewAllGeos">view all users geos</a>

view all users geos







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the user id who the UserGEO beLongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK | <a href="#/definitions/UserGeoDto">UserGeoDto</a>|
| 404    | User not found |  - |






### POST


<a id="createGEOLocation">create a new UserGeo</a>

returns the created UserGeo







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td>the user id who the UserGEO beLongs to (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>body</th>
<td>body</td>
<td>yes</td>
<td>the UserGeo information</td>
<td> - </td>

<td>

<a href="#/definitions/UserGeoDto">UserGeoDto</a>
</td>

</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 201    | Geo Created |  - |
| 400    | Geo body is not valid |  - |
| 404    | User not found |  - |














## /users/{id}/profile


### GET

<a id="viewUserProfile">Get a users profile details</a>

Details like name firstname







#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json, application/xml


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | User Profile | <a href="#/definitions/UserProfileDto">UserProfileDto</a>|
| 404    | User not found |  - |




### PUT

<a id="updateUserProfile">Update a given users profile details</a>

Update user personal details like name firstname







#### Request


**Content-Type: ** application/json, application/xml

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>body</th>
<td>body</td>
<td>no</td>
<td></td>
<td> - </td>

<td>

<a href="#/definitions/CreateProfileBaseDto">CreateProfileBaseDto</a>
</td>

</tr>

<tr>
<th>id</th>
<td>path</td>
<td>yes</td>
<td> (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/json, application/xml


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Updated User Profile | <a href="#/definitions/ProfileBaseDto">ProfileBaseDto</a>|
| 404    | User not found |  - |















## /users/{userId}/agency


### GET

<a id="viewDeliveryAgencies">Returns all delivery agencies linked to the user</a>

This call will return a







#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the user (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>


</table>



#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | UserNotFound |  - |

















## /users/{userId}/balance


### GET

<a id="getUserBalance">Get transactions for a user</a>









#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the user (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | UserNotFound |  - |

















## /users/{userId}/transactions


### GET

<a id="getUserTransactions">Get transactions for a user</a>









#### Request


**Content-Type: ** application/xml, application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>userId</th>
<td>path</td>
<td>yes</td>
<td>The Id of the user (**Pattern**: `\d+`)</td>
<td> - </td>


<td>integer (int64)</td>


</tr>

<tr>
<th>page</th>
<td>query</td>
<td>yes</td>
<td>the current page number</td>
<td>1</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>pagesize</th>
<td>query</td>
<td>yes</td>
<td>the amount of records per page</td>
<td>20</td>


<td>integer (int32)</td>


</tr>

<tr>
<th>from</th>
<td>query</td>
<td>no</td>
<td>From date to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>upto</th>
<td>query</td>
<td>no</td>
<td>Date up to which to get transactions</td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>sort</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>

<tr>
<th>transactiontypes</th>
<td>query</td>
<td>no</td>
<td></td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/xml, application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | OK |  - |
| 404    | UserNotFound |  - |

















## /verification/email_address


### GET

<a id="verifyEmailAddress">Verify an email address</a>

Users are directed here when they follow the link in the verification email







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>hash</th>
<td>query</td>
<td>yes</td>
<td>Verification hash</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /verification/mobile_number


### GET

<a id="verifyMobileNumber">Verify a mobile number</a>

Users are directed here when they follow the link in the verification sms







#### Request


**Content-Type: ** application/json

##### Parameters

<table border="1">
<tr>
<th>Name</th>
<th>Located in</th>
<th>Required</th>
<th>Description</th>
<th>Default</th>
<th>Schema</th>
</tr>



<tr>
<th>hash</th>
<td>query</td>
<td>yes</td>
<td>Verification hash</td>
<td> - </td>


<td>string </td>


</tr>


</table>



#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| default    | successful operation |  - |

















## /version


### GET

<a id="checkVersion">return the current version</a>

current version of the API







#### Request


**Content-Type: ** application/json

##### Parameters






#### Response

**Content-Type: ** application/json


| Status Code | Reason      | Response Model |
|-------------|-------------|----------------|
| 200    | Returns version | <a href="#/definitions/VersionDto">VersionDto</a>|


















# Definitions

## <a name="/definitions/AcceptOrderStatusDto">AcceptOrderStatusDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>message</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>estimatedReadyTime</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/AddAttributeDto">AddAttributeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/BankDetail">BankDetail</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountHolderName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountHolderSurname</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountType</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>bank</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>branchCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>branchName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>clientNo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CODPaymentShortDto">CODPaymentShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>orderRef</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Connection">Connection</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/ConnectionType">ConnectionType</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ended</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fee</td>
<td>


array[<a href="#/definitions/ConnectionFee">ConnectionFee</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>draftFee</td>
<td>


array[<a href="#/definitions/ConnectionFeeDraft">ConnectionFeeDraft</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settings</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>payments</td>
<td>


array[<a href="#/definitions/Payment">Payment</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settlementInterval</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastSettled</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>priceModifiers</td>
<td>


array[<a href="#/definitions/ConnectionPriceModifier">ConnectionPriceModifier</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>discounts</td>
<td>


array[<a href="#/definitions/ProductDiscount">ProductDiscount</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>priceModifier</td>
<td>

<a href="#/definitions/ConnectionPriceModifier">ConnectionPriceModifier</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Connection Fee">Connection Fee</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>fee type id</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>fee type code</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionDto">ConnectionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromOrganisation</td>
<td>

<a href="#/definitions/OrganisationDto">OrganisationDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>toOrganisation</td>
<td>

<a href="#/definitions/OrganisationDto">OrganisationDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/ConnectionTypeDto">ConnectionTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ended</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fee</td>
<td>


array[<a href="#/definitions/OrganisationFeeDto">OrganisationFeeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>draftFee</td>
<td>


array[<a href="#/definitions/ConnectionFeeDraftDto">ConnectionFeeDraftDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settlementInterval</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFee">ConnectionFee</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>clientPays</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeDetails</td>
<td>


array[<a href="#/definitions/ConnectionFeeDetail">ConnectionFeeDetail</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeType">FeeType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>structure</td>
<td>

<a href="#/definitions/FeeStructure">FeeStructure</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>metric</td>
<td>

<a href="#/definitions/FeeMetric">FeeMetric</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDetail">ConnectionFeeDetail</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDraft">ConnectionFeeDraft</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>clientPays</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeType">FeeType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>structure</td>
<td>

<a href="#/definitions/FeeStructure">FeeStructure</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>metric</td>
<td>

<a href="#/definitions/FeeMetric">FeeMetric</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeDetails</td>
<td>


array[<a href="#/definitions/ConnectionFeeDraftDetail">ConnectionFeeDraftDetail</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDraftDetail">ConnectionFeeDraftDetail</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDraftDetailDto">ConnectionFeeDraftDetailDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDraftDto">ConnectionFeeDraftDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>clientPays</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>proposedByOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeDetails</td>
<td>


array[<a href="#/definitions/ConnectionFeeDraftDetailDto">ConnectionFeeDraftDetailDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeTypeDto">FeeTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>metric</td>
<td>

<a href="#/definitions/FeeMetricDto">FeeMetricDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>structure</td>
<td>

<a href="#/definitions/FeeStructureDto">FeeStructureDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionFeeDto">ConnectionFeeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>clientPays</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeDetails</td>
<td>


array[<a href="#/definitions/OrganisationFeeDetailDto">OrganisationFeeDetailDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeTypeDto">FeeTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>metric</td>
<td>

<a href="#/definitions/FeeMetricDto">FeeMetricDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>structure</td>
<td>

<a href="#/definitions/FeeStructureDto">FeeStructureDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionPriceModifier">ConnectionPriceModifier</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionShortDetailDto">ConnectionShortDetailDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>toOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/ConnectionTypeDto">ConnectionTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fee</td>
<td>


array[<a href="#/definitions/ConnectionFeeDto">ConnectionFeeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>draftFee</td>
<td>


array[<a href="#/definitions/ConnectionFeeDraftDto">ConnectionFeeDraftDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settings</td>
<td>


array[<a href="#/definitions/SettingDto">SettingDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionShortDto">ConnectionShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>toOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/ConnectionTypeDto">ConnectionTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionType">ConnectionType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationSetting</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>group</td>
<td>

<a href="#/definitions/SecurityGroup">SecurityGroup</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ConnectionTypeDto">ConnectionTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ContactPersonUserDto">ContactPersonUserDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/ProfileBaseDto">ProfileBaseDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Coordinate">Coordinate</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>x</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>y</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>z</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CoordinateSequence">CoordinateSequence</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>dimension</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CoordinateSequenceFactory">CoordinateSequenceFactory</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

</table>

## <a name="/definitions/CreateAttributeDto">CreateAttributeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateBatchExternalPluDto">CreateBatchExternalPluDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateConnectionDto">CreateConnectionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>toOrganisationId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromOrganisationId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>typeCode</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateConnectionFeeDetailDto">CreateConnectionFeeDetailDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateConnectionOrganisationFeeDto">CreateConnectionOrganisationFeeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>startDate</td>
<td>


string

</td>
<td>optional</td>
<td>date on which the fee starts</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string

</td>
<td>optional</td>
<td>date on which the fee ends</td>
<td></td>
</tr>

<tr>
<td>details</td>
<td>


array[<a href="#/definitions/CreateConnectionFeeDetailDto">CreateConnectionFeeDetailDto</a>]



</td>
<td>required</td>
<td>details of the fees</td>
<td></td>
</tr>

<tr>
<td>feeType</td>
<td>

<a href="#/definitions/Connection Fee">Connection Fee</a>


</td>
<td>required</td>
<td>type of fee</td>
<td></td>
</tr>

<tr>
<td>feeStructure</td>
<td>

<a href="#/definitions/Fee Structure">Fee Structure</a>


</td>
<td>required</td>
<td>structure of fee</td>
<td></td>
</tr>

<tr>
<td>feeMetric</td>
<td>

<a href="#/definitions/Fee Metric">Fee Metric</a>


</td>
<td>required</td>
<td>volume, price range etc</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>Enabled</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateConnectionSettingDto">CreateConnectionSettingDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settingKeyId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateDeliveryAreaDto">CreateDeliveryAreaDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>radius</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateExternalPluDto">CreateExternalPluDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateExtraDto">CreateExtraDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateMarkupSettingDto">CreateMarkupSettingDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>value</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settingKeyId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateNotificationSubscriptionDto">CreateNotificationSubscriptionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>channel</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>eventType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>recipients</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>parties</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOptionDto">CreateOptionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrderDto">CreateOrderDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>items</td>
<td>


array[<a href="#/definitions/CreateOrderItemDto">CreateOrderItemDto</a>]



</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationId</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>paymentStatus</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>userId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tip</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryCost</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>userGeo</td>
<td>

<a href="#/definitions/UserGeoDto">UserGeoDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryService</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderSourceChannel</td>
<td>

<a href="#/definitions/OrderSourceChannelDto">OrderSourceChannelDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>scheduledTime</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrderItemDetailDto">CreateOrderItemDetailDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>options</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extras</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrderItemDto">CreateOrderItemDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>quantity</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>detail</td>
<td>

<a href="#/definitions/CreateOrderItemDetailDto">CreateOrderItemDetailDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>readyEstimate</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrderSourceChannelDto">CreateOrderSourceChannelDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrganisationConnectionDto">CreateOrganisationConnectionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>toOrganisationId</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>typeCode</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrganisationDto">CreateOrganisationDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>types</td>
<td>


array[integer]

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>timezoneOffset</td>
<td>


integer (int32)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>registeredDirectly</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>industry</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>notificationSourceEmail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>operatingHours</td>
<td>


array[<a href="#/definitions/CreateOrganisationOperatingHoursDto">CreateOrganisationOperatingHoursDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currencyCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrganisationGeoDto">CreateOrganisationGeoDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetName</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>complex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>suburb</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>city</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>postalCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>province</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>country</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrganisationOperatingHoursDto">CreateOrganisationOperatingHoursDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>day</td>
<td>


integer (int32)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>openTime</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>closeTime</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateOrganisationProfileDto">CreateOrganisationProfileDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>contactPerson</td>
<td>

<a href="#/definitions/ContactPersonUserDto">ContactPersonUserDto</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>contactNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>notificationSourceEmail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProductDiscountDto">CreateProductDiscountDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>provider</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProductDto">CreateProductDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>available</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attributes</td>
<td>


array[<a href="#/definitions/AddAttributeDto">AddAttributeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>optionSets</td>
<td>


array[<a href="#/definitions/ProductOptionSetDto">ProductOptionSetDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSetDto">ProductExtraSetDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/Product Tag">Product Tag</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductTypeDto">ProductTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>additionalInfo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProductLibraryAttributeDto">CreateProductLibraryAttributeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProductLibraryItemDto">CreateProductLibraryItemDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductTypeDto">ProductTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>brandOwner</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/Product Tag">Product Tag</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>additionalInfo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProductTagDto">CreateProductTagDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tagType</td>
<td>

<a href="#/definitions/Product Tag Type">Product Tag Type</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateProfileBaseDto">CreateProfileBaseDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>firstName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>surname</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>email</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nickName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>mobileCountryCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateSetDto">CreateSetDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateSettlementDto">CreateSettlementDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>encryptedUserId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreateUserDto">CreateUserDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>mobileNumberCountry</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>password</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>firstName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>surname</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>email</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nickName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumber</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupIds</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sendWelcomeMessage</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CreditCardPaymentShortDto">CreditCardPaymentShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>budgetPeriod</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cardExpiryMonth</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cardExpiryYear</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nameOnCard</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cvv</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cardNumber</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>threeDSecure</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>threeDSecureReturnUrl</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CurrencyDetails">CurrencyDetails</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>isoCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>symbol</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>format</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/CurrencyDto">CurrencyDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>isoCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>symbol</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>format</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DeliveryAgent">DeliveryAgent</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minBalance</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxBalance</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountNo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>walletId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cardNo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/DeliveryAgentStatus">DeliveryAgentStatus</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DeliveryAgentDto">DeliveryAgentDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>user</td>
<td>

<a href="#/definitions/UserProfileDto">UserProfileDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minBalance</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxBalance</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/DeliveryAgentStatusDto">DeliveryAgentStatusDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountNo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cardNo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>walletId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DeliveryAgentStatus">DeliveryAgentStatus</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DeliveryAgentStatusDto">DeliveryAgentStatusDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DeliveryType">DeliveryType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

</table>

## <a name="/definitions/DetailType">DetailType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reverse</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>systemPermissable</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>manualPermissable</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ownerRequired</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DetailTypeDto">DetailTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/DisplayUserDto">DisplayUserDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/EftPaymentDto">EftPaymentDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>amt</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountIdentity</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>detailTypeCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>uuid</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currency</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>testMode</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>bankName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderRef</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>accountHolder</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>branchName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>branchCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Envelope">Envelope</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>height</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>width</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>null</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>area</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minX</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxX</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minY</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxY</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ExternalPlu">ExternalPlu</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Fee Metric">Fee Metric</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>metric id</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>metric code</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Fee Structure">Fee Structure</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>structure id</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>structure code</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeMetric">FeeMetric</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeMetricDto">FeeMetricDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeSplitConditionalDto">FeeSplitConditionalDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>type</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>entity</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>key</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>parties</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connectionType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/FeeSplitTransactionDto">FeeSplitTransactionDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeSplitIterativeDto">FeeSplitIterativeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>param</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/FeeSplitTransactionDto">FeeSplitTransactionDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>conditional</td>
<td>


array[<a href="#/definitions/FeeSplitConditionalDto">FeeSplitConditionalDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeSplitStructureDto">FeeSplitStructureDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>conditional</td>
<td>


array[<a href="#/definitions/FeeSplitConditionalDto">FeeSplitConditionalDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/FeeSplitTransactionDto">FeeSplitTransactionDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>iterative</td>
<td>


array[<a href="#/definitions/FeeSplitIterativeDto">FeeSplitIterativeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeSplitTransactionDto">FeeSplitTransactionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>type</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>entity</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentage</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixed</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>parties</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connectionType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>inclusions</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>exclusions</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>inclusionsPercentage</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeStructure">FeeStructure</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentage</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>flatfee</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeStructureDto">FeeStructureDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentage</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>flatFee</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volume</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeType">FeeType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FeeTypeDto">FeeTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/FraudDto">FraudDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>emailSubject</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fraudLevel</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>user</td>
<td>

<a href="#/definitions/UserDto">UserDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationDto">OrganisationDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryAgent</td>
<td>

<a href="#/definitions/DeliveryAgentDto">DeliveryAgentDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Geometry">Geometry</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>factory</td>
<td>

<a href="#/definitions/GeometryFactory">GeometryFactory</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>userData</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>valid</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>length</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>empty</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>simple</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dimension</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinates</td>
<td>


array[<a href="#/definitions/Coordinate">Coordinate</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>numPoints</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>boundaryDimension</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinate</td>
<td>

<a href="#/definitions/Coordinate">Coordinate</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>geometryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>srid</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>numGeometries</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>precisionModel</td>
<td>

<a href="#/definitions/PrecisionModel">PrecisionModel</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>rectangle</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>area</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>envelopeInternal</td>
<td>

<a href="#/definitions/Envelope">Envelope</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/GeometryFactory">GeometryFactory</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>precisionModel</td>
<td>

<a href="#/definitions/PrecisionModel">PrecisionModel</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinateSequenceFactory</td>
<td>

<a href="#/definitions/CoordinateSequenceFactory">CoordinateSequenceFactory</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>srid</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/GetOrderScheduleDto">GetOrderScheduleDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>organisations</td>
<td>


array[integer]

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromDate</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>toDate</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/GroupDto">GroupDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisations</td>
<td>


array[<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>roles</td>
<td>


array[<a href="#/definitions/RoleDto">RoleDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/GroupingType">GroupingType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/IndustryDto">IndustryDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/InputPart">InputPart</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>headers</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>mediaType</td>
<td>

<a href="#/definitions/MediaType">MediaType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>bodyAsString</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>contentTypeFromMessage</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/InvitationCreationDto">InvitationCreationDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>emailAddress</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/LoyaltyProvider">LoyaltyProvider</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisations</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MediaType">MediaType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>type</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>subtype</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>parameters</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>wildcardType</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>wildcardSubtype</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageGroup">MessageGroup</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>messages</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageGroupDto">MessageGroupDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>messageTemplateList</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageTemplate">MessageTemplate</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>subject</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sequence</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>messages</td>
<td>


array[<a href="#/definitions/OrderStatusMessage">OrderStatusMessage</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/MessageType">MessageType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>grouping</td>
<td>

<a href="#/definitions/MessageGroup">MessageGroup</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>event</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>templatePath</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fromAddress</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageTemplateDto">MessageTemplateDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>subject</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>body</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sequence</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderStatusMessageList</td>
<td>


array[<a href="#/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationDto">OrganisationDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/MessageTypeDto">MessageTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>comMessageGroupId</td>
<td>

<a href="#/definitions/MessageGroupDto">MessageGroupDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageType">MessageType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>size</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxSize</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>templates</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MessageTypeDto">MessageTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>size</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxSize</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/MultipartFormDataInput">MultipartFormDataInput</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>formData</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>formDataMap</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>preamble</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>parts</td>
<td>


array[<a href="#/definitions/InputPart">InputPart</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItem">OrderItem</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>linePrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unitPrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>markupPercentage</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>markup</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>quantity</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>product</td>
<td>

<a href="#/definitions/Product">Product</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrderStatus">OrderStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>order</td>
<td>

<a href="#/definitions/Orders">Orders</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>readyEstimate</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>itemOptions</td>
<td>


array[<a href="#/definitions/OrderItemOption">OrderItemOption</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>itemExtras</td>
<td>


array[<a href="#/definitions/OrderItemExtra">OrderItemExtra</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>itemDiscount</td>
<td>

<a href="#/definitions/OrderItemDiscount">OrderItemDiscount</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>itemError</td>
<td>


array[<a href="#/definitions/OrderItemError">OrderItemError</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nextStatus</td>
<td>

<a href="#/definitions/OrderStatus">OrderStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemDiscount">OrderItemDiscount</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>discount</td>
<td>

<a href="#/definitions/ProductDiscount">ProductDiscount</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>item</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productDiscountedPrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemError">OrderItemError</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>errorMessage</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemExtra">OrderItemExtra</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extra</td>
<td>

<a href="#/definitions/ProductExtra">ProductExtra</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemExtraDto">OrderItemExtraDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extra</td>
<td>

<a href="#/definitions/ProductExtraDisplayDto">ProductExtraDisplayDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemOption">OrderItemOption</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderItem</td>
<td>

<a href="#/definitions/OrderItem">OrderItem</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>option</td>
<td>

<a href="#/definitions/ProductOption">ProductOption</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderItemOptionDto">OrderItemOptionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>option</td>
<td>

<a href="#/definitions/ProductOptionDisplayDto">ProductOptionDisplayDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderPayment">OrderPayment</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>when</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>message</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderSourceChannel">OrderSourceChannel</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderSourceChannelDto">OrderSourceChannelDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderStatus">OrderStatus</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderStatusDto">OrderStatusDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderStatusHistory">OrderStatusHistory</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderStatus</td>
<td>

<a href="#/definitions/OrderStatus">OrderStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>statusMessage</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>statusTimestamp</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderStatusMessage">OrderStatusMessage</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrderStatus">OrderStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>template</td>
<td>

<a href="#/definitions/MessageTemplate">MessageTemplate</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrderStatusMessageDto">OrderStatusMessageDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationDto">OrganisationDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrderStatusDto">OrderStatusDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Orders">Orders</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortReference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>estimatedDeliveryTime</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tip</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>statusHistory</td>
<td>


array[<a href="#/definitions/OrderStatusHistory">OrderStatusHistory</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrderStatus">OrderStatus</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>paymentStatus</td>
<td>


array[<a href="#/definitions/OrderPayment">OrderPayment</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currentPaymentStatus</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>items</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>payments</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>userGeo</td>
<td>

<a href="#/definitions/UserGeo">UserGeo</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryAgent</td>
<td>

<a href="#/definitions/DeliveryAgent">DeliveryAgent</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderSourceChannel</td>
<td>

<a href="#/definitions/OrderSourceChannel">OrderSourceChannel</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryCost</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>scheduledDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastPaymentStatus</td>
<td>

<a href="#/definitions/OrderPayment">OrderPayment</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>itemOrganisations</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Organisation">Organisation</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>types</td>
<td>


array[<a href="#/definitions/OrganisationType">OrganisationType</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>timezoneOffset</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>statusFlowRule</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastOnline</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>delivering</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>open</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>registeredDirectly</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrganisationStatus">OrganisationStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationSetting</td>
<td>


array[<a href="#/definitions/OrganisationSetting">OrganisationSetting</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>industries</td>
<td>


array[<a href="#/definitions/OrganisationIndustry">OrganisationIndustry</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>users</td>
<td>


array[<a href="#/definitions/User">User</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>bankDetail</td>
<td>


array[<a href="#/definitions/BankDetail">BankDetail</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profiles</td>
<td>


array[<a href="#/definitions/OrganisationProfile">OrganisationProfile</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fees</td>
<td>


array[<a href="#/definitions/OrganisationFee">OrganisationFee</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/Transaction">Transaction</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ordersHash</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>operatingHours</td>
<td>


array[<a href="#/definitions/OrganisationOperatingHours">OrganisationOperatingHours</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>anomalyMessage</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeSplitJson</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>loyaltyProviders</td>
<td>


array[<a href="#/definitions/LoyaltyProvider">LoyaltyProvider</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currency</td>
<td>

<a href="#/definitions/CurrencyDetails">CurrencyDetails</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>apiServices</td>
<td>


array[<a href="#/definitions/OrganisationApiServiceDescription">OrganisationApiServiceDescription</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>activeOrganisationProfile</td>
<td>

<a href="#/definitions/OrganisationProfile">OrganisationProfile</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/OrganisationProfile">OrganisationProfile</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationProfile</td>
<td>


array[<a href="#/definitions/OrganisationProfile">OrganisationProfile</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>activeBankDetail</td>
<td>

<a href="#/definitions/BankDetail">BankDetail</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>privateSalt</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>statusFlowRules</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationApiServiceDescription">OrganisationApiServiceDescription</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>apiServiceName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>hostUrl</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>credentials</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationDto">OrganisationDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>types</td>
<td>


array[<a href="#/definitions/OrganisationTypeDto">OrganisationTypeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>industries</td>
<td>


array[<a href="#/definitions/IndustryDto">IndustryDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/OrganisationProfileDto">OrganisationProfileDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>operatingHours</td>
<td>


array[<a href="#/definitions/OrganisationOperatingHoursDto">OrganisationOperatingHoursDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ordersHash</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>

<a href="#/definitions/OrganisationStatusDto">OrganisationStatusDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastOnline</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>delivering</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>open</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>registeredDirectly</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>anomalyMessage</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currency</td>
<td>

<a href="#/definitions/CurrencyDto">CurrencyDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationFee">OrganisationFee</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>feeDetails</td>
<td>


array[<a href="#/definitions/OrganisationFeeDetail">OrganisationFeeDetail</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeType">FeeType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>structure</td>
<td>

<a href="#/definitions/FeeStructure">FeeStructure</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>metric</td>
<td>

<a href="#/definitions/FeeMetric">FeeMetric</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connection</td>
<td>

<a href="#/definitions/Connection">Connection</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationFeeDetail">OrganisationFeeDetail</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationFeeDetailDto">OrganisationFeeDetailDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxValue</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fixedAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>percentageAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>volumeAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationFeeDto">OrganisationFeeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>details</td>
<td>


array[<a href="#/definitions/OrganisationFeeDetailDto">OrganisationFeeDetailDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/FeeTypeDto">FeeTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationGeo">OrganisationGeo</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>complex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>suburb</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>city</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>postalCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>province</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>country</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>geometricLocation</td>
<td>

<a href="#/definitions/Point">Point</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>distance</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationGeoDto">OrganisationGeoDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetName</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>complex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>suburb</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>city</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>postalCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>province</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>country</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationIndustry">OrganisationIndustry</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationOperatingHours">OrganisationOperatingHours</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>day</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>openTime</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>closeTime</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationOperatingHoursDto">OrganisationOperatingHoursDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>day</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>openTime</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>closeTime</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationProfile">OrganisationProfile</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>contactNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>notificationSourceEmail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>address</td>
<td>


array[<a href="#/definitions/OrganisationGeo">OrganisationGeo</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>activeGeo</td>
<td>

<a href="#/definitions/OrganisationGeo">OrganisationGeo</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationProfileDto">OrganisationProfileDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>contactPerson</td>
<td>

<a href="#/definitions/ContactPersonUserDto">ContactPersonUserDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>contactNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>notificationSourceEmail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>address</td>
<td>

<a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationSetting">OrganisationSetting</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settingKey</td>
<td>

<a href="#/definitions/SettingKey">SettingKey</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connectionType</td>
<td>

<a href="#/definitions/ConnectionType">ConnectionType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationShortDto">OrganisationShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationShortGeoDto">OrganisationShortGeoDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>address</td>
<td>

<a href="#/definitions/OrganisationGeoDto">OrganisationGeoDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationStatus">OrganisationStatus</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationStatusDto">OrganisationStatusDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationType">OrganisationType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plural</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/OrganisationTypeDto">OrganisationTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plural</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Payment">Payment</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>creationDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


array[<a href="#/definitions/PaymentStatus">PaymentStatus</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>gatewayTransactionId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>requestId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>paymentGatewayCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>paymentMethod</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>grouping</td>
<td>

<a href="#/definitions/TransactionGroup">TransactionGroup</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currency</td>
<td>

<a href="#/definitions/CurrencyDetails">CurrencyDetails</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orders</td>
<td>

<a href="#/definitions/Orders">Orders</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>threeDSecure</td>
<td>

<a href="#/definitions/ThreeDSecure">ThreeDSecure</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastPaymentStatus</td>
<td>

<a href="#/definitions/PaymentStatus">PaymentStatus</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/PaymentDto">PaymentDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>creationDate</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastPaymentStatus</td>
<td>

<a href="#/definitions/PaymentStatusDto">PaymentStatusDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>gatewayTransactionId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>requestId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>requestedByUser</td>
<td>

<a href="#/definitions/DisplayUserDto">DisplayUserDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>requestedByOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currencyCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>paymentMethod</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>gateway</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>grouping</td>
<td>

<a href="#/definitions/TransactionGroupDto">TransactionGroupDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/PaymentStatus">PaymentStatus</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>when</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>message</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>current</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/PaymentStatusDto">PaymentStatusDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>status</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>when</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>message</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/PermissionDto">PermissionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>permission</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Point">Point</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>envelope</td>
<td>

<a href="#/definitions/Geometry">Geometry</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>factory</td>
<td>

<a href="#/definitions/GeometryFactory">GeometryFactory</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>userData</td>
<td>


object

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinates</td>
<td>


array[<a href="#/definitions/Coordinate">Coordinate</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>empty</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>simple</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dimension</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>numPoints</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>boundaryDimension</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>x</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>y</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinate</td>
<td>

<a href="#/definitions/Coordinate">Coordinate</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>boundary</td>
<td>

<a href="#/definitions/Geometry">Geometry</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>geometryType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>coordinateSequence</td>
<td>

<a href="#/definitions/CoordinateSequence">CoordinateSequence</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>valid</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>length</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>srid</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>numGeometries</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>precisionModel</td>
<td>

<a href="#/definitions/PrecisionModel">PrecisionModel</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>rectangle</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>area</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>envelopeInternal</td>
<td>

<a href="#/definitions/Envelope">Envelope</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/PrecisionModel">PrecisionModel</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>scale</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>floating</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/Type">Type</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maximumSignificantDigits</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>offsetX</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>offsetY</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Product">Product</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attributes</td>
<td>


array[<a href="#/definitions/ProductItemAttribute">ProductItemAttribute</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>optionSets</td>
<td>


array[<a href="#/definitions/ProductOptionSet">ProductOptionSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSet">ProductExtraSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/ProductTag">ProductTag</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>orderItems</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>customProduct</td>
<td>

<a href="#/definitions/ProductCustomItem">ProductCustomItem</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryProduct</td>
<td>

<a href="#/definitions/ProductLibraryItem">ProductLibraryItem</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>available</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>stockLevel</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>externalPlu</td>
<td>


array[<a href="#/definitions/ExternalPlu">ExternalPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Product Extra">Product Extra</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Product Tag">Product Tag</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tagType</td>
<td>

<a href="#/definitions/Product Tag Type">Product Tag Type</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>childTags</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Product Tag Type">Product Tag Type</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductAttribute">ProductAttribute</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>customAttribute</td>
<td>

<a href="#/definitions/ProductCustomAttribute">ProductCustomAttribute</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productLibraryAttribute</td>
<td>

<a href="#/definitions/ProductLibraryAttribute">ProductLibraryAttribute</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductAttributeDto">ProductAttributeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductCustomAttribute">ProductCustomAttribute</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductCustomExtra">ProductCustomExtra</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extra</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductCustomItem">ProductCustomItem</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductType">ProductType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupItems</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>images</td>
<td>


array[<a href="#/definitions/ProductCustomItemImage">ProductCustomItemImage</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>additionalInfo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductCustomItemImage">ProductCustomItemImage</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>thumbnail</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>default</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductCustomOption">ProductCustomOption</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>option</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductDiscount">ProductDiscount</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductDiscountDto">ProductDiscountDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>discountProvider</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>brand</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connection</td>
<td>

<a href="#/definitions/ConnectionShortDto">ConnectionShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productItem</td>
<td>

<a href="#/definitions/ProductShortDto">ProductShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductDto">ProductDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>available</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductTypeDto">ProductTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>discount</td>
<td>

<a href="#/definitions/ProductPriceDiscountDto">ProductPriceDiscountDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>stockLevel</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupItems</td>
<td>


array[<a href="#/definitions/ProductDto">ProductDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attributes</td>
<td>


array[<a href="#/definitions/ProductItemAttributeDisplayDto">ProductItemAttributeDisplayDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>optionSets</td>
<td>


array[<a href="#/definitions/ProductOptionSetDto">ProductOptionSetDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSetDto">ProductExtraSetDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/Product Tag">Product Tag</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>images</td>
<td>


array[<a href="#/definitions/ProductImageDto">ProductImageDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>globalProduct</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>additionalInfo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductExtra">ProductExtra</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSet">ProductExtraSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>customExtra</td>
<td>

<a href="#/definitions/ProductCustomExtra">ProductCustomExtra</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>externalPlu</td>
<td>


array[<a href="#/definitions/ExternalPlu">ExternalPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductExtraDisplayDto">ProductExtraDisplayDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductExtraSet">ProductExtraSet</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extras</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductExtraSetDto">ProductExtraSetDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extras</td>
<td>


array[<a href="#/definitions/Product Extra">Product Extra</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductImageDto">ProductImageDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>thumbnail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>default</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductItemAttribute">ProductItemAttribute</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attribute</td>
<td>

<a href="#/definitions/ProductAttribute">ProductAttribute</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductItemAttributeDisplayDto">ProductItemAttributeDisplayDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryAttribute">ProductLibraryAttribute</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryExtra">ProductLibraryExtra</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extras</td>
<td>


array[<a href="#/definitions/ProductExtra">ProductExtra</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryExtraPlus</td>
<td>


array[<a href="#/definitions/ProductLibraryExtraPlu">ProductLibraryExtraPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryExtraPlu">ProductLibraryExtraPlu</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>

<a href="#/definitions/DeliveryType">DeliveryType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryExtraSet">ProductLibraryExtraSet</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extras</td>
<td>


array[<a href="#/definitions/ProductLibraryExtra">ProductLibraryExtra</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryItem">ProductLibraryItem</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductType">ProductType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>brandOwner</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>extraSets</td>
<td>


array[<a href="#/definitions/ProductLibraryExtraSet">ProductLibraryExtraSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>optionSets</td>
<td>


array[<a href="#/definitions/ProductLibraryOptionSet">ProductLibraryOptionSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attributes</td>
<td>


array[<a href="#/definitions/ProductLibraryItemAttribute">ProductLibraryItemAttribute</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupItems</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>images</td>
<td>


array[<a href="#/definitions/ProductLibraryItemImage">ProductLibraryItemImage</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryItemPlus</td>
<td>


array[<a href="#/definitions/ProductLibraryItemPlu">ProductLibraryItemPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>additionalInfo</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryItemAttribute">ProductLibraryItemAttribute</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>attribute</td>
<td>

<a href="#/definitions/ProductLibraryAttribute">ProductLibraryAttribute</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryItemImage">ProductLibraryItemImage</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>thumbnail</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>default</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryItemPlu">ProductLibraryItemPlu</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>

<a href="#/definitions/DeliveryType">DeliveryType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryOption">ProductLibraryOption</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockOptionSets</td>
<td>


array[<a href="#/definitions/ProductLibraryOptionSet">ProductLibraryOptionSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockExtraSets</td>
<td>


array[<a href="#/definitions/ProductLibraryExtraSet">ProductLibraryExtraSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryOptionPlus</td>
<td>


array[<a href="#/definitions/ProductLibraryOptionPlu">ProductLibraryOptionPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryOptionPlu">ProductLibraryOptionPlu</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>plu</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryType</td>
<td>

<a href="#/definitions/DeliveryType">DeliveryType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductLibraryOptionSet">ProductLibraryOptionSet</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductOption">ProductOption</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>customOption</td>
<td>

<a href="#/definitions/ProductCustomOption">ProductCustomOption</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryOption</td>
<td>

<a href="#/definitions/ProductLibraryOption">ProductLibraryOption</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockOptionSets</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockExtraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSet">ProductExtraSet</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>externalPlu</td>
<td>


array[<a href="#/definitions/ExternalPlu">ExternalPlu</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductOptionDisplayDto">ProductOptionDisplayDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductOptionDto">ProductOptionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockOptionSets</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>unlockExtraSets</td>
<td>


array[<a href="#/definitions/ProductExtraSetDto">ProductExtraSetDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductOptionSet">ProductOptionSet</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[<a href="#/definitions/ProductOption">ProductOption</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductOptionSetDto">ProductOptionSetDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>displayName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>options</td>
<td>


array[<a href="#/definitions/ProductOptionDto">ProductOptionDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductPriceDiscountDto">ProductPriceDiscountDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>discountAmount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>discountPrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductSearchCriteriaDto">ProductSearchCriteriaDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/ProductTagShortDto">ProductTagShortDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>minPrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>maxPrice</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>available</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>order</td>
<td>


array[string]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisations</td>
<td>


array[integer]

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productIds</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductShortDto">ProductShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>price</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortGeoDto">OrganisationShortGeoDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>available</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sku</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>availableOnline</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productType</td>
<td>

<a href="#/definitions/ProductTypeDto">ProductTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupItems</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductTag">ProductTag</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>shortDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>childTags</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>products</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>libraryItems</td>
<td>


array[<a href="#/definitions/ProductLibraryItem">ProductLibraryItem</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>productTagType</td>
<td>

<a href="#/definitions/ProductTagType">ProductTagType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/Organisation">Organisation</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductTagShortDto">ProductTagShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tagType</td>
<td>

<a href="#/definitions/Product Tag Type">Product Tag Type</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductTagType">ProductTagType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductType">ProductType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProductTypeDto">ProductTypeDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProfileBase">ProfileBase</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>email</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>emailHash</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>idNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>firstName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>surname</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nickName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nonVerifiedEmail</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>phoneNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumberVerifyToken</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumberVerified</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>emailVerifyToken</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>emailVerified</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>fullName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ProfileBaseDto">ProfileBaseDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>firstName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>surname</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>email</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>nickName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>cellphoneNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/RestHookCreationDto">RestHookCreationDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>url</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>eventType</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>atOrganisationId</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/RoleDto">RoleDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SecurityGroup">SecurityGroup</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>standardGroup</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>founderGroup</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>newUsersGroup</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Setting">Setting</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>salt</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>encrypted</td>
<td>


boolean

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>user</td>
<td>

<a href="#/definitions/User">User</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connection</td>
<td>

<a href="#/definitions/Connection">Connection</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SettingDto">SettingDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>value</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>key</td>
<td>

<a href="#/definitions/SettingKeyShortDto">SettingKeyShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>startDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>endDate</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SettingKey">SettingKey</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>validationregex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>tags</td>
<td>


array[<a href="#/definitions/SettingTag">SettingTag</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>settings</td>
<td>


array[<a href="#/definitions/Setting">Setting</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>valueType</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>required</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>defaultValue</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longDescription</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SettingKeyShortDto">SettingKeyShortDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SettingTag">SettingTag</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>getkeys</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/StatusMessageDto">StatusMessageDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>message</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/SubscribeScheduleReportDto">SubscribeScheduleReportDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>schedule</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>email</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/ThreeDSecure">ThreeDSecure</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>form</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Transaction">Transaction</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>detailType</td>
<td>

<a href="#/definitions/DetailType">DetailType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactionType</td>
<td>

<a href="#/definitions/TransactionType">TransactionType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


number (double)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>notes</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>grouping</td>
<td>

<a href="#/definitions/TransactionGroup">TransactionGroup</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connection</td>
<td>

<a href="#/definitions/Connection">Connection</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryAgent</td>
<td>

<a href="#/definitions/DeliveryAgent">DeliveryAgent</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>order</td>
<td>

<a href="#/definitions/Orders">Orders</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amountInSent</td>
<td>


integer (int32)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/TransactionDisplayDto">TransactionDisplayDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sign</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>date</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactionOrganisation</td>
<td>

<a href="#/definitions/OrganisationShortDto">OrganisationShortDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactionUser</td>
<td>

<a href="#/definitions/UserDto">UserDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>deliveryAgent</td>
<td>

<a href="#/definitions/DeliveryAgentDto">DeliveryAgentDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>connection</td>
<td>

<a href="#/definitions/ConnectionDto">ConnectionDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/DetailTypeDto">DetailTypeDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>amount</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupingId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reversible</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>groupReversible</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/TransactionGroup">TransactionGroup</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>type</td>
<td>

<a href="#/definitions/GroupingType">GroupingType</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/TransactionGroupDto">TransactionGroupDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>reference</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>description</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>typeName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>typeCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/TransactionDisplayDto">TransactionDisplayDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/TransactionType">TransactionType</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>sign</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/Type">Type</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

</table>

## <a name="/definitions/TypeIndustryDto">TypeIndustryDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>types</td>
<td>


array[<a href="#/definitions/OrganisationTypeDto">OrganisationTypeDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>industries</td>
<td>


array[<a href="#/definitions/IndustryDto">IndustryDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/UpdateOrganisationDto">UpdateOrganisationDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>code</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>types</td>
<td>


array[integer]

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>timezoneOffset</td>
<td>


integer (int32)

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>registeredDirectly</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>industry</td>
<td>


array[integer]

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationProfile</td>
<td>

<a href="#/definitions/CreateOrganisationProfileDto">CreateOrganisationProfileDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>operatingHours</td>
<td>


array[<a href="#/definitions/CreateOrganisationOperatingHoursDto">CreateOrganisationOperatingHoursDto</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>currencyCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/User">User</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>verified</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>ussdId</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>activationHash</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>dateCreated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>expiration</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>external</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>federated</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastUpdated</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>realm</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>lastLogin</td>
<td>


string (date-time)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>resetPasswordToken</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>bankDetail</td>
<td>


array[<a href="#/definitions/BankDetail">BankDetail</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/ProfileBase">ProfileBase</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>transactions</td>
<td>


array[<a href="#/definitions/Transaction">Transaction</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>addresses</td>
<td>


array[<a href="#/definitions/UserGeo">UserGeo</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>globalAdministrator</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>organisationProfile</td>
<td>


array[<a href="#/definitions/OrganisationProfile">OrganisationProfile</a>]



</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>activeBankDetail</td>
<td>

<a href="#/definitions/BankDetail">BankDetail</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/UserDto">UserDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>password</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/ProfileBaseDto">ProfileBaseDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/UserGeo">UserGeo</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetName</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>complex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>suburb</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>city</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>postalCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>address</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/UserGeoDto">UserGeoDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>latitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>name</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetNumber</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>streetName</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>complex</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>suburb</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>city</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>postalCode</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>note</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>enabled</td>
<td>


boolean

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>longitude</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/UserProfileDto">UserProfileDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>id</td>
<td>


integer (int64)

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>username</td>
<td>


string

</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

<tr>
<td>profile</td>
<td>

<a href="#/definitions/ProfileBaseDto">ProfileBaseDto</a>


</td>
<td>optional</td>
<td>-</td>
<td></td>
</tr>

</table>

## <a name="/definitions/VersionDto">VersionDto</a>

<table border="1">
<tr>
<th>name</th>
<th>type</th>
<th>required</th>
<th>description</th>
<th>example</th>
</tr>

<tr>
<td>version</td>
<td>


string

</td>
<td>required</td>
<td>-</td>
<td></td>
</tr>

</table>


</xmp>

<script src="http://strapdownjs.com/v/0.2/strapdown.js"></script>
</html>