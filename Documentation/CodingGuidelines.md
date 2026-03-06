# Neos Coding Guidelines

## Attributes

Almost always needed in any applicable php file:

```php
use Neos\Flow\Annotations as Flow;
```

> [!NOTE]
> Always use PHP native attributes instead of doc-block. Only use doc-block if the user says so.c

### Injection

Neos Flow provides dependency injection.

Always write it as:

```php
    #[Flow\Inject()]
    protected MyServiceInterface $myService
```

## Configuration

Create configuration files ONLY in the `Configuration` Folder.

The only allowed configuration FileNamePrefixes are:

- `Settings`
- `Objects`
- `Routes`
- `Caches`

> [!IMPORTANT]
> On legacy systems there is also the `NodeType` type. This should be avoided and any new code/Node Type configuration should be put in the `NodeTypes` folder instead.

### Semantic Naming

When creating a new Configuration File you should add the package for which the configuration is as part of the filename.
The exception is the setting for the current package.

#### Example: Vendor.Site

**Configuration**:

```yaml
Vendor:
    Site:
        someSetting: true
```

_Resulting File_: `Vendor.Site/Configuration/Settings.yaml`

#### Example: Neos.Flow

**Configuration**:

```yaml
Neos:
    Flow:
        # override
        someSetting: true
```

_Resulting File_: `Vendor.Site/Configuration/Settings.Neos.Flow.yaml`

#### Example: Neos.Neos

**Configuration**:

```yaml
Neos:
    Neos:
        # override
        cmsSetting: true
```

_Resulting File_: `Vendor.Site/Configuration/Settings.Neos.Neos.yaml`
