# SaveRandomWeatherInfoToTxtFile

## Overview

This UiPath automation project extracts random weather information from a web generator and saves it to a text file.
![Automation Recording](https://github.com/amrayman999/Raya-RPA-Training/blob/master/Automation%20Developer%20Associate/Task01/AutomationRecording.gif)

## Automation Flow

1. **Open Edge Browser**  
   - Navigates to [Google](https://www.google.com).

2. **Search for Weather Generator**  
   - Types "generate random weather" in the Google search area.
   - Clicks the search button.
   - Clicks the first link in the results.

3. **Configure Weather Generator**  
   - Selects "Warm" for Climate.
   - Selects "Winter" for Season.
   - Selects "Rare" for Supernatural Weather.

4. **Generate and Extract Weather Info**  
   - Clicks the "Generate" button.
   - Extracts the main weather information and description from the result page.

5. **Save to Text File**  
   - Writes the extracted information to `WeatherInformation.txt` in the following format:
     ```
     Main Information
     {main info}
     Description
     {description}
     ```

6. **Close Browser**  
   - Kills the Edge browser process.

## Key Features

- Fully automated browser interaction using UiPath activities.
- Dynamic selection of weather parameters.
- Extraction of structured weather data.
- Output saved in a readable text file.
- Automatic browser cleanup.

## Requirements

- UiPath Studio
- Microsoft Edge browser
