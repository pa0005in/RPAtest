# Cost Tool Data Extraction Automation:
  
## Description:
This UIPath automation was created to automate data extraction of an online cost estimation tool.  
The extracted data will then be analyzed to determine the coefficients of the different variables.  
In order to do so, a large number of data points must be collected from the cost estimation tool.  
  
## Scripts  
__Main.xaml__  
This is the main script that contains the automation programming.  
This is the file to be opened in UIPath studio to run the automation.  
  
## Requirements
This script was programmed using UIPath Studio 2022.10.13 edition.  
However, it should still work with newer versions of UIPath.  
  
__Web browser__  
This script was programmed with chrome browser as the base, therefore chrome browser must be installed in order for the tool to run.  
  
## Features
### Automated Data Extraction
The data extracted from the estimator consists of multiple parts:  
__Table of Data__  
The data centre cost summary is extracted as a table and stored within a single Excel sheet.  
As the redundancy level options are adjusted, the new data point is extracted as another column to be added to the summary excel sheet.  

__Screenshot of Cost Breakdown__  
Within the cost estimator, there is use of pie chart to display the breakdown of the cost in different categories:  
(1) Type, (2) System, (3) Power, (4) Cooling and (5) Others  
The automation script will take a screenshot of the respective pie charts for data extraction and cycle through the pie chart options if required.  

__Auto generation of storage folders__  
As the script is running, a folder will be generated for each redundancy option to keep the data separate.  
This keeps the final folder neat and tidy, easy for user to reference the extracted data if necessary.  

### Redundancy Level Options
The current script cycles through all redundancy options for power while keeping cooling at N level, while also cycles through all redundancy options for cooling while keeping power at N level.  
All other options available to cost estimator is kept constant throughout the automation.  

## Current Issues/Future Roadmap
__1) Piechart information can only be extracted manually.__  
  Incorporating API of image reading AI tool can be considered.  
  Have to consider the AI tool's ability to recognize numbers if they overlap with one another.  

## Acknowledgements  
This idea of the script was provided by my colleague from my intern company.  
Thanking Professor Michael for teaching us how to use UIPath.
I am grateful to Gerald, Henry and Bryan for their contributions in this project; their contributions helped to move this project along quickly and complete it on time.
