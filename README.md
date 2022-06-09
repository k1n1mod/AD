# AD
## Add user to your Domian
Add User to your Domain
>addUserToAD.ps1
## Add users to your Domian via CSV
Add Users to your Domain via csv
>addUsersToADViaCSV.ps1
## Move one user in the ActiveDirectory to a group
Move User 1 to Group 1
>addUserToAD.ps1
```
Add-ADGroupMember -Identity <groupName> -Members <userName>
```
## Move more users into a group via csv
Move the users form the csv to the diffrent groups
>addOneUserToGroup.ps1
```
import-csv C:\Path\group.csv | ForEach-Object {Add-ADGroupMember -Identity $_.groupname -Members $_.username}
```
## Remove more users from a group via csv
Move the users form the csv to the diffrent groups
>removeMoreUserToGroupViaCSV.ps1
```
import-csv C:\Path\group.csv | ForEach-Object {remove-ADGroupMember -Identity $_.groupname -Members $_.username}
```