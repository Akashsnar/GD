# v2_api

V2Api - JavaScript client for v2_api
OpenAPI spec for Solr's v2 API endpoints
This SDK is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 9.6.0
- Package version: 9.6.0
- Build package: org.openapitools.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/), please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install v2_api --save
```

Finally, you need to build the module:

```shell
npm run build
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

To use the link you just defined in your project, switch to the directory you want to use your v2_api from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

Finally, you need to build the module:

```shell
npm run build
```

#### git

If the library is hosted at a git repository, e.g.https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var V2Api = require('v2_api');


var api = new V2Api.AliasPropertiesApi()
var aliasName = "aliasName_example"; // {String} Alias Name
var propName = "propName_example"; // {String} Property Name
var updateAliasPropertyRequestBody = new V2Api.UpdateAliasPropertyRequestBody(); // {UpdateAliasPropertyRequestBody} Property value that needs to be updated
var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
api.createOrUpdateAliasProperty(aliasName, propName, updateAliasPropertyRequestBody, callback);

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*V2Api.AliasPropertiesApi* | [**createOrUpdateAliasProperty**](docs/AliasPropertiesApi.md#createOrUpdateAliasProperty) | **PUT** /aliases/{aliasName}/properties/{propName} | Update a specific property for a collection alias.
*V2Api.AliasPropertiesApi* | [**deleteAliasProperty**](docs/AliasPropertiesApi.md#deleteAliasProperty) | **DELETE** /aliases/{aliasName}/properties/{propName} | Delete a specific property for a collection alias.
*V2Api.AliasPropertiesApi* | [**getAliasProperty**](docs/AliasPropertiesApi.md#getAliasProperty) | **GET** /aliases/{aliasName}/properties/{propName} | Get a specific property for a collection alias.
*V2Api.AliasPropertiesApi* | [**getAllAliasProperties**](docs/AliasPropertiesApi.md#getAllAliasProperties) | **GET** /aliases/{aliasName}/properties | Get properties for a collection alias.
*V2Api.AliasPropertiesApi* | [**updateAliasProperties**](docs/AliasPropertiesApi.md#updateAliasProperties) | **PUT** /aliases/{aliasName}/properties | Update properties for a collection alias.
*V2Api.AliasesApi* | [**deleteAlias**](docs/AliasesApi.md#deleteAlias) | **DELETE** /aliases/{aliasName} | Deletes an alias by its name
*V2Api.AliasesApi* | [**getAliasByName**](docs/AliasesApi.md#getAliasByName) | **GET** /aliases/{aliasName} | Get details for a specific collection alias.
*V2Api.AliasesApi* | [**getAliases**](docs/AliasesApi.md#getAliases) | **GET** /aliases | List the existing collection aliases.
*V2Api.ClusterApi* | [**balanceReplicas**](docs/ClusterApi.md#balanceReplicas) | **POST** /cluster/replicas/balance | Balance Replicas across the given set of Nodes.
*V2Api.ClusterApi* | [**migrateReplicas**](docs/ClusterApi.md#migrateReplicas) | **POST** /cluster/replicas/migrate | Migrate Replicas from a given set of nodes.
*V2Api.CollectionBackupsApi* | [**createCollectionBackup**](docs/CollectionBackupsApi.md#createCollectionBackup) | **POST** /collections/{collectionName}/backups/{backupName}/versions | Creates a new backup point for a collection
*V2Api.CollectionBackupsApi* | [**deleteMultipleBackupsByRecency**](docs/CollectionBackupsApi.md#deleteMultipleBackupsByRecency) | **DELETE** /backups/{backupName}/versions | Delete all incremental backup points older than the most recent N
*V2Api.CollectionBackupsApi* | [**deleteSingleBackupById**](docs/CollectionBackupsApi.md#deleteSingleBackupById) | **DELETE** /backups/{backupName}/versions/{backupId} | Delete incremental backup point by ID
*V2Api.CollectionBackupsApi* | [**garbageCollectUnusedBackupFiles**](docs/CollectionBackupsApi.md#garbageCollectUnusedBackupFiles) | **PUT** /backups/{backupName}/purgeUnused | Garbage collect orphaned incremental backup files
*V2Api.CollectionBackupsApi* | [**listBackupsAtLocation**](docs/CollectionBackupsApi.md#listBackupsAtLocation) | **GET** /backups/{backupName}/versions | List existing incremental backups at the specified location.
*V2Api.CollectionPropertiesApi* | [**createOrUpdateCollectionProperty**](docs/CollectionPropertiesApi.md#createOrUpdateCollectionProperty) | **PUT** /collections/{collName}/properties/{propName} | Create or update a collection property
*V2Api.CollectionPropertiesApi* | [**deleteCollectionProperty**](docs/CollectionPropertiesApi.md#deleteCollectionProperty) | **DELETE** /collections/{collName}/properties/{propName} | Delete the specified collection property from the collection
*V2Api.CollectionSnapshotsApi* | [**createCollectionSnapshot**](docs/CollectionSnapshotsApi.md#createCollectionSnapshot) | **POST** /collections/{collName}/snapshots/{snapshotName} | Creates a new snapshot of the specified collection.
*V2Api.CollectionSnapshotsApi* | [**deleteCollectionSnapshot**](docs/CollectionSnapshotsApi.md#deleteCollectionSnapshot) | **DELETE** /collections/{collName}/snapshots/{snapshotName} | Delete an existing collection-snapshot by name.
*V2Api.CollectionsApi* | [**balanceShardUnique**](docs/CollectionsApi.md#balanceShardUnique) | **POST** /collections/{collectionName}/balance-shard-unique | Ensure a specified per-shard property is distributed evenly amongst physical nodes comprising a collection
*V2Api.CollectionsApi* | [**createCollection**](docs/CollectionsApi.md#createCollection) | **POST** /collections | Creates a new SolrCloud collection.
*V2Api.CollectionsApi* | [**deleteCollection**](docs/CollectionsApi.md#deleteCollection) | **DELETE** /collections/{collectionName} | Deletes a collection from SolrCloud
*V2Api.CollectionsApi* | [**listCollections**](docs/CollectionsApi.md#listCollections) | **GET** /collections | List all collections in this Solr cluster
*V2Api.CollectionsApi* | [**reloadCollection**](docs/CollectionsApi.md#reloadCollection) | **POST** /collections/{collectionName}/reload | Reload all cores in the specified collection.
*V2Api.CollectionsApi* | [**renameCollection**](docs/CollectionsApi.md#renameCollection) | **POST** /collections/{collectionName}/rename | Rename a SolrCloud collection
*V2Api.ConfigsetsApi* | [**listConfigSet**](docs/ConfigsetsApi.md#listConfigSet) | **GET** /cluster/configs | List the configsets available to Solr.
*V2Api.CoreBackupsApi* | [**createBackup**](docs/CoreBackupsApi.md#createBackup) | **POST** /cores/{coreName}/backups | Creates a core-level backup
*V2Api.CoreSnapshotsApi* | [**createSnapshot**](docs/CoreSnapshotsApi.md#createSnapshot) | **POST** /cores/{coreName}/snapshots/{snapshotName} | Create a new snapshot of the specified core.
*V2Api.CoreSnapshotsApi* | [**deleteSnapshot**](docs/CoreSnapshotsApi.md#deleteSnapshot) | **DELETE** /cores/{coreName}/snapshots/{snapshotName} | Delete a single snapshot from the specified core.
*V2Api.CoreSnapshotsApi* | [**listSnapshots**](docs/CoreSnapshotsApi.md#listSnapshots) | **GET** /cores/{coreName}/snapshots | List existing snapshots for the specified core.
*V2Api.CoresApi* | [**installCoreData**](docs/CoresApi.md#installCoreData) | **POST** /cores/{coreName}/install | Install an offline index to a specified core
*V2Api.CoresApi* | [**mergeIndexes**](docs/CoresApi.md#mergeIndexes) | **POST** /cores/{coreName}/merge-indices | The MERGEINDEXES action merges one or more indexes to another index.
*V2Api.CoresApi* | [**reloadCore**](docs/CoresApi.md#reloadCore) | **POST** /cores/{coreName}/reload | Reload the specified core.
*V2Api.CoresApi* | [**renameCore**](docs/CoresApi.md#renameCore) | **POST** /cores/{coreName}/rename | The RENAME action changes the name of a Solr core
*V2Api.CoresApi* | [**restoreCore**](docs/CoresApi.md#restoreCore) | **POST** /cores/{coreName}/restore | Restore a previously-taken backup to the specified core
*V2Api.CoresApi* | [**swapCores**](docs/CoresApi.md#swapCores) | **POST** /cores/{coreName}/swap | SWAP atomically swaps the names used to access two existing Solr cores.
*V2Api.CoresApi* | [**unloadCore**](docs/CoresApi.md#unloadCore) | **POST** /cores/{coreName}/unload | Unloads a single core specified by name
*V2Api.NodeApi* | [**deleteNode**](docs/NodeApi.md#deleteNode) | **POST** /cluster/nodes/{nodeName}/clear | Delete all replicas off of the specified SolrCloud node
*V2Api.NodeApi* | [**getCommandStatus**](docs/NodeApi.md#getCommandStatus) | **GET** /node/commands/{requestId} | Request the status of an already submitted asynchronous CoreAdmin API call.
*V2Api.NodeApi* | [**getPublicKey**](docs/NodeApi.md#getPublicKey) | **GET** /node/key | Retrieve the public key of the receiving Solr node.
*V2Api.NodeApi* | [**replaceNode**](docs/NodeApi.md#replaceNode) | **POST** /cluster/nodes/{sourceNodeName}/replace | &#39;Replace&#39; a specified node by moving all replicas elsewhere
*V2Api.QueryingApi* | [**jsonQuery**](docs/QueryingApi.md#jsonQuery) | **POST** /{indexType}/{indexName}/select | Query a Solr core or collection using the structured request DSL
*V2Api.QueryingApi* | [**query**](docs/QueryingApi.md#query) | **GET** /{indexType}/{indexName}/select | Query a Solr core or collection using individual query parameters
*V2Api.ReplicaPropertiesApi* | [**addReplicaProperty**](docs/ReplicaPropertiesApi.md#addReplicaProperty) | **PUT** /collections/{collName}/shards/{shardName}/replicas/{replicaName}/properties/{propName} | Adds a property to the specified replica
*V2Api.ReplicaPropertiesApi* | [**deleteReplicaProperty**](docs/ReplicaPropertiesApi.md#deleteReplicaProperty) | **DELETE** /collections/{collName}/shards/{shardName}/replicas/{replicaName}/properties/{propName} | Delete an existing replica property
*V2Api.ReplicasApi* | [**createReplica**](docs/ReplicasApi.md#createReplica) | **POST** /collections/{collectionName}/shards/{shardName}/replicas | Creates a new replica of an existing shard.
*V2Api.ReplicasApi* | [**deleteReplicaByName**](docs/ReplicasApi.md#deleteReplicaByName) | **DELETE** /collections/{collectionName}/shards/{shardName}/replicas/{replicaName} | Delete an single replica by name
*V2Api.ReplicasApi* | [**deleteReplicasByCount**](docs/ReplicasApi.md#deleteReplicasByCount) | **DELETE** /collections/{collectionName}/shards/{shardName}/replicas | Delete one or more replicas from the specified collection and shard
*V2Api.ReplicasApi* | [**deleteReplicasByCountAllShards**](docs/ReplicasApi.md#deleteReplicasByCountAllShards) | **PUT** /collections/{collectionName}/scale | Scale the replica count for all shards in the specified collection
*V2Api.SchemaApi* | [**getSchemaInfo**](docs/SchemaApi.md#getSchemaInfo) | **GET** /{indexType}/{indexName}/schema | Fetch the entire schema of the specified core or collection
*V2Api.SchemaApi* | [**getSchemaName**](docs/SchemaApi.md#getSchemaName) | **GET** /{indexType}/{indexName}/schema/name | Get the name of the schema used by the specified core or collection
*V2Api.SchemaApi* | [**getSchemaSimilarity**](docs/SchemaApi.md#getSchemaSimilarity) | **GET** /{indexType}/{indexName}/schema/similarity | Get the default similarity configuration used by the specified core or collection
*V2Api.SchemaApi* | [**getSchemaUniqueKey**](docs/SchemaApi.md#getSchemaUniqueKey) | **GET** /{indexType}/{indexName}/schema/uniquekey | Fetch the uniquekey of the specified core or collection
*V2Api.SchemaApi* | [**getSchemaVersion**](docs/SchemaApi.md#getSchemaVersion) | **GET** /{indexType}/{indexName}/schema/version | Fetch the schema version currently used by the specified core or collection
*V2Api.SchemaApi* | [**getSchemaZkVersion**](docs/SchemaApi.md#getSchemaZkVersion) | **GET** /{indexType}/{indexName}/schema/zkversion | Fetch the schema version currently used by the specified core or collection
*V2Api.ShardsApi* | [**createShard**](docs/ShardsApi.md#createShard) | **POST** /collections/{collectionName}/shards | Create a new shard in an existing collection
*V2Api.ShardsApi* | [**deleteShard**](docs/ShardsApi.md#deleteShard) | **DELETE** /collections/{collectionName}/shards/{shardName} | Delete an existing shard
*V2Api.ShardsApi* | [**forceShardLeader**](docs/ShardsApi.md#forceShardLeader) | **POST** /collections/{collectionName}/shards/{shardName}/force-leader | Force leader election to occur on the specified collection and shard
*V2Api.ShardsApi* | [**installShardData**](docs/ShardsApi.md#installShardData) | **POST** /collections/{collName}/shards/{shardName}/install | Install offline index into an existing shard
*V2Api.ShardsApi* | [**syncShard**](docs/ShardsApi.md#syncShard) | **POST** /collections/{collectionName}/shards/{shardName}/sync | Trigger a &#39;sync&#39; operation for the specified shard


## Documentation for Models

 - [V2Api.AddReplicaPropertyRequestBody](docs/AddReplicaPropertyRequestBody.md)
 - [V2Api.BackupDeletionData](docs/BackupDeletionData.md)
 - [V2Api.BackupDeletionResponseBody](docs/BackupDeletionResponseBody.md)
 - [V2Api.BalanceReplicasRequestBody](docs/BalanceReplicasRequestBody.md)
 - [V2Api.BalanceShardUniqueRequestBody](docs/BalanceShardUniqueRequestBody.md)
 - [V2Api.CollectionBackupDetails](docs/CollectionBackupDetails.md)
 - [V2Api.CreateCollectionBackupRequestBody](docs/CreateCollectionBackupRequestBody.md)
 - [V2Api.CreateCollectionRequestBody](docs/CreateCollectionRequestBody.md)
 - [V2Api.CreateCollectionRouterProperties](docs/CreateCollectionRouterProperties.md)
 - [V2Api.CreateCollectionSnapshotRequestBody](docs/CreateCollectionSnapshotRequestBody.md)
 - [V2Api.CreateCollectionSnapshotResponse](docs/CreateCollectionSnapshotResponse.md)
 - [V2Api.CreateCoreBackupRequestBody](docs/CreateCoreBackupRequestBody.md)
 - [V2Api.CreateCoreSnapshotResponse](docs/CreateCoreSnapshotResponse.md)
 - [V2Api.CreateReplicaRequestBody](docs/CreateReplicaRequestBody.md)
 - [V2Api.CreateShardRequestBody](docs/CreateShardRequestBody.md)
 - [V2Api.DeleteCollectionSnapshotResponse](docs/DeleteCollectionSnapshotResponse.md)
 - [V2Api.DeleteNodeRequestBody](docs/DeleteNodeRequestBody.md)
 - [V2Api.DeleteSnapshotResponse](docs/DeleteSnapshotResponse.md)
 - [V2Api.ErrorInfo](docs/ErrorInfo.md)
 - [V2Api.ErrorMetadata](docs/ErrorMetadata.md)
 - [V2Api.FlexibleSolrJerseyResponse](docs/FlexibleSolrJerseyResponse.md)
 - [V2Api.GetAliasByNameResponse](docs/GetAliasByNameResponse.md)
 - [V2Api.GetAliasPropertyResponse](docs/GetAliasPropertyResponse.md)
 - [V2Api.GetAllAliasPropertiesResponse](docs/GetAllAliasPropertiesResponse.md)
 - [V2Api.GetNodeCommandStatusResponse](docs/GetNodeCommandStatusResponse.md)
 - [V2Api.IndexType](docs/IndexType.md)
 - [V2Api.InstallCoreDataRequestBody](docs/InstallCoreDataRequestBody.md)
 - [V2Api.InstallShardDataRequestBody](docs/InstallShardDataRequestBody.md)
 - [V2Api.ListAliasesResponse](docs/ListAliasesResponse.md)
 - [V2Api.ListCollectionBackupsResponse](docs/ListCollectionBackupsResponse.md)
 - [V2Api.ListCollectionsResponse](docs/ListCollectionsResponse.md)
 - [V2Api.ListConfigsetsResponse](docs/ListConfigsetsResponse.md)
 - [V2Api.ListCoreSnapshotsResponse](docs/ListCoreSnapshotsResponse.md)
 - [V2Api.MergeIndexesRequestBody](docs/MergeIndexesRequestBody.md)
 - [V2Api.MigrateReplicasRequestBody](docs/MigrateReplicasRequestBody.md)
 - [V2Api.PublicKeyResponse](docs/PublicKeyResponse.md)
 - [V2Api.PurgeUnusedFilesRequestBody](docs/PurgeUnusedFilesRequestBody.md)
 - [V2Api.PurgeUnusedResponse](docs/PurgeUnusedResponse.md)
 - [V2Api.PurgeUnusedStats](docs/PurgeUnusedStats.md)
 - [V2Api.ReloadCollectionRequestBody](docs/ReloadCollectionRequestBody.md)
 - [V2Api.ReloadCoreRequestBody](docs/ReloadCoreRequestBody.md)
 - [V2Api.RenameCollectionRequestBody](docs/RenameCollectionRequestBody.md)
 - [V2Api.RenameCoreRequestBody](docs/RenameCoreRequestBody.md)
 - [V2Api.ReplaceNodeRequestBody](docs/ReplaceNodeRequestBody.md)
 - [V2Api.ResponseHeader](docs/ResponseHeader.md)
 - [V2Api.RestoreCoreRequestBody](docs/RestoreCoreRequestBody.md)
 - [V2Api.ScaleCollectionRequestBody](docs/ScaleCollectionRequestBody.md)
 - [V2Api.SchemaInfoResponse](docs/SchemaInfoResponse.md)
 - [V2Api.SchemaNameResponse](docs/SchemaNameResponse.md)
 - [V2Api.SchemaSimilarityResponse](docs/SchemaSimilarityResponse.md)
 - [V2Api.SchemaUniqueKeyResponse](docs/SchemaUniqueKeyResponse.md)
 - [V2Api.SchemaVersionResponse](docs/SchemaVersionResponse.md)
 - [V2Api.SchemaZkVersionResponse](docs/SchemaZkVersionResponse.md)
 - [V2Api.SnapshotInformation](docs/SnapshotInformation.md)
 - [V2Api.SolrJerseyResponse](docs/SolrJerseyResponse.md)
 - [V2Api.SubResponseAccumulatingJerseyResponse](docs/SubResponseAccumulatingJerseyResponse.md)
 - [V2Api.SwapCoresRequestBody](docs/SwapCoresRequestBody.md)
 - [V2Api.UnloadCoreRequestBody](docs/UnloadCoreRequestBody.md)
 - [V2Api.UpdateAliasPropertiesRequestBody](docs/UpdateAliasPropertiesRequestBody.md)
 - [V2Api.UpdateAliasPropertyRequestBody](docs/UpdateAliasPropertyRequestBody.md)
 - [V2Api.UpdateCollectionPropertyRequestBody](docs/UpdateCollectionPropertyRequestBody.md)


## Documentation for Authorization

All endpoints do not require authorization.