# AZCLI

This role installs the Azure CLI on Windows or Linux servers.

## Requirements

There are no external requirements for this role.

## Role Variables

There are a few variables that can be set from the playbook if you like and the role makes an assumption in the defaults
section.

### azcli_version

This is the version of Azure CLI that will be installed, the complete list can be found on the [Azure CLI Release](https://github.com/Azure/azure-cli/releases) page.

```yaml
  azcli_version: 2.16.0
```

### download_dir

This is the directory where the Terraform installation package will be downloaded to.

#### Windows Default

```yaml
  download_dir: "C:\\Windows\\Temp"
```

#### Linux Default

```yaml
  download_dir: "/tmp"
```

## Dependencies

There are no external dependencies for this role.

## Example Playbooks

A playbook that installs a specific version of the Azure CLI to all hosts.

```yaml
    - hosts: all
      roles:
         - azcli
      vars:
        azcli_version: 2.16.0
```

## License

MIT

## Author Information

My name is Jeff Patton, feel free to contact me via [issues](https://github.com/anisble-playbooks/azcli/issues).
