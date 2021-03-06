---

copyright:

  years: 2018


lastupdated: "2018-06-21"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# CLI commands for Managing API Keys and Policies
{: #ibmcloud_commands_iam}

<table summary="ibmcloud commands that you can use to manage API keys and policies.">
 <caption>Table 1. Commands for managing API keys and policies</caption>
  <thead>
  <th colspan="5">Commands for managing API keys and policies</th>
  </thead>
  <tbody>
  <tr>
   <td>[ibmcloud iam service-ids](ic_cli_api_policy.html#ibmcloud_iam_service_ids)</td>
   <td>[ibmcloud iam service-id](ic_cli_api_policy.html#ibmcloud_iam_service_id)</td>
   <td>[ibmcloud iam service-id-create](ic_cli_api_policy.html#ibmcloud_iam_service_id_create)</td>
   <td>[ibmcloud iam service-id-update](ic_cli_api_policy.html#ibmcloud_iam_service_id_update)</td>
   <td>[ibmcloud iam service-id-delete](ic_cli_api_policy.html#ibmcloud_iam_service_id_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam service-id-lock](ic_cli_api_policy.html#ibmcloud_iam_service_id_lock)</td>
   <td>[ibmcloud iam service-id-unlock](ic_cli_api_policy.html#ibmcloud_iam_service_id_unlock)</td>
   <td>[ibmcloud iam api-keys](ic_cli_api_policy.html#ibmcloud_iam_api_keys)</td>
   <td>[ibmcloud iam api-key-create](ic_cli_api_policy.html#ibmcloud_iam_api_key_create)</td>
   <td>[ibmcloud iam api-key-delete](ic_cli_api_policy.html#ibmcloud_iam_api_key_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam api-key-update](ic_cli_api_policy.html#ibmcloud_iam_api_key_update)</td>
   <td>[ibmcloud iam api-key-lock](ic_cli_api_policy.html#ibmcloud_iam_api_key_lock)</td>
   <td>[ibmcloud iam api-key-unlock](ic_cli_api_policy.html#ibmcloud_iam_api_key_unlock)</td>
   <td>[ibmcloud iam service-api-keys](ic_cli_api_policy.html#ibmcloud_iam_service_api_keys)</td>
   <td>[ibmcloud iam service-api-key](ic_cli_api_policy.html#ibmcloud_iam_service_api_key)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam service-api-key-create](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_create)</td>
   <td>[ibmcloud iam service-api-key-update](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_update)</td>
   <td>[ibmcloud iam service-api-key-delete](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_delete)</td>
   <td>[ibmcloud iam service-api-key-lock](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_lock)</td>
   <td>[ibmcloud iam service-api-key-unlock](ic_cli_api_policy.html#ibmcloud_iam_service_api_key_unlock)</td>
  </tr>
  <tr>
    <td>[ibmcloud iam service-policies](ic_cli_api_policy.html#ibmcloud_iam_service_policies)</td>
    <td>[ibmcloud iam service-policy](ic_cli_api_policy.html#ibmcloud_iam_service_policy)</td>
    <td>[ibmcloud iam service-policy-create](ic_cli_api_policy.html#ibmcloud_iam_service_policy_create)</td>
    <td>[ibmcloud iam service-policy-update](ic_cli_api_policy.html#ibmcloud_iam_service_policy_update)</td>
    <td>[ibmcloud iam service-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_service_policy_delete)</td>
  </tr>
  <tr>
   <td>[ibmcloud iam user-policies](ic_cli_api_policy.html#ibmcloud_iam_user_policies)</td>
   <td>[ibmcloud iam user-policy](ic_cli_api_policy.html#ibmcloud_iam_user_policy)</td>
   <td>[ibmcloud iam user-policy-create](ic_cli_api_policy.html#ibmcloud_iam_user_policy_create)</td>
   <td>[ibmcloud iam user-policy-update](ic_cli_api_policy.html#ibmcloud_iam_user_policy_update)</td>
   <td>[ibmcloud iam user-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_user_policy_delete)</td>
  </tr>
  <tr>
     <td>[ibmcloud iam oauth-tokens](ic_cli_api_policy.html#ibmcloud_iam_oauth_tokens)</td>
     <td>[ibmcloud iam dedicated-id-disconnect](ic_cli_api_policy.html#ibmcloud_iam_dedicated_id_disconnect)</td>
     <td>[ibmcloud iam authorization-policy-create](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy_create)</td>
     <td>[ibmcloud iam authorization-policy-delete](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy_delete)</td>
     <td>[ibmcloud iam authorization-policy](ic_cli_api_policy.html#ibmcloud_iam_authorization_policy)</td>
  </tr>
  <tr>
     <td>[ibmcloud iam authorization-policies](ic_cli_api_policy.html#ibmcloud_iam_authorization_policies)</td>
  </tr>
  </tbody>
  </table>
  
  ### ibmcloud iam service-ids
{: #ibmcloud_iam_service_ids}

List all service IDs

```
ibmcloud iam service-ids [--uuid]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>--uuid</dt>
  <dd>Show UUID of service IDs only</dd>
</dl>

<strong>Examples</strong>:
List UUID of all service IDs under current account

```
ibmcloud iam service-ids --uuid
```

### ibmcloud iam service-id
{: #ibmcloud_iam_service_id}

Display details of a service ID

```
ibmcloud iam service-id (NAME|UUID) [--uuid]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>--uuid</dt>
  <dd>Display the UUID of the service ID</dd>
</dl>

<strong>Examples</strong>:

Show details of service ID `sample-test`

```
ibmcloud iam service-id sample-test
```
Show details of service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-create
{: #ibmcloud_iam_service_id_create}

Create a service ID

```
ibmcloud iam service-id-create NAME [-d, --description DESCRIPTION] [--lock]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service</dd>
  <dt>-d, --description</dt>
  <dd>Description of the service ID</dd>
  <dt>--lock</dt>
  <dd>Lock the service ID when being created</dd>
</dl>

<strong>Examples</strong>:

Create a service ID with service name `sample-test` and description `hello, world!`

```
ibmcloud iam service-id-create sample-test -d 'hello, world!'
```

Create a locked service ID with service name `sample-test` and description `hello, world!`

```
ibmcloud iam service-id-create sample-test -d 'hello, world!' --lock
```

### ibmcloud iam service-id-update

{: #ibmcloud_iam_service_id_update}
Update a service ID

```
ibmcloud iam service-id-update (NAME|UUID) [-n, --name NEW_NAME] [-d, --description DESCRIPTION] [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-n, --name</dt>
  <dd>New name of the service</dd>
  <dt>-d, --description</dt>
  <dd>New description of the service</dd>
  <dt>-f, --force</dt>
  <dd>Update without confirmation</dd>
</dl>

<strong>Examples</strong>:

Rename service ID `sample-test` to `sample-test-2` without confirmation

```
ibmcloud iam service-id-update sample-test -n sample-test-2 -f
```

Update description of service `sample-test`

```
ibmcloud iam service-id-update sample-test -d 'hello, friend!'
```

Rename service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` to `sample-test-3` with new description

```
ibmcloud iam service-id-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 -n sample-test-3 -d 'hello, my friends!'
```

### ibmcloud iam service-id-delete
{: #ibmcloud_iam_service_id_delete}

Delete a service ID

```
ibmcloud iam service-id-delete (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-f, --force</dt>
  <dd>Delete without confirmation</dd>
</dl>

<strong>Examples</strong>:

Delete service ID `sample-teset` without confirmation

```
ibmcloud iam service-id-delete sample-teset -f
```

Delete service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-lock
{: #ibmcloud_iam_service_id_lock}

Lock a service ID

```
ibmcloud iam service-id-lock (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-f, --force</dt>
  <dd>Lock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Lock service ID `sample-teset` without confirmation

```
ibmcloud iam service-id-lock sample-teset -f
```

Lock service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id-lock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-id-unlock
{: #ibmcloud_iam_service_id_unlock}

Unlock a service ID

```
ibmcloud iam service-id-unlock (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-f, --force</dt>
  <dd>Unlock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Unlock service ID `sample-teset` without confirmation

```
ibmcloud iam service-id-unlock sample-teset -f
```

Unlock service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id-unlock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam api-keys
{: #ibmcloud_iam_api_keys}

List all {{site.data.keyword.Bluemix_notm}} platform API keys

```
ibmcloud iam api-keys
```

<strong>Prerequisites</strong>:  Endpoint, Login

### ibmcloud iam api-key-create
{: #ibmcloud_iam_api_key_create}

Create a new {{site.data.keyword.Bluemix_notm}} platform API key

```
ibmcloud iam api-key-create NAME [-d DESCRIPTION] [--file FILE] [--lock]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>NAME (required)</dt>
<dd>Name of the API key to be created.</dd>
<dt>-d <i>DESCRIPTION</i> (optional)</dt>
<dd>Description of the API key</dd>
<dt>--file <i>FILE</i></dt>
<dd>Save API key information to specified file. If not set, the JSON content will be displayed.</dd>
<dt>--lock</dt>
<dd>Lock the API key when being created</dd>
</dl>

<strong>Examples</strong>:

Create an API key and save to a file

```
ibmcloud iam api-key-create MyKey -d "this is my API key" --file key_file
```

Create a locked API key with name "test-key"

```
ibmcloud iam api-key-create test-key --lock
```

### ibmcloud iam api-key-update
{: #ibmcloud_iam_api_key_update}

Update a {{site.data.keyword.Bluemix_notm}} platform API key

```
ibmcloud iam api-key-update (NAME|UUID) [-n name] [-d description]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>NAME (required)</dt>
<dd>The old name of the API key to be updated, exclusive with UUID</dd>
<dt>UUID (required)</dt>
<dd>The UUID of the API key to be updated, exclusive with NAME</dd>
<dt>-n <i>NAME</i> (optional)</dt>
<dd>The new name of the API key</dd>
<dt>-d <i>DESCRIPTION</i> (optional)</dt>
<dd>The new description of the API key</dd>
</dl>

<strong>Examples</strong>:

Update the description of an API key:

```
ibmcloud iam api-key-update MyKey -d "the new description of my key"
```

### ibmcloud api-key-delete
{: #ibmcloud_iam_api_key_delete}

Delete a {{site.data.keyword.Bluemix_notm}} platform API key

```
ibmcloud iam api-key-delete (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>NAME (required)</dt>
<dd>Name of the API key to be deleted, exclusive with UUID</dd>
<dt>UUID (required)</dt>
<dd>UUID of the API key to be deleted, exclusive with NAME</dd>
<dt>-f, --force</dt>
<dd>Force deletion without confirmation.</dd>
</dl>

### ibmcloud api-key-lock
{: #ibmcloud_iam_api_key_lock}

Lock a platform API key

```
ibmcloud iam api-key-lock (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>NAME (required)</dt>
<dd>Name of the API key to be locked, exclusive with UUID</dd>
<dt>UUID (required)</dt>
<dd>UUID of the API key to be locked, exclusive with NAME</dd>
<dt>-f, --force</dt>
<dd>Force lock without confirmation.</dd>
</dl>

<strong>Examples</strong>:

Lock API key test-api-key

```
ibmcloud iam api-key-lock test-api-key
```

Lock API key with given UUID without confirmation

```
ibmcloud iam api-key-lock ApiKey-18f773b0-db53-43f1-ad68-92c667c218fe --force
```

### ibmcloud api-key-unlock
{: #ibmcloud_iam_api_key_unlock}

Unlock a platform API key

```
ibmcloud iam api-key-unlock (NAME|UUID) [-f, --force]
```

<strong>Prerequisites</strong>:  Endpoint, Login

<strong>Command options</strong>:
<dl>
<dt>NAME (required)</dt>
<dd>Name of the API key to be unlocked, exclusive with UUID</dd>
<dt>UUID (required)</dt>
<dd>UUID of the API key to be unlocked, exclusive with NAME</dd>
<dt>-f, --force</dt>
<dd>Force unlock without confirmation.</dd>
</dl>

<strong>Examples</strong>:

Unlock API key test-api-key

```
ibmcloud iam api-key-unlock test-api-key
```

Unlock API key with given UUID without confirmation

```
ibmcloud iam api-key-unlock ApiKey-18f773b0-db53-43f1-ad68-92c667c218fe --force
```

### ibmcloud iam service-api-keys
{: #ibmcloud_iam_service_api_keys}

List all API keys of a service

```
ibmcloud iam service-api-keys (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Display service API keys without confirmation</dd>
</dl>

<strong>Examples</strong>:

List all API keys of service `sample-service` :

```
ibmcloud iam service-api-keys sample-service
```

### ibmcloud iam service-api-key
{: #ibmcloud_iam_service_api_key}

List details of a service API key

```
ibmcloud iam service-api-key (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [--uuid] [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>--uuid</dt>
  <dd>Display the UUID of service API key</dd>
  <dt>-f, --force</dt>
  <dd>Display service API key without confirmation</dd>
</dl>

<strong>Examples</strong>:

Show details of service API key `sample-key` of service `sample-service` :

```
ibmcloud iam service-api-key sample-key sample-service
```

### ibmcloud iam service-api-key-create
{: #ibmcloud_iam_service_api_key_create}

Create a service API key

```
ibmcloud iam service-api-key-create NAME (SERVICE_ID_NAME|SERVICE_ID_UUID) [-d, --description DESCRIPTION] [--file FILE] [-f, --force] [--lock]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service ID or newly created service API key</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-d, --description</dt>
  <dd>Description of the API key</dd>
  <dt>--file</dt>
  <dd>Save API key information to specified file. If not set, the JSON content will be displayed.</dd>
  <dt>-f, --force</dt>
  <dd>Force creation without confirmation</dd>
</dl>

<strong>Examples</strong>:

Create a service API key `sample-key` for service `sample-service` without confirmation:

```
ibmcloud iam service-api-key-create sample-key sample-service -f
```

### ibmcloud iam service-api-key-update
{: #ibmcloud_iam_service_api_key_update}

Update a service API key

```
ibmcloud iam service-api-key-update (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID)  [-n, --name NEW_NAME] [-d, --description DESCRIPTION] [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-n, --name</dt>
  <dd>New name of the service API key</dd>
  <dt>-d, --description</dt>
  <dd>New description of the service API key</dd>
  <dt>-f, --force</dt>
  <dd>Update without confirmation</dd>
</dl>

<strong>Examples</strong>:

Rename service API key `sample-key` to `new-sample-key` :

```
ibmcloud iam service-api-key-update sample-key sample-service -n new-sample-key
```

### ibmcloud iam service-api-key-delete
{: #ibmcloud_iam_service_api_key_delete}

Delete a service API key

```
ibmcloud iam service-api-key-delete (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Delete without confirmation</dd>
</dl>

<strong>Examples</strong>:

Delete service API key `sample-key` of service ID `sample-service`:

```
ibmcloud iam service-api-key-delete sample-key sample-service
```

### ibmcloud iam service-api-key-lock
{: #ibmcloud_iam_service_api_key_lock}

Lock a service API key

```
ibmcloud iam service-api-key-lock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Lock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Lock service API key `sample-key` of service ID `sample-service`:

```
ibmcloud iam service-api-key-lock sample-key sample-service
```

### ibmcloud iam service-api-key-unlock
{: #ibmcloud_iam_service_api_key_unlock}

Unlock a service API key

```
ibmcloud iam service-api-key-unlock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Unlock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Unlock service API key `sample-key` of service ID `sample-service`:

```
ibmcloud iam service-api-key-unlock sample-key sample-service
```

### ibmcloud iam user-policies
{: #ibmcloud_iam_user_policies}

List policies of user `name@example.com`:

```
ibmcloud iam user-policies name@example.com
```

<strong>Prerequisites</strong>:  Endpoint, Login, Account Targeted

<strong>Command options</strong>:
<dl>
<dt>USER_NAME (required)</dt>
<dd>User name to whom the policies belong</dd>
</dl>

<strong>Examples</strong>:

List policies of user `name@example.com`:

```
ibmcloud iam user-policies name@example.com
```

### ibmcloud iam user-policy
{: #ibmcloud_iam_user_policy}

Display details of a user policy

```
ibmcloud iam user-policy USER_NAME POLICY_ID
```

<strong>Prerequisites</strong>:  Endpoint, Login, Account Targeted

<strong>Command options</strong>:
<dl>
<dt>USER_NAME (required)</dt>
<dd>User name to whom the policy belongs</dd>
<dt>POLICY_ID (required)</dt>
<dd>ID of the policy</dd>
</dl>

<strong>Examples</strong>:

List policy `0bb730daa` of user `name@example.com`:

```
ibmcloud iam user-policy name@example.com 0bb730daa
```

### ibmcloud iam user-policy-create
{: #ibmcloud_iam_user_policy_create}

Create a user policy

```
ibmcloud iam user-policy-create USER_NAME {--file JSON_FILE | --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>Prerequisites</strong>:  Endpoint, Login, Account Targeted

<strong>Command options</strong>:
<dl>
<dt>USER_NAME (required)</dt>
<dd>User name to whom the policy belongs to</dd>
<dt>--file <i>FILE</i> (optional)</dt>
<dd>JSON file of policy definition</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (optional)</dt>
<dd>Role names of the policy definition. For supported roles of a specific service, run 'ibmcloud iam roles --service SERVICE_NAME'. This option is exclusive with '--file'.</dd>
<dt>--service-name <i>SERVICE_NAME</i> (optional)</dt>
<dd>Service name of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE_GUID</i> (optional)</dt>
<dd>GUID of service instance of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--region <i>REGION</i> (optional)</dt>
<dd>Region of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (optional)</dt>
<dd>Resource type of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource <i>RESOURCE</i> (optional)</dt>
<dd>Resource of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (optional)</dt>
<dd>Name of the resource group, This is exclusive with '--file', '--resource' and '--resource-group-id' flags.</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (optional)</dt>
<dd>ID of the resource group, This is exclusive with '--file', '--resource' and '--resource-group-name' flags.</dd>
</dl>

<strong>Examples</strong>:

Create user policy for user `name@example.com` from policy JSON file `policy.json`:

```
ibmcloud iam user-policy-create name@example.com --file @policy.json
```

Give `name@example.com` `Administrator` role for all `sample-service` resources:

```
ibmcloud iam user-policy-create name@example.com --roles Administrator --service-name sample-service
```

Give `name@example.com` `Editor` role for resource `key123` of sample service instance with GUID `d161aeea-fd02-40f8-a487-df1998bd69a9` in `us-south` region:

```
ibmcloud iam user-policy-create name@example.com --roles Editor --service-name sample-service --service-instance d161aeea-fd02-40f8-a487-df1998bd69a9 --region us-south --resource-type key --resource key123
```

Give `name@example.com` `Operator` role for resource group with ID `dda27e49d2a1efca58083a01dfde18f6`:

```
ibmcloud iam user-policy-create name@example.com --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

Give `name@example.com` `Viewer` role for the members of resource group `sample-resource-group`:

```
ibmcloud iam user-policy-create name@example.com --roles Viewer --resource-group-name sample-resource-group
```

Give `name@example.com` `Viewer` role for the members of resource group with ID `dda27e49d2a1efca58083a01dfde18f6`:

```
ibmcloud iam user-policy-create name@example.com --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

### ibmcloud iam user-policy-update
{: #ibmcloud_iam_user_policy_update}

Update a user policy

```
ibmcloud iam user-policy-update USER_NAME POLICY_ID {--file JSON_FILE | [--roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>Prerequisites</strong>:  Endpoint, Login, Account Targeted

<strong>Command options</strong>:
<dt>USER_NAME (required)</dt>
<dd>User name to whom the policy belongs to</dd>
<dt>POLICY_ID (required)</dt>
<dd>ID of the policy to update</dd>
<dt>--file <i>FILE</i> (optional)</dt>
<dd>JSON file of policy definition</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (optional)</dt>
<dd>Role names of the policy definition. For supported roles of a specific service, run 'ibmcloud iam roles --service SERVICE_NAME'. This option is exclusive with '--file'.</dd>
<dt>--service-name <i>SERVICE_NAME</i> (optional)</dt>
<dd>Service name of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE_GUID</i> (optional)</dt>
<dd>GUID of service instance of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--region <i>REGION</i> (optional)</dt>
<dd>Region of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (optional)</dt>
<dd>Resource type of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource <i>RESOURCE</i> (optional)</dt>
<dd>Resource of the policy definition, This is exclusive with '--file' flag.</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (optional)</dt>
<dd>Name of the resource group, This is exclusive with '--file', '--resource' and '--resource-group-id' flags.</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (optional)</dt>
<dd>ID of the resource group, This is exclusive with '--file', '--resource' and '--resource-group-name' flags.</dd>
</dl>

<strong>Examples</strong>:

Update user policy with the one in JSON file：

```
ibmcloud iam user-policy-update name@example.com 0bb730daa --file @policy.json
```

Update user policy to give `name@example.com` `Administrator` role for all `sample-service` resources：

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Administrator --service-name sample-service
```

 Update user policy to give `name@example.com` `Editor` role for resource `key123` of sample service instance with GUID `d161aeea-fd02-40f8-a487-df1998bd69a9` in `us-south` region:

```
ibmcloud iam user-policy-update name@example.com --roles Editor --service-name sample-service --service-instance d161aeea-fd02-40f8-a487-df1998bd69a9 --region us-south --resource-type key --resource key123
```

Update user policy to give `name@example.com` `Operator` role for resource group with ID `dda27e49d2a1efca58083a01dfde18f6`:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

Update user policy to give `name@example.com` `Viewer` role for members of resource group `sample-resource-group`:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-name sample-resource-group
```

Update user policy to give `name@example.com` `Viewer` role for members of resource group with ID `dda27e49d2a1efca58083a01dfde18f6`:

```
ibmcloud iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

### ibmcloud iam user-policy-delete
{: #ibmcloud_iam_user_policy_delete}

Delete a user policy

```
ibmcloud iam user-policy-delete USER_ID POLICY_ID [-f, --force]
```

<strong>Prerequisites</strong>:  Endpoint, Login, Account Targeted

<strong>Command Options</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>Delete user policy without confirmation</dd>
</dl>

<strong>Examples</strong>:
Delete policies `user-policy-id` of user `name@example.com`:

```
ibmcloud iam user-policy-delete name@example.com user-policy-id
```

Delete policies `user-policy-id` of user `name@example.com` without confirmation:

```
ibmcloud iam user-policy-delete name@example.com user-policy-id -f
```

### ibmcloud iam service-policies
{: #ibmcloud_iam_service_policies}

List all service policies of specified service

```
ibmcloud iam service-policies SERVICE_ID [--json] [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID (required)</dt>
  <dd>Name or UUID of service ID</dd>
  <dt>-json</dt>
  <dd>Display policy in JSON format</dd>
  <dt>-f, --force</dt>
  <dd>Display service policies without confirmation</dd>
</dl>

<strong>Examples</strong>:

List policies of service `test`:

```
ibmcloud iam service-policies test
```
List policies of service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`:

```
ibmcloud iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### ibmcloud iam service-policy
{: #ibmcloud_iam_service_policy}

Display details of a service policy

```
ibmcloud iam service-policy SERVICE_ID POLICY_ID [--json] [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID (required)</dt>
  <dd>Name or UUID of service ID</dd>
  <dt>POLICY_ID (required)</dt>
  <dd>ID of the service policy<dd>
  <dt>-json</dt>
  <dd>Display policy in JSON format</dd>
  <dt>-f, --force</dt>
  <dd>Display service policy without confirmation</dd>
</dl>

<strong>Examples</strong>:

Show policy `140798e2-8ea7db3` of service `test`:

```
ibmcloud iam service-policies test 140798e2-8ea7db3
```
Show policy `140798e2-8ea7db3` of service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`:

```
ibmcloud iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```

### ibmcloud iam service-policy-create
{: #ibmcloud_iam_service_policy_create}

Create a service policy

```
ibmcloud iam service-policy-create SERVICE_ID {--file JSON_FILE | -r, --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID (required)</dt>
  <dd>Name or UUID of service ID</dd>
  <dt>--file</dt>
  <dd>JSON file of policy definition. This is exclusive with '-r, --roles', '--service-name', '--service-instance', '--region', '--resource-type', '--resource', '--resource-group-name' and '--resource-group-id' flags.</dd>
  <dt>-r, --roles</dt>
  <dd>Role names of the policy definition. For supported roles of a specific service, run 'ibmcloud iam roles --service SERVICE_NAME'. This option is exclusive with '--file'.</dd>
  <dt>--service-name</dt>
  <dd>Service name of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>--service-instance <i>SERVICE_INSTANCE_GUID</i></dt>
  <dd>GUID of service instance of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>-region</dt>
  <dd>Region of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>--resource-type</dt>
  <dd>Resource type of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>--resource</dt>
  <dd>Resource of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>--resource-group-name</dt>
  <dd>Name of the resource group. This option is exclusive with '--file' and '--resource-group-id'.</dd>
  <dt>--resource-group-id </dt>
  <dd>ID of the resource group. This option is exclusive with '--file' and '--resource-group-name'.</dd>
  <dt>-f, --force</dt>
  <dd>Create service policy without confirmation</dd>
</dl>

<strong>Examples</strong>:

Create service policy from JSON file for service `test`:

```
ibmcloud iam service-policy-create test --file @policy.json
```
Create service policy from JSON file for service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`:

```
ibmcloud iam service-policy-create ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 --file @policy.json
```

### ibmcloud iam service-policy-update
{: #ibmcloud_iam_service_policy_update}

Update a service policy

```
ibmcloud iam service-policy-update SERVICE_ID POLICY_ID {--file JSON_FILE | [-r, --roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE_GUID] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID (required)</dt>
  <dd>Name or UUID of service ID</dd>
  <dt>POLICY_ID (required)</dt>
  <dd>ID of the service policy<dd>
  <dt>--file</dt>
  <dd>JSON file of policy definition. This is exclusive with '-r, --roles', '--service-name', '--service-instance', '--region', '--resource-type', '--resource', 'resource-group-name' and 'resource-group-id' flags.</dd>
  <dt>-r, --roles</dt>
  <dd>Role names of the policy definition. For supported roles of a specific service, run 'ibmcloud iam roles --service SERVICE_NAME'. This option is exclusive with '--file'.</dd>
  <dt>-service-name</dt>
  <dd>Service name of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>-service-instance <i>SERVICE_INSTANCE_GUID</i></dt>
  <dd>GUID of service instance of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>-region</dt>
  <dd>Region of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>-resource-type</dt>
  <dd>Resource type of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>-resource</dt>
  <dd>Resource of the policy definition. This is exclusive with '--file' flag.</dd>
  <dt>--resource-group-name</dt>
  <dd>Name of the resource group. This option is exclusive with '--file' and '--resource-group-id'.</dd>
  <dt>--resource-group-id </dt>
  <dd>ID of the resource group. This option is exclusive with '--file' and '--resource-group-name'.</dd>
  <dt>-f, --force</dt>
  <dd>Update service policy without confirmation</dd>
</dl>

<strong>Examples</strong>:

Update service policy `140798e2-8ea7db3` from JSON file for service `test`:

```
ibmcloud iam service-policy-update test 140798e2-8ea7db3 --file @policy.json
```
Update service policy `140798e2-8ea7db3` from JSON file for service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`:

```
ibmcloud iam service-policy-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3 --file @policy.json
```

### ibmcloud iam service-policy-delete
{: #ibmcloud_iam_service_policy_delete}

Delete a service policy

```
ibmcloud iam service-policy-delete SERVICE_ID POLICY_ID [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SERVICE_ID (required)</dt>
  <dd>Name or UUID of service ID</dd>
  <dt>POLICY_ID (required)</dt>
  <dd>ID of the service policy<dd>
  <dt>-f, --force</dt>
  <dd>Delete without confirmation</dd>
</dl>

<strong>Examples</strong>:

Delete policy `140798e2-8ea7db3` of service `test`

```
ibmcloud iam service-policy-delete test 140798e2-8ea7db3
```
Delete policy `140798e2-8ea7db3` of service `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-policy-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```

### ibmcloud iam oauth-tokens
{: #ibmcloud_iam_oauth_tokens}

Retrieve and display the OAuth tokens for the current session

```
ibmcloud iam oauth-tokens
```

<strong>Prerequisites</strong>: Login, Target

<strong>Command Options</strong>:
<dl>
</dl>

<strong>Examples</strong>:

Refresh and display OAuth tokens

```
ibmcloud iam oauth-tokens
```

### ibmcloud iam dedicated-id-disconnect
{: #ibmcloud_iam_dedicated_id_disconnect}

Disconnect the public IBMid with dedicated non-IBMid

```
ibmcloud iam dedicated-id-disconnect [-f, --force]
```

<strong>Prerequisites</strong>: Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>Force disconnect without confirmation</dd>
</dl>

### ibmcloud iam authorization-policy-create
{: #ibmcloud_iam_authorization_policy_create}

Create an authorization policy to allow a service instance access to another service instance.

```
ibmcloud iam authorization-policy-create SOURCE_SERVICE_NAME TARGET_SERVICE_NAME ROLE_NAME1,ROLE_NAME2... [—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME] [—-target-service-instance TARGET_SERVICE_INSTANCE_NAME]
```

<strong>Prerequisites</strong>: Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>SOURCE_SERVICE_NAME</dt>
  <dd>Source service that can be authorized to access.</dd>
  <dt>TARGET_SERVICE_NAME</dt>
  <dd>Target service that the source service can be authorized to access.</dd>
  <dt>ROLE_NAME1,ROLE_NAME2...</dt>
  <dd>The roles that provide access for the source service.</dd>  
  <dt>—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME</dt>
  <dd>Source service instance name, if not specified, all instances of the source service will be authorized to access.</dd>
  <dt>—-target-service-instance TARGET_SERVICE_INSTANCE_NAME</dt>
  <dd>Target service instance name, if not specified, all instances of the target service will be authorized to access.</dd>
</dl>

### ibmcloud iam authorization-policy-delete
{: #ibmcloud_iam_authorization_policy_delete}

Delete an authorization policy.

```
ibmcloud iam authorization-policy-delete AUTHORIZATION_POLICY_ID [-f, --force]
```

<strong>Prerequisites</strong>: Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>ID of authorization policy to be deleted.</dd>
  <dt>-f, --force</dt>
  <dd>Force delete without confirmation.</dd>
</dl>

### ibmcloud iam authorization-policy
{: #ibmcloud_iam_authorization_policy}

Show details of an authorization policy.

```
ibmcloud iam authorization-policy AUTHORIZATION_POLICY_ID
```

<strong>Prerequisites</strong>: Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>ID of authorization policy to show.</dd>
</dl>

### ibmcloud iam authorization-policies
{: #ibmcloud_iam_authorization_policies}

List authorization policies under the current account.

```
ibmcloud iam authorization-policies
```

<strong>Prerequisites</strong>: Login, Target
