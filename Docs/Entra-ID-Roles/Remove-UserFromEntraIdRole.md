# `Remove-UserFromEntraIdRole.ps1`

## SYNOPSIS

Remove a user's assignment to an Entra ID role.

## DESCRIPTION

Remove a user's active or eligible assignment to an Entra ID role.

## PARAMETERS

### `UserId`

The ID of the user in Entra ID.

### `RoleName`

The name of the directory role. If not provided, it will default to all directory roles.

## EXAMPLES

### EXAMPLE 01

Removes the user's assignment from the "User Administrator" directory role.

```powershell
Remove-UserFromEntraIdRole.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "User Administrator"
```

### EXAMPLE 02

Removes the user's assignment from any directory role.

```powershell
Remove-UserFromEntraIdRole.ps1 -UserId "jwinger@greendalecc.edu"
```

## REQUIRED MODULES

| Module Name | Version |
| --- | --- |
| `Microsoft.Graph.Authentication` | `2.17.0 <=` |
| `Microsoft.Graph.Groups` | `2.17.0 <=` |
| `Microsoft.Graph.Users` | `2.17.0 <=` |
| `Microsoft.Graph.Beta.Identity.Governance` | `2.17.0 <=` |
