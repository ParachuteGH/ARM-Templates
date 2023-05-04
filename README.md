# Introduction 
ARM Templates are designed to automate Azure deployments and implement Parachute standards and best practices.


> This repository is designed to host the parent JSON templates so that the "**Deploy to Azure**" button can be created and hosted in Azure DevOps readme files. 


# Getting Started (Create Deploy to Azure Button)
1.	Click "**Add File**"
2.	Type "***Folder Name***" 
3.	Add "***/***" to the end
4.	Type "***ARM Template Name***"
5.	Paste your parent JSON code
6.	Click "**Commit Changes**"
7.	Copy the "**RAW**" URL of the parent template
8.  Convert URL to URL-encoded value by pasting **RAW** URL into the PowerShell script below
  
```
$url = "<RAW_URL_HERE>"
$convertedURL = [uri]::EscapeDataString($url)
$appendURL = "https://portal.azure.com/#create/Microsoft.Template/uri/" + $convertedURL
$azureButton = "[![Deploy to Azure](https://aka.ms/deploytoazurebutton)]("+$appendURL+")"

Write-Host "`n`nAzure Button:"
Write-Host $azureButton -ForegroundColor Yellow
```

9.  Paste PowerShell output into the Azure DevOps README.md file


# Contribute
If you notice that there are errors or you have suggestions please submit them to akrytus@parachutetechs.com 


