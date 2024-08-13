# `Add-UserToPrivilegedAccessGroup.ps1`

## Description

Add a user to a privileged access group in Entra ID.

## Parameters

### `UserId`

The ID or UserPrincipalName of the user in Entra ID.

### `GroupId`

The ID of the group in Entra ID.

### `GroupName`

The name of the group in Entra ID.

### `RoleType`

Whether the user should be assigned as a member or owner of the group.

### `StartsOn`

The date and time the assignment will start. Defaults to the start of the current day.

### `ExpiresOn`

The date and time the assignment will expire. Defaults to six months from the current date.

### `AssignmentType`

Whether the assignment should be active or eligible.

### `Justification`

The justification for the assignment.

## Examples

### Example 1

Assigns the user as eligible to the group as a member that starts now and expires in six months.

```powershell
PS > Add-UserToPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "00000000-0000-0000-0000-000000000000"
```

### Example 2

Assigns the user as active to the group as a member that starts now and expires in three months.

```powershell
PS > Add-UserToPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu" -GroupId "00000000-0000-0000-0000-000000000000" -ExpiresOn ([System.DateTimeOffset]::Now.AddMonths(3)) -AssignmentType "Active"
```

### Example 3

Assigns the user as active to the group as an owner that starts on September 17th, 2009, at 8:00 AM and expires on May 9th, 2013, at 5:00 PM with the justification "Jeff is the leader of the group."

```powershell
PS > Add-UserToPrivilegedAccessGroup.ps1 -UserId "jwinger@greendalecc.edu" -GroupName "The Study Group" -RoleType "owner" -StartsOn "2009-09-17 08:00:00 -4:00" -ExpiresOn "2013-05-09 17:00 -4:00" -AssignmentType "Active" -Justification "Jeff is the leader of the group."
```

## Required Modules

| Module Name | Module Version |
| --- | --- |
| [`Microsoft.Graph.Authentication`](https://www.powershellgallery.com/packages/Microsoft.Graph.Authentication) | `2.17.0 <=` |
| [`Microsoft.Graph.Groups`](https://www.powershellgallery.com/packages/Microsoft.Graph.Groups) | `2.17.0 <=` |
| [`Microsoft.Graph.Users`](https://www.powershellgallery.com/packages/Microsoft.Graph.Users) | `2.17.0 <=` |
| [`Microsoft.Graph.Beta.Identity.Governance`](https://www.powershellgallery.com/packages/Microsoft.Graph.Beta.Identity.Governance) | `2.17.0 <=` |
