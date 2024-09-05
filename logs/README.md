# Log Directory

## Overview
The `log/` directory is used to store execution logs and reports generated after running tests. These logs are essential for debugging failed tests and understanding the execution flow.

## Directory Structure
- **`log.html`**: The detailed log of the test execution.
- **`report.html`**: The summary report of the test run, including the status of each test case.

## Best Practices
- Review logs after each test execution to diagnose issues or verify successful runs.
- Archive or clean up old logs periodically to manage disk space and maintain project cleanliness.
- Utilize the information in `log.html` for in-depth debugging and in `report.html` for a high-level overview of the test results.

## Example Usage
After running your tests, you can open the `log.html` and `report.html` files in a web browser to view the detailed and summary results, respectively:

```bash
robot -d log/ testsuites/suite_1.robot
