# Extract Corona Numbers To Text

## Overview

This UiPath automation extracts COVID-19 statistics for a user-specified country from Worldometer, then writes the results to a formatted Notepad file. The project supports both classic and modern workflows.

![Automation Recording](https://github.com/amrayman999/Raya-RPA-Training/blob/master/Automation%20Developer%20Associate/Task02/AutomationRecording.gif)

## Workflows

### Main.xaml
- Entry point for the automation.
- Invokes either [`ClassicWorkFlow`](Project/ExtractCoronaNumbersToText/ClassicWorkFlow.xaml) or [`ModernWorkFlow`](Project/ExtractCoronaNumbersToText/ModernWorkFlow.xaml) based on project requirements.

### ClassicWorkFlow.xaml
- Uses classic activities to:
  - Prompt the user for a country name.
  - Launch a browser and search for COVID-19 statistics.
  - Extract cases, deaths, and recoveries.
  - Write the results to a Notepad file.

### ModernWorkFlow.xaml
- Uses modern activities and application cards for improved reliability.
- Steps:
  1. **Input Dialog**: Prompts for the country name.
  2. **Edge Browser Automation**:
     - Types the search query in Google.
     - Clicks the search button.
     - Clicks the first result (Worldometer).
     - Extracts cases, deaths, and recoveries using selectors.
  3. **Notepad Automation**:
     - Types the extracted data into Notepad in a formatted way.
     - Applies font family, style, and size.
     - Saves the file in the `CoronaNumbers` folder with a timestamped filename.
     - Closes the Notepad tab.

## Variables

- `strCountryName`: Country to search for.
- `strCoronaCases`: Extracted cases.
- `strCoronaDeaths`: Extracted deaths.
- `strCoronaRecoveries`: Extracted recoveries.
- `strFullFilePath`: Path for saving the output file.

## Output

- A text file named `{CountryName}-{yyyy-MM-dd_HH-mm-ss}.txt` in the `CoronaNumbers` folder containing the extracted statistics.

## Requirements

- UiPath Studio 24.10 or later.
- Dependencies:
  - UiPath.System.Activities
  - UiPath.UIAutomation.Activities

## How to Run

1. Open [Main.xaml](Project/ExtractCoronaNumbersToText/Main.xaml) in UiPath Studio.
2. Run the workflow.
3. Enter the desired country name when prompted.
4. The automation will extract the data and save it to a Notepad file.

## File Structure

- [Main.xaml](Project/ExtractCoronaNumbersToText/Main.xaml): Main workflow.
- [ClassicWorkFlow.xaml](Project/ExtractCoronaNumbersToText/ClassicWorkFlow.xaml): Classic implementation.
- [ModernWorkFlow.xaml](Project/ExtractCoronaNumbersToText/ModernWorkFlow.xaml): Modern implementation.
- `CoronaNumbers/`: Output folder for saved files.

## Notes

- Selectors are dynamic and use the country name for navigation and extraction.
- Font formatting is applied in Notepad for
