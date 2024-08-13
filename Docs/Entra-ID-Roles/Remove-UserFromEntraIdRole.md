# `Remove-UserFromEntraIdRole.ps1`

## Description

Remove a user's active or eligible assignment to an Entra ID role.

## Parameters

### `UserId`

The ID of the user in Entra ID.

### `RoleName`

The name of the directory role. If not provided, it will default to all directory roles.

## Examples

### Example 1

Removes the user's assignment from the "User Administrator" directory role.

```powershell
PS > Remove-UserFromEntraIdRole.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "User Administrator"
```

### Example 2

Removes the user's assignment from any directory role.

```powershell
PS > Remove-UserFromEntraIdRole.ps1 -UserId "jwinger@greendalecc.edu"
```

## Required Modules

| Module Name | Module Version |
| --- | --- |
| [`Microsoft.Graph.Authentication`](https://www.powershellgallery.com/packages/Microsoft.Graph.Authentication) | `2.17.0 <=` |
| [`Microsoft.Graph.Groups`](https://www.powershellgallery.com/packages/Microsoft.Graph.Groups) | `2.17.0 <=` |
| [`Microsoft.Graph.Users`](https://www.powershellgallery.com/packages/Microsoft.Graph.Users) | `2.17.0 <=` |
| [`Microsoft.Graph.Beta.Identity.Governance`](https://www.powershellgallery.com/packages/Microsoft.Graph.Beta.Identity.Governance) | `2.17.0 <=` |
