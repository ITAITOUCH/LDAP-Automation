# PowerShell LDAP Automation Tool

This PowerShell script automates the process of creating, modifying, and uploading CSV files for LDAP (Lightweight Directory Access Protocol) management tasks. The script is tailored to work with a specified set of DC (Domain Controller) names, modifying certain columns within CSVs and preparing them for upload.

## Features ##

- **Create CSV**: Generates CSV files for each DC and exports them to a named CSV file.
- **Modify CSV**: Appends a date to a specified column within existing CSV files.
- **Delete Original CSV**: Removes the original CSV files, leaving only the modified ones.
- **Upload CSV**: Uploads the modified CSV files using a specific `.ini` configuration file.

## Parameters ##

The script accepts the following parameters:

- `inputPath`: The file path where the LDAP Loader executable and CSV files are located.
- `guid`: A unique identifier for the upload process.
- `columnToChange`: The name of the column in the CSV files that will be modified.

## Default Values ##

```powershell
param (
    [string]$inputPath = "C:\Program Files (x86)\Dcoya\LDap Automation Service",
    [string]$guid = "d65d037584e4406284de18a480d695c7",
    [string]$columnToChange = "group"
)

## Usage ## 

1.  Set up the necessary parameters in the script or pass them as arguments when invoking the script.
2.  Run the script. It will perform the following actions in order:
	- Create CSV files from each DC.
	- Modify the specified column of each CSV file by appending the current date.
	- Delete the original, unmodified CSV files.
	- Upload the modified CSV files.

## Functions ##
The script includes several functions:

Create-CSV-For-Any-DC: Creates a CSV for each DC.
Modify-CSV: Modifies the specified column in the CSV files.
Delete-Original-CSV: Deletes the original CSV files.
Upload-CSV: Uploads the modified CSV files using a corresponding .ini configuration file.

## Prerequisites ## 
PowerShell 5.0 or higher.
Access to the specified inputPath with the necessary permissions.
The Dcoya-Ldap-Loader.exe must be present at the inputPath.

## Important Notes ##
The script assumes .csv files and .ini configuration files are in the same directory.
Ensure that the Dcoya-Ldap-Loader.exe application has the appropriate permissions to execute.
Before running the script in a production environment, test it in a controlled setting to ensure it performs as expected.
