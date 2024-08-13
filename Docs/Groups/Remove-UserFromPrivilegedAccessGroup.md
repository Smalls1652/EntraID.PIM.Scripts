# `Remove-UserFromPrivilegedAccessGroup.ps1`

## Description

Remove a user from a Privileged Access Group(s) in Entra ID.

## Parameters

### `UserId`

The ID of the user in Entra ID.

### `GroupId`

The ID of the group in Entra ID. If not provided, all groups that are assignable to a role will be fetched.

### `RoleType`

The role type to remove the user from.

## Examples

### Example 1

Removes the user's "member" role from the group with the ID "00000000-0000-0000-0000-000000000000".

```powershell
PS > Remove-UserFromPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "00000000-0000-0000-0000-000000000000"
```

### Example 2

Removes the user's "member" role from any group that is assignable to a role.

```powershell
PS > Remove-UserFromPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu"
```

### Example 3

Removes the user's "owner" role from the group with the ID "00000000-0000-0000-0000-000000000000".

```powershell
PS > Remove-UserFromPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "00000000-0000-0000-0000-000000000000" -RoleType "owner"
```

## Required Modules

| Module Name | Module Version |
| --- | --- |
| [`Microsoft.Graph.Authentication`](https://www.powershellgallery.com/packages/Microsoft.Graph.Authentication) | `2.17.0 <=` |
| [`Microsoft.Graph.Groups`](https://www.powershellgallery.com/packages/Microsoft.Graph.Groups) | `2.17.0 <=` |
| [`Microsoft.Graph.Users`](https://www.powershellgallery.com/packages/Microsoft.Graph.Users) | `2.17.0 <=` |
| [`Microsoft.Graph.Beta.Identity.Governance`](https://www.powershellgallery.com/packages/Microsoft.Graph.Beta.Identity.Governance) | `2.17.0 <=` |
