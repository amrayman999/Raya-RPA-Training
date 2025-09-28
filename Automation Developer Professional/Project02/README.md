# Generate Yearly Report - Project Documentation

This project automates the process of generating yearly reports using UiPath's Robotic Enterprise Framework (REFramework). It is divided into two main components: **Dispatcher** and **Performer**. Each component follows best practices for modularity, error handling, and reusability.

---


## Project Structure

```
Generate Yearly Report/
├── Dispatcher/
│   ├── Data/
│   │   ├── Config.xlsx
│   │   ├── Input/
│   │   │   └── placeholder.txt
│   │   ├── Output/
│   │   │   └── placeholder.txt
│   │   └── Temp/
│   │       └── placeholder.txt
│   ├── Documentation/
│   │   └── REFramework Documentation-EN.pdf
│   ├── Exceptions_Screenshots/
│   │   └── placeholder.txt
│   ├── Framework/
│   │   ├── CloseAllApplications.xaml
│   │   ├── GetTransactionData.xaml
│   │   ├── InitAllApplications.xaml
│   │   ├── InitAllSettings.xaml
│   │   ├── KillAllProcesses.xaml
│   │   ├── Process.xaml
│   │   ├── RetryCurrentTransaction.xaml
│   │   ├── SetTransactionStatus.xaml
│   │   └── TakeScreenshot.xaml
│   ├── System1/
│   │   ├── System1_Close.xaml
│   │   ├── System1_Extract_WIsDataTable.xaml
│   │   ├── System1_FilterWIDataTable.xaml
│   │   ├── System1_Login.xaml
│   │   └── System1_NavigateTo_WorkItems.xaml
│   ├── Tests/
│   │   ├── GetTransactionDataTestCase.xaml
│   │   ├── InitAllApplicationsTestCase.xaml
│   │   ├── InitAllSettingsTestCase.xaml
│   │   ├── MainTestCase.xaml
│   │   ├── ProcessTestCase.xaml
│   │   ├── Tests.xlsx
│   │   └── WorkflowTestCaseTemplate.xaml
│   ├── LICENSE
│   ├── Main.xaml
│   ├── Main.xaml.json
│   ├── project.json
│   └── README.md
├── Performer/
│   ├── Data/
│   │   ├── Config.xlsx
│   │   ├── Input/
│   │   │   └── placeholder.txt
│   │   ├── Output/
│   │   │   ├── placeholder.txt
│   │   │   └── Reports/
│   │   │       ├── Yearly-Report-2024-DE325476.xlsx
│   │   │       ├── Yearly-Report-2024-DE456232.xlsx
│   │   │       ├── Yearly-Report-2024-FR065748.xlsx
│   │   │       ├── Yearly-Report-2024-FR121212.xlsx
│   │   │       ├── Yearly-Report-2024-FR329083.xlsx
│   │   │       ├── Yearly-Report-2024-IT754893.xlsx
│   │   │       ├── Yearly-Report-2024-RO212121.xlsx
│   │   │       ├── Yearly-Report-2024-RO254678.xlsx
│   │   │       ├── Yearly-Report-2024-RO657483.xlsx
│   │   │       └── Yearly-Report-2024-RO874231.xlsx
│   │   └── Temp/
│   │       └── placeholder.txt
│   ├── Documentation/
│   │   └── REFramework Documentation-EN.pdf
│   ├── Exceptions_Screenshots/
│   │   ├── ExceptionScreenshot_250927.010313.png
│   │   ├── ExceptionScreenshot_250927.010328.png
│   │   ├── ExceptionScreenshot_250927.010343.png
│   │   ├── ExceptionScreenshot_250927.011057.png
│   │   ├── ExceptionScreenshot_250927.013521.png
│   │   ├── ExceptionScreenshot_250927.014203.png
│   │   ├── ExceptionScreenshot_250927.020842.png
│   │   ├── ExceptionScreenshot_250927.031018.png
│   │   ├── ExceptionScreenshot_250927.124120.png
│   │   └── placeholder.txt
│   ├── Framework/
│   │   ├── CloseAllApplications.xaml
│   │   ├── GetTransactionData.xaml
│   │   ├── InitAllApplications.xaml
│   │   ├── InitAllSettings.xaml
│   │   ├── KillAllProcesses.xaml
│   │   ├── Process.xaml
│   │   ├── RetryCurrentTransaction.xaml
│   │   ├── SetTransactionStatus.xaml
│   │   └── TakeScreenshot.xaml
│   ├── System1/
│   │   ├── System1_Close.xaml
│   │   ├── System1_DownloadMonthlyReports.xaml
│   │   ├── System1_Extract_ClientDetails.xaml
│   │   ├── System1_Login.xaml
│   │   ├── System1_MergeMonthlyReports.xaml
│   │   ├── System1_NavigateTo.xaml
│   │   ├── System1_Update_WorkItem.xaml
│   │   └── System1_UploadYearlyReport.xaml
│   ├── Tests/
│   │   ├── GetTransactionDataTestCase.xaml
│   │   ├── InitAllApplicationsTestCase.xaml
│   │   ├── InitAllSettingsTestCase.xaml
│   │   ├── MainTestCase.xaml
│   │   ├── ProcessTestCase.xaml
│   │   ├── Tests.xlsx
│   │   └── WorkflowTestCaseTemplate.xaml
│   ├── LICENSE
│   ├── Main.xaml
│   ├── Main.xaml.json
│   ├── project.json
│   └── README.md
```

