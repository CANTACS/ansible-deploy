# DVM Deployment Playbooks

#### Install the roles:
```
ansible-galaxy install -r roles/requirements.yml -p ./roles
```

## FNE

### Role Variables

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| install | Set this variable to install/reinstall the DVM Project FNE to the host. This might be useful to turn off if you use the role to regenerate the configs. | true | No |
| use_netbird | Set this to true if Netbird is installed on the host | false | No |
| dvm_folder | Set this variable to use a custom folder name throughout the role | dvm | No |
| dvmprov | Set this variable to install the DVM Provisioning Manager to the FNE host | true | No |

### Limitations

It is **highly recommended** to set `install` to `true` if you make configuration changes, as it is possible the underlying binary has had changes.

## Sites (hosts)

### Role Variables

| Variable | Description | Default | Required |
|----------|-------------|---------|----------|
| use_netbird | Set this to true if Netbird is installed on the host | false | No |
| dvm_folder | Set this variable to use a custom folder name throughout the role | dvm | No |

### Limitations

- This role only supports P25.  While DVM supports DMR and NXDN, I did not add support for configuring them as part of this role.
- This role does not *yet* support DVRS mode.  Support for DVRS mode is planned in the future.

PRs are welcomed if you want to help add support for either of those things.