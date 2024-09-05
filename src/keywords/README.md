
# Keywords Directory

## Overview
The `keywords/` directory is where user-defined keywords are stored. Keywords are reusable actions or sequences of actions that can be used across multiple test cases. This promotes reusability and cleaner test scripts.

## Directory Structure
- **`page_keywords.robot`**: Contains keywords specific to page interactions, combining multiple actions into single reusable steps.

## Best Practices
- Group keywords logically by functionality (e.g., page-specific, validation-related).
- Make your keywords as atomic as possible (perform one specific action) to maximize reuse.
- Document keywords clearly, explaining what each keyword does and how it should be used.

## Example Usage
You can use the keywords defined in this directory as follows:

```robot
*** Settings ***
Resource    src/keywords/page_keywords.robot

*** Test Cases ***
User Can Log In
    [Documentation]    Test case using custom keywords for login
    Open Browser    ${URL}    chrome
    Login To Application
    Verify Successful Login
    [Teardown]    Close Browser
