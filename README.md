# Get-ExchangeCUandSUcopytoServers
Download the required Exchange CU or SU (security update) and copy to all your Exchange servers at once

This is somesort of fork from the project started by Rune Moskvil Lyngås over at https://github.com/runely/PowerShell/tree/master/Get-ExchangeCU
All credit goes to Rune Moskvil Lyngås

I adjusted the module he made and added the SU's and the latest CU's including Exchange 2019

Run the module as follows:
Import-Module yourpath\Get-ExchangeCUandSUcopytoServers.psm1
Get-ExchangeCU -Version 2019_CU11_SU_JAN_2022 -Directory C$\Temp -Name server1,server2 -RemoveTemp

.Synopsis
Download Cumulative Update or Security Update for Exchange 2013/2016/2019
.DESCRIPTION
Download Cumulative Update or Security Update for Exchange 2013/2016/2019 to all or specified servers
.EXAMPLE
Get-ExchangeCU -Version "2013_CUn" -Name Server1,Server2 -Directory "C$\Source" -RemoveTemp
Download latest Cumulative Update for installed Exchange version (Exchange Management Shell required)
.EXAMPLE
Get-MailboxServer | Get-ExchangeCU -Version "2013_CUnr"
Download Cumulative Update to given Exchange servers at default location(\\Server\C$\Source).
.EXAMPLE
Get-ExchangeCU -Version "2013_CUnr" -Name Server1,Server2
Download Cumulative Update to given Exchange servers at default location(\\Server\C$\Source).
.EXAMPLE
Get-MailboxServer | Get-ExchangeCU -Version "2013_CUnr" -Directory "C$\Source" -RemoveTemp
Download Cumulative Update to given Exchange servers at specified location and remove temporary downloaded file
.EXAMPLE
Get-ExchangeCU -Version "2013_CUnr" -Name Server1,Server2 -Directory "C$\Source" -RemoveTemp
Download Cumulative Update to given Exchange servers at specified location and remove temporary downloaded file
   
