# Calculate Client Security Hash (UiPath REFramework Project)

## Overview
This project is a complete implementation of the **UiPath Robotic Enterprise Framework (REFramework)**, developed as part of the UiPath Automation Developer Professional training. The solution demonstrates best practices in building robust, scalable, and maintainable RPA processes using UiPath Studio.

## Project Purpose
The main goal of this project is to automate the calculation of the Client Security Hash for work items in the ACME test system. The automation follows the REFramework template, ensuring high reliability, modularity, and reusability.

## Project Structure

```
Calculate Client Security Hash/
│   LICENSE
│   Main.xaml
│   Main.xaml.json
│   project.json
│   README.md
│
├───Common/
│       SendEmail.xaml
│
├───Data/
│   │   Config.xlsx
│   ├───Input/
│   ├───Output/
│   └───Temp/
│
├───Documentation/
│       REFramework Documentation-EN.pdf
│
├───Exceptions_Screenshots/
│
├───Framework/
│       CloseAllApplications.xaml
│       GetTransactionData.xaml
│       InitAllApplications.xaml
│       InitAllSettings.xaml
│       KillAllProcesses.xaml
│       Process.xaml
│       RetryCurrentTransaction.xaml
│       SetTransactionStatus.xaml
│       TakeScreenshot.xaml
│
├───SHA1/
│       SHA1_Close.xaml
│       SHA1_Open.xaml
│       SHA1_ProcessHash.xaml
│
├───System1/
│       System1_Close.xaml
│       System1_Extract_ClientInformation.xaml
│       System1_Extract_WIsDataTable.xaml
│       System1_Login.xaml
│       System1_NavigateTo_UpdateworkItem.xaml
│       System1_NavigateTo_WIDetails.xaml
│       System1_NavigateTo_WorkItems.xaml
│       System1_Update_WorkItem.xaml
│
└───Tests/
        GetTransactionDataTestCase.xaml
        InitAllApplicationsTestCase.xaml
        InitAllSettingsTestCase.xaml
        MainTestCase.xaml
        ProcessTestCase.xaml
        Tests.xlsx
        WorkflowTestCaseTemplate.xaml
```

## Key Components
- **Main.xaml**: Entry point of the automation, orchestrates the REFramework workflow.
- **Framework/**: Contains core REFramework workflows for initialization, transaction processing, error handling, and cleanup.
- **Data/Config.xlsx**: Central configuration file for settings, constants, and asset references.
- **System1/**: Workflows for interacting with the ACME test system (login, navigation, data extraction, and update).
- **SHA1/**: Workflows for calculating the SHA1 hash required for the client security hash.
- **Common/**: Reusable components, such as email sending.
- **Tests/**: Automated test cases for validating individual components and end-to-end process.
- **Documentation/**: Includes the official REFramework documentation for reference.

## How It Works
1. **Initialization**: Loads configuration, assets, and opens required applications.
2. **Get Transaction Data**: Retrieves work items to process (from Orchestrator queue or data table).
3. **Process Transaction**: Extracts client information, computes the security hash, and updates the work item.
4. **End Process**: Closes all applications and performs cleanup.

## How to Use
1. Open the project in UiPath Studio.
2. Review and update `Data/Config.xlsx` as needed for your environment.
3. Run `Main.xaml` to execute the automation.
4. Use the test cases in the `Tests/` folder to validate individual components.

## Dependencies
- UiPath.Excel.Activities
- UiPath.Mail.Activities
- UiPath.System.Activities
- UiPath.Testing.Activities
- UiPath.UIAutomation.Activities

All dependencies are managed via `project.json`.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements
- Developed as part of the **UiPath Automation Developer Professional** training.
- Based on the official UiPath REFramework template.

---
