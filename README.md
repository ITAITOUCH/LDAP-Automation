# PowerShell LDAP Automation Tool
This PowerShell script is designed to automate the LDAP (Lightweight Directory Access Protocol) management tasks by creating, modifying, and uploading CSV files for different DC (Domain Controller) names.

## Features
- **Create CSV**: Generates individual CSV files for each specified DC.
- **Modify CSV**: Appends a date to the specified column within the CSV files.
- **Delete Original CSV**: Cleans up by removing the original, unmodified CSV files.
- **Upload CSV**: Handles the upload of modified CSV files using associated `.ini` configuration files.

## Usage
Before running the script, ensure that the parameters are correctly set to match your environment. The script performs a series of functions in a specified order: creating CSV files, modifying them, deleting the original versions, and finally, uploading the new ones.

### Step-by-Step Process:
1. The script first creates CSV files for each DC.
2. It then modifies a specified column by appending the current date to its values.
3. The original CSV files are deleted, leaving only the modified versions.
4. Lastly, the script uploads the modified CSV files, utilizing `.ini` configuration files for each upload.

## Functions
- `Create-CSV-For-Any-DC`: Creates a CSV file for each DC with the necessary information.
- `Modify-CSV`: Alters the specified column within the CSV files by appending the current date.
- `Delete-Original-CSV`: Removes the original CSV files from the directory.
- `Upload-CSV`: Performs the upload of the modified CSV files.

## Prerequisites
To ensure the script runs smoothly, you need:
- PowerShell 5.0 or higher.
- Proper access to the directory specified in `inputPath`.
- The `Dcoya-Ldap-Loader.exe` must be located in the `inputPath` directory.

## Important Notes
- Before executing the script, ensure that the `Dcoya-Ldap-Loader.exe` and the corresponding `.csv` and `.ini` files are present in the specified `inputPath`.
- Test the script in a non-production environment to validate its functionality.

## Contribution
Contributions to enhance the functionality or efficiency of this script are welcome. Please adhere to the coding standards established in the script and document your changes thoroughly.

When saving this content, name the file `README.md` and place it in the root directory of your repository. This will display the formatted README on your GitHub repository's main page. Remember to review and adjust the README as necessary to fit your specific project's needs or to add any additional instructions or information you find relevant.

