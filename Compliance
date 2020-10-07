function Get-Runningservices {
    Write-Host "Getting Running Services..."
    <#Get-Service | Where-Object {$_.Status -eq "stopped"}#>
    Get-Service -RequiredServices | Where-Object {$_.Status -eq "Running"} | Sort-Object status | Format-Table
     

    }

function Get-Runningprocesses {
    Write-Host "Getting Running Processes..."
    Get-Process | Select-Object -Property Name, SI, Id, MachineName, WorkingSet, Priorityclass | Where-Object {$_.WorkingSet -ge 20000000} | Format-Table

    

    }

function Get-Compliantusers {

    }

    
Get-Runningservices
Get-Runningprocesses
#Get-Compliantusers
