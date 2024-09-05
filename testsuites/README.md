# Test Suites Directory

## Overview
The `testsuites/` directory organizes multiple test cases into cohesive test suites. Test suites are collections of test cases that target specific functionalities or parts of the application. Organizing tests into suites helps manage larger projects and run related tests together.

## Directory Structure
- **`suite_1.robot`**: A suite of related tests, such as login tests.
- **`suite_2.robot`**: Another suite, potentially focused on a different feature or part of the application.

## Best Practices
- Group related test cases into suites for easier execution and maintenance.
- Name test suites descriptively to reflect the area of the application they cover.
- Use tags to further categorize and control the execution of test cases within suites.

## Example Usage
You can run specific test suites using the Robot Framework command line:

```bash
robot testsuites/suite_1.robot
