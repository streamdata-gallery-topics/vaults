---
swagger: "2.0"
x-collection-name: Azure Key Vault
x-complete: 0
info:
  title: Azure Key Vault API Vaults List
  description: The List operation gets information about the vaults associated with
    the subscription.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.KeyVault/vaults/{vaultName}:
    put:
      summary: Vaults Create Or Update
      description: Create or update a key vault in the specified subscription.
      operationId: Vaults_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-keyvaultvaultsvaultname-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters to create or update the vault
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the Resource Group to which the server belongs
      - in: path
        name: vaultName
        description: Name of the vault
      responses:
        200:
          description: OK
      tags:
      - Vaults
    delete:
      summary: Vaults Delete
      description: Deletes the specified Azure key vault.
      operationId: Vaults_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-keyvaultvaultsvaultname-delete
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the Resource Group to which the vault belongs
      - in: path
        name: vaultName
        description: The name of the vault to delete
      responses:
        200:
          description: OK
      tags:
      - Vaults
    get:
      summary: Vaults Get
      description: Gets the specified Azure key vault.
      operationId: Vaults_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-keyvaultvaultsvaultname-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the Resource Group to which the vault belongs
      - in: path
        name: vaultName
        description: The name of the vault
      responses:
        200:
          description: OK
      tags:
      - Vaults
  /subscriptions/{subscriptionId}/resources:
    get:
      summary: Vaults List
      description: The List operation gets information about the vaults associated
        with the subscription.
      operationId: Vaults_List
      x-api-path-slug: subscriptionssubscriptionidresources-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: query
        name: $top
        description: Maximum number of results to return
      - in: query
        name: api-version
        description: Azure Resource Manager Api Version
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Vaults
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---