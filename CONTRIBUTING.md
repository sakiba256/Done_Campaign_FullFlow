# How to Contribute?
To execute this project, please follow the instructions provided in the README.md file. Ensure that all required files and test cases are included in the project before execution.

This framework is designed using the **Page Object Model (POM)** approach, making all functions reusable. There is no need to write separate scripts for login or other common functionalities, as these can be accessed by simply calling the existing functions.

# Implementing New Functionalities and Test Cases
  1. For any newly created function, invoke it from main.spec.js to execute it accordingly.

  2. To include test results in the report, use this.report.logResult(). Additionally, screenshots can be captured and incorporated into the report for better documentation.

  3. If new test cases need to be added, create a corresponding function and call it from the main function to ensure efficient reuse of existing functionalities.

# Framework Structure
  All test cases are organized within the Support folder, as per the framework’s design.
  New test cases should also be added to the Support folder to maintain consistency.
  This structured approach ensures modularity, reusability, and maintainability, streamlining test execution 
  and reporting.