---

## Dispatcher
Responsible for reading and queuing work items for processing. 

### Key Folders & Files
- **Data/**: Contains configuration (`Config.xlsx`), input, output, and temp data folders.
- **Documentation/**: REFramework documentation.
- **Exceptions_Screenshots/**: Stores screenshots of exceptions for debugging.
- **Framework/**: Contains reusable workflows for application and process management (e.g., `InitAllApplications.xaml`, `GetTransactionData.xaml`).
- **System1/**: Workflows for interacting with the target system (e.g., login, data extraction, navigation).
- **Tests/**: Test cases and templates for validating workflows.
- **Main.xaml**: Entry point for the Dispatcher process.
- **project.json**: Project metadata and dependencies.

### Main Workflows
- **InitAllApplications.xaml**: Initializes all required applications.
- **GetTransactionData.xaml**: Retrieves transaction data for processing.
- **Process.xaml**: Main logic for processing each transaction.
- **SetTransactionStatus.xaml**: Updates the status of each transaction.

---

## Performer
Responsible for processing the queued work items and generating the yearly reports.

### Key Folders & Files
- **Data/**: Configuration and data folders similar to Dispatcher.
- **Documentation/**: REFramework documentation.
- **Exceptions_Screenshots/**: Exception screenshots for debugging.
- **Framework/**: Reusable workflows for process management.
- **System1/**: Workflows for interacting with the system (e.g., downloading reports, merging, uploading).
- **Tests/**: Test cases for workflow validation.
- **Main.xaml**: Entry point for the Performer process.
- **project.json**: Project metadata and dependencies.

### Main Workflows
- **System1_DownloadMonthlyReports.xaml**: Downloads monthly reports for each client.
- **System1_MergeMonthlyReports.xaml**: Merges monthly reports into a yearly report.
- **System1_UploadYearlyReport.xaml**: Uploads the generated yearly report.
- **System1_Update_WorkItem.xaml**: Updates the status of processed work items.

---

## REFramework Usage
Both Dispatcher and Performer are built on UiPath's REFramework, ensuring:
- Robust error handling and retry mechanisms
- Modular and reusable workflow design
- Easy configuration and extensibility

---

## How to Use
1. **Configure**: Update `Config.xlsx` in both Dispatcher and Performer with environment-specific settings.
2. **Run Dispatcher**: Use `Main.xaml` in Dispatcher to queue work items.
3. **Run Performer**: Use `Main.xaml` in Performer to process the queue and generate reports.
4. **Review Outputs**: Check the `Output/` folders and exception screenshots as needed.

---

## Testing
- Test cases are provided in the `Tests/` folders for both Dispatcher and Performer.
- Use these to validate individual workflows and the overall process.

---

## License
See `LICENSE` files in each component for licensing information.

---

## Additional Notes
- Exception screenshots are automatically saved for failed transactions.
- Documentation is provided for reference on REFramework best practices.
- The project is structured for scalability and maintainability.
