# ACME Verify Account Positions

This project is an RPA (Robotic Process Automation) solution for verifying account positions using UiPath. It is structured into two main components: **Dispatcher** and **Performer**, each with their own workflows and supporting modules.

## Project Structure

```
ACME Verify Account Positions/
├── ACME_Dispatcher/
│   ├── Main.xaml
│   ├── project.json
│   ├── ACMEWeb/
│   │   ├── ACMEWeb_CloseApp.xaml
│   │   ├── ACMEWeb_ExtractWorkItems.xaml
│   │   ├── ACMEWeb_InitializeApp.xaml
│   │   ├── ACMEWeb_Login.xaml
│   │   ├── ACMEWeb_Logout.xaml
│   │   └── ACMEWeb_NavigateWorkItems.xaml
│   ├── Control/
│   │   └── WorkflowControl_CheckLoginStatus.xaml
│   ├── DataManagement/
│   │   └── DataManagement_InitializeAssets.xaml
│   └── Dispatcher/
│       └── Dispatcher_DispatchWorkItems.xaml
├── ACME_Performer/
│   ├── Main.xaml
│   ├── project.json
│   ├── ACMEDesktop/
│   │   ├── ACMEDesktop_CloseApp.xaml
│   │   ├── ACMEDesktop_ControlTabs.xaml
│   │   ├── ACMEDesktop_InitializeApp.xaml
│   │   ├── ACMEDesktop_Login.xaml
│   │   ├── ACMEDesktop_NavigateToAccountTransactions.xaml
│   │   ├── ACMEDesktop_NavigateToClientAccounts.xaml
│   │   ├── ACMEDesktop_NavigateToClientDetails.xaml
│   │   ├── ACMEDesktop_NavigateToClientSearch.xaml
│   │   └── ACMEDesktop_SumAccountTransactions.xaml
│   ├── ACMEWeb/
│   │   ├── ACMEWeb_CloseApp.xaml
│   │   ├── ACMEWeb_ExtractWorkItemData.xaml
│   │   ├── ACMEWeb_InitializeApp.xaml
│   │   ├── ACMEWeb_Login.xaml
│   │   ├── ACMEWeb_Logout.xaml
│   │   ├── ACMEWeb_NavigateToUpdateWorkItem.xaml
│   │   └── ACMEWeb_UpdateWorkItem.xaml
│   ├── Control/
│   │   ├── Control_CheckAccountPosition.xaml
│   │   ├── Control_CheckLoginStatusACME1.xaml
│   │   ├── Control_CloseApps.xaml
│   │   └── Control_InitializeApps.xaml
│   └── DataManagement/
│       ├── DataManagement_InitializeAssets.xaml
│       └── DataManagement_RetrieveQueueItem.xaml
```

## Components Overview

### 1. ACME_Dispatcher
Responsible for extracting work items from the ACME web application and dispatching them to the Orchestrator queue.
- **Main.xaml**: Entry point for dispatcher process.
- **ACMEWeb/**: Web automation workflows (login, extract, navigation, etc.).
- **Control/**: Workflow control and login status checks.
- **DataManagement/**: Asset initialization.
- **Dispatcher/**: Dispatches work items to the queue.

### 2. ACME_Performer
Processes the work items from the queue, performing required actions in both web and desktop applications.
- **Main.xaml**: Entry point for performer process.
- **ACMEDesktop/**: Desktop automation workflows (login, navigation, transaction processing, etc.).
- **ACMEWeb/**: Web automation for updating work items and related actions.
- **Control/**: Application control and status checks.
- **DataManagement/**: Asset initialization and queue item retrieval.

## Key Features
- Modular design for easy maintenance and scalability.
- Separation of dispatcher and performer for robust queue-based processing.
- Reusable workflows for login, navigation, and data extraction.
- Supports both web and desktop automation.

## How to Use
1. **Configure Assets and Queues** in UiPath Orchestrator as required by the workflows.
2. **Run the Dispatcher** to extract and dispatch work items.
3. **Run the Performer** to process the dispatched items.

## Technologies Used
- UiPath Studio
- UiPath Orchestrator
- RPA best practices (modularization, reusability, error handling)

## Author
- Amr Ayman

---


