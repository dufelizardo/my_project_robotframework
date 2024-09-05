# Test Cases Directory

## Overview
This directory contains individual test cases written in `.robot` files. Each test case file can include multiple tests that verify specific functionalities of the application. 

## Directory Structure
- **`example_test.robot`**: A sample test case to demonstrate the structure and usage of keywords, variables, and settings.
- **`another_test.robot`**: Another sample test case to showcase additional testing scenarios.

## Best Practices
- Write test cases that are independent and can run in any order.
- Keep test cases modular and reusable.
- Use meaningful names for test cases to easily identify their purpose.
- Include proper documentation for each test case to describe its purpose and expected outcome.

## Example Usage
```robot
*** Settings ***
Resource    src/resources/locators.robot
Resource    src/keywords/page_keywords.robot

*** Test Cases ***
Verify Login Functionality
    [Documentation]    Verify that a user can log in with valid credentials
    Open Browser    ${URL}    chrome
    Login To Application    ${USERNAME}    ${PASSWORD}
    Verify Successful Login
    [Teardown]    Close Browser
