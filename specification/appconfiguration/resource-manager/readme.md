# AppConfiguration

> see https://aka.ms/autorest

This is the AutoRest configuration file for AppConfiguration.

---

## Getting Started

To build the SDK for AppConfiguration, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

### Basic Information

These are the global settings for the AppConfiguration API.

``` yaml
openapi-type: arm
tag: package-2025-02-01-preview
```

### Tag: package-2025-02-01-preview

These settings apply only when `--tag=package-2025-02-01-preview` is specified on the command line.

```yaml $(tag) == 'package-2025-02-01-preview'
input-file:
  - Microsoft.AppConfiguration/preview/2025-02-01-preview/appconfiguration.json
```

### Tag: package-preview-2024-06-15-preview

These settings apply only when `--tag=package-preview-2024-06-15-preview` is specified on the command line.

```yaml $(tag) == 'package-preview-2024-06-15-preview'
input-file:
  - Microsoft.AppConfiguration/preview/2024-06-15-preview/appconfiguration.json
```

### Tag: package-2024-06-01

These settings apply only when `--tag=package-2024-06-01` is specified on the command line.

```yaml $(tag) == 'package-2024-06-01'
input-file:
  - Microsoft.AppConfiguration/stable/2024-06-01/appconfiguration.json

```

### Tag: package-2024-05-01

These settings apply only when `--tag=package-2024-05-01` is specified on the command line.

```yaml $(tag) == 'package-2024-05-01'
input-file:
  - Microsoft.AppConfiguration/stable/2024-05-01/appconfiguration.json
```

### Tag: package-2023-09-01-preview

These settings apply only when `--tag=package-2023-09-01-preview` is specified on the command line.

```yaml $(tag) == 'package-2023-09-01-preview'
input-file:
  - Microsoft.AppConfiguration/preview/2023-09-01-preview/appconfiguration.json
```

### Tag: package-2023-08-01-preview

These settings apply only when `--tag=package-2023-08-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2023-08-01-preview'
input-file:
  - Microsoft.AppConfiguration/preview/2023-08-01-preview/appconfiguration.json
```

### Tag: package-2023-03-01

These settings apply only when `--tag=packge-2023-03-01` is specified on the command line.

``` yaml $(tag) == 'package-2023-03-01'
input-file:
  - Microsoft.AppConfiguration/stable/2023-03-01/appconfiguration.json
```

### Tag: package-2022-05-01

These settings apply only when `--tag=2022-05-01` is specified on the command line.

``` yaml $(tag) == 'package-2022-05-01'
input-file:
- Microsoft.AppConfiguration/stable/2022-05-01/appconfiguration.json
```

### Tag: package-2022-03-01-preview

These settings apply only when `--tag=2022-03-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2022-03-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2022-03-01-preview/appconfiguration.json
```

### Tag: package-2021-10-01-preview

These settings apply only when `--tag=2021-10-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2021-10-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2021-10-01-preview/appconfiguration.json
```

### Tag: package-2021-03-01-preview

These settings apply only when `--tag=2021-03-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2021-03-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2021-03-01-preview/appconfiguration.json
```

### Tag: package-2020-07-01-preview

These settings apply only when `--tag=2020-07-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2020-07-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2020-07-01-preview/appconfiguration.json
```

### Tag: package-2020-06-01

These settings apply only when `--tag=package-2020-06-01` is specified on the command line.

``` yaml $(tag) == 'package-2020-06-01'
input-file:
- Microsoft.AppConfiguration/stable/2020-06-01/appconfiguration.json
```

### Tag: package-2019-11-01-preview

These settings apply only when `--tag=package-2019-11-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-11-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2019-11-01-preview/appconfiguration.json
```

### Tag: package-2019-02-01-preview

These settings apply only when `--tag=package-2019-02-01-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-02-01-preview'
input-file:
- Microsoft.AppConfiguration/preview/2019-02-01-preview/appconfiguration.json
```

### Tag: package-2019-10-01

These settings apply only when `--tag=package-2019-10-01` is specified on the command line.

``` yaml $(tag) == 'package-2019-10-01'
input-file:
- Microsoft.AppConfiguration/stable/2019-10-01/appconfiguration.json
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-ruby
    after_scripts:
      - bundle install && rake arm:regen_all_profiles['azure_mgmt_app_configuration']
  - repo: azure-resource-manager-schemas
  - repo: azure-powershell
```

## C#

See configuration in [readme.csharp.md](./readme.csharp.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## Java

See configuration in [readme.java.md](./readme.java.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Ruby

See configuration in [readme.ruby.md](./readme.ruby.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## CLI

See configuration in [readme.cli.md](./readme.cli.md)

## Suppression

``` yaml
directive:
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.NameAvailabilityStatus.properties.nameAvailable
    reason: This is standard for check name availability.
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.ApiKey.properties.readOnly
    reason: We did consider using an enum instead but found it to not be helpful.
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.KeyValueProperties.properties.locked
    reason: This is data plane level information proxied through the RP and cannot be changed.
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.ConfigurationStoreProperties.properties.disableLocalAuth
    reason: This is a standardized ARM API.
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.ConfigurationStorePropertiesUpdateParameters.properties.disableLocalAuth
    reason: This is a standardized ARM API.
  - suppress: EnumInsteadOfBoolean
    from: appconfiguration.json
    where: $.definitions.OperationDefinition.properties.isDataAction
    reason: This is a standardized ARM API.
  - suppress: NestedResourcesMustHaveListOperation
    from: appconfiguration.json
    where: $.definitions.KeyValue
    resource: Listing is not supported in ARM templates.
  - suppress: TrackedResourceListByImmediateParent
    from: appconfiguration.json
    where: $.definitions.KeyValue
    reason: Listing is not supported in ARM templates.
  - suppress: NestedResourcesMustHaveListOperation
    from: appconfiguration.json
    where: $.definitions.Snapshot
    reason: Following KeyValue, with both being proxies for data plane resources.
  - suppress: AllProxyResourcesShouldHaveDelete
    from: appconfiguration.json
    where: $.definitions.Snapshot
    reason: This is a proxy for a data plane snapshot which doesn't support delete.
  - suppress: RequiredReadOnlySystemData
    from: appconfiguration.json
    where: 
      - '$.paths["/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.AppConfiguration/configurationStores/{configStoreName}/snapshots/{snapshotName}"].get'
      - '$.paths["/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.AppConfiguration/configurationStores/{configStoreName}/snapshots/{snapshotName}"].put'
    reason: This is a proxy for a data plane snapshot which doesn't have the info.
  - suppress: TrackedResourcePatchOperation
    from: appconfiguration.json
    where: $.definitions.Replica
    reason: Replica is a proxy resource
```
