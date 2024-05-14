# Documentation

- [Documentation](#documentation)
  - [Common requirements](#common-requirements)
    - [PowerShell](#powershell)
    - [`Microsoft.Graph` PowerShell modules](#microsoftgraph-powershell-modules)
  - [Scripts](#scripts)
    - [Entra ID Roles](#entra-id-roles)
    - [Privileged Access Groups](#privileged-access-groups)

## Common requirements

### PowerShell

All of the scripts were written with PowerShell 7.4. I haven't tested with other versions, so your mileage may vary.

Documentation for installing PowerShell can be found:

- [Install PowerShell on Windows](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows)
- [Install PowerShell on Linux](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-linux)
- [Install PowerShell on macOS](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-macos)

### `Microsoft.Graph` PowerShell modules

While not all scripts require all of the modules in the `Microsoft.Graph` meta-module, it's easier to install them all.

> ⚠️ **Note:**
>
> The required modules are listed on each script's documentation page.

To install the `Microsoft.Graph` modules:

**`PowerShellGet`** (Available by default)

```powershell
Install-Module -Name "Microsoft.Graph" -Scope "CurrentUser"
```

**`Microsoft.PowerShell.PSResourceGet`**

```powershell
Install-PSResource -Name "Microsoft.Graph" -Scope "CurrentUser"
```

## Scripts

### Entra ID Roles

Scripts related to Entra ID roles.

| Name | Description |
| --- | --- |
| [`Remove-UserFromEntraIdRole.ps1`](./Entra-ID-Roles/Remove-UserFromEntraIdRole.md) | Remove a user from an Entra ID role. |

### Privileged Access Groups

Scripts related to Privileged Access Groups.

| Name | Description |
| --- | --- |
| [`Remove-UserFromPrivilegedAccessGroup.ps1`](./Groups/Remove-UserFromPrivilegedAccessGroup.md) | Remove a user from a Privileged Access Group. |
