# Voter Roll Download Automation Using Selenium

## Project Overview

This project automates the process of downloading voter rolls from the official Telangana Chief Electoral Officer (CEO) website using Selenium WebDriver with Java.

The automation script interacts with the website, selects the required District, Assembly Constituency, and Polling Station, and automates the voter roll download workflow.

**Website:** https://ceotserms2.telangana.gov.in/ts_erolls/rolls.aspx

## Problem Statement

Develop a Selenium automation script to download voter rolls from the Telangana CEO website based on the following inputs:

1. **District** – Select the required district.
2. **Assembly Constituency** – Select the required assembly constituency.
3. **Polling Station** – Select the required polling station.

The primary objective is to demonstrate Selenium automation skills by automating the website's user flow, handling web elements, managing test data, and validating the download process.

## Technology Stack

- **Programming Language:** Java
- **Automation Tool:** Selenium WebDriver
- **Build and Dependency Management:** Maven
- **Test Framework:** TestNG
- **Test Data Management:** Excel
- **Excel Integration:** Apache POI
- **Reporting:** Extent Reports
- **Design Pattern:** Page Object Model (POM)

## Framework Design

The project follows the **Page Object Model (POM)** design pattern to separate page interactions and locators from test logic. This improves maintainability, reusability, and readability.

### Key Features

- Automates the voter roll download workflow.
- Uses reusable page classes and utility methods.
- Reads test inputs from Excel files using Apache POI.
- Manages project dependencies through Maven.
- Uses TestNG to organize and execute test cases.
- Generates HTML execution reports using Extent Reports.
- Captures screenshots for failed test cases.
- Keeps configuration files and external test data separate from test code.

## Project Structure

```text
VoterRoll/
├── src/
│   ├── main/
│   │   └── java/
│   │       └── utilities/
│   │           └── Reusable utility classes
│   └── test/
│       └── java/
│           ├── pages/
│           │   └── Page classes and locators
│           ├── tests/
│           │   └── TestNG test classes
│           ├── base/
│           │   └── Base test class
│           └── listeners/
│               └── TestNG listeners
├── Resources/
│   ├── Test data Excel files
│   └── Configuration files
├── Screenshot/
│   └── Screenshots of failed test cases
├── TestReport/
│   └── Generated HTML reports
├── pom.xml
└── README.md
```

*Note: The structure above is illustrative. Adjust directory names to match the actual repository.*

## Automation Workflow

1. Launch the browser using Selenium WebDriver.
2. Navigate to the Telangana CEO voter rolls website.
3. Read the required District, Assembly Constituency, and Polling Station values from the Excel test data.
4. Select the corresponding values on the website.
5. Complete the required interactions to initiate the voter roll download.
6. Verify that the expected file has been downloaded successfully.
7. Capture screenshots if a test fails.
8. Generate an HTML execution report using Extent Reports.

## Test Data Management

Test inputs are maintained in Excel files and accessed using Apache POI.

| District | Assembly Constituency | Polling Station |
|---|---|---|
| Configured in Excel | Configured in Excel | Configured in Excel |

The values shown above are placeholders. Actual test data should be supplied in the Excel file based on the website's available options.

## Reporting and Failure Handling

Extent Reports provide an HTML summary of test execution, while screenshots help investigate failures.

The framework is designed to support:

- Test execution status and failure details.
- Screenshots for failed test cases.
- Reusable reporting and utility methods.
- Download verification to confirm that the expected file exists.

## Prerequisites

Ensure the following are installed and configured:

- Java JDK
- Maven
- A supported web browser
- Compatible Selenium WebDriver setup
- TestNG and required project dependencies

## How to Run

Clone the repository:

```bash
git clone https://github.com/shreyvyas/VoterRoll.git
cd VoterRoll
```

Run the TestNG tests through Maven:

```bash
mvn clean test
```

Review the generated test reports and screenshots in their configured output directories.

## Expected Outcome

The automation should successfully navigate the voter roll website, apply the specified selection criteria, initiate the download, and verify the downloaded file. Test execution results should be available through the configured reporting framework.

## Learning Objectives

This project demonstrates practical experience with:

- Selenium WebDriver automation using Java.
- Page Object Model implementation.
- Maven dependency management.
- TestNG-based test execution.
- Excel-driven test data using Apache POI.
- HTML reporting and screenshot capture.
- End-to-end UI workflow automation and download validation.
