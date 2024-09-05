# Pages Directory

## Overview
This directory follows the Page Object Model (POM) design pattern. Each `.robot` file within this directory represents a specific page or component of the application under test. The purpose of using the POM is to encapsulate the elements and interactions of a web page, making the test cases more modular, maintainable, and reusable.

## Directory Structure
- **`home_page.robot`**: Contains the page object for the Home page of the application.
- **`login_page.robot`**: Contains the page object for the Login page of the application.

## Best Practices
- Define all locators and page-specific keywords within these files.
- Keep your page objects as clean and concise as possible to ensure maintainability.
- Reuse page objects across different test cases to avoid duplication of code.

## Example Usage
In your test cases, you can import and use these page objects as follows:

```robot
*** Settings ***
Resource    src/pages/home_page.robot
Resource    src/pages/login_page.robot

*** Test Cases ***
Login to Application
    Open Browser    ${URL}    chrome
    Input Username    ${USERNAME}
    Input Password    ${PASSWORD}
    Click Login Button
    [Teardown]    Close Browser
