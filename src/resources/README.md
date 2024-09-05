# Resources Directory

## Overview
The `resources/` directory is intended to store shared components such as locators, variables, and custom libraries that can be reused across different test cases. This modular approach helps in maintaining consistency and simplifies updates.

## Directory Structure
- **`locators.robot`**: Contains all the locators (e.g., XPath, CSS selectors) used across the application.
- **`custom_library.py`**: Custom Python library with functions that extend the Robot Framework's capabilities.

## Best Practices
- Keep locators organized and grouped logically (e.g., by page or component).
- Store frequently used variables or constants here for easy access across multiple test cases.
- Use custom libraries to encapsulate complex logic that is not natively supported by the Robot Framework.

## Example Usage
You can import and use the resources in your test cases like this:

```robot
*** Settings ***
Resource    src/resources/locators.robot
Library     src/resources/custom_library.py

*** Variables ***
${TIMEOUT}  10

*** Test Cases ***
Verify Page Elements
    [Documentation]    Example test case to verify elements using locators from the resources
    Wait Until Element Is Visible    ${LOCATOR}    ${TIMEOUT}
    Run Custom Function    Custom Argument
