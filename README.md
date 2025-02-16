This script enables users to create and configure Drone Campaigns according to their specific requirements efficiently.

The automation is implemented using **Playwright with JavaScript** to streamline the campaign creation process. Additionally, a custom HTML report is integrated to provide clear and structured test execution results.

# Drone_Campaign_RTCMS
Full Automation Steps in RT CMS UI:
 1. Login to RT CMS portal
 2. Go to Audience Builder, create and submit audience
 3. Go to Drone Admin Tab, create all combinations with created Audience ID and validate existing combinations
 4. Go to Drone Campaign Tab, create required campaigns and validating after submit the campaign
 5. Stopped the newly created Campaigns

**N.B** The automation script is unable to remove the newly created Audience ID due to insufficient access permissions. As a result, users must manually input a different Audience Name in **audience.spec.js** file each time, since submitting an audience with the same name is not allowed.
    
# Key Features of the Automation Script:
 1. Implemented **Page Object Model (POM)**: Ensuring modularity and reusability of all methods.
 2. CSV-Based Input Handling: Reads input data from a **CSV file** for dynamic test execution.
 3. Generic QA Account Usage: Utilizes a predefined QA account for testing purposes.
 4. Error Handling & Screenshots: Captures **screenshots** upon errors for debugging.
 5. **Validation** Mechanism: Ensures test execution continues smoothly even in case of failures.
 6. Custom HTML Report: Generates detailed and structured test execution **reports**.

This automation is built using Playwright with JavaScript to ensure efficiency, reliability, and ease of use

# Framework Structure
 1. Test Case Management: All test cases are organized within the Support folder.
Functions are invoked from the main.spec.js file for execution.

 2. Screenshot Handling: All captured screenshots are stored in the Screenshots folder for debugging and reference.

 3. Reporting: Test execution reports are generated and stored in the main branch for accessibility and tracking.

# Playwright Configuration
 The prerequisites for Playwright are as follows:

1. Operating System:
 Windows, macOS, or Linux: Playwright is compatible with all major operating systems.

2. Node.js:
 Playwright requires Node.js version 14 or higher. Make sure Node.js is installed on your system.
 You can download it from the Node.js official website.

3. Package Manager:
 npm (comes with Node.js) or yarn to install Playwright and its dependencies.

4. Browser Dependencies:
 Playwright automatically downloads the required browser binaries (Chromium, Firefox, WebKit) during installation. No additional browser setup is typically needed.

5. Development Tools:
 A code editor like Visual Studio Code is recommended for writing and debugging scripts.
 Git for version control is optional but useful.

6. Playwright Installation:
      Run the following command to install Playwright:
     
     
      npm install playwright
      
      If you want browser dependencies as well, use:
      
      
      npx playwright install

7. Additional Libraries (Optional):
 Testing Frameworks: Playwright Test is included by default, but you can integrate it with Jest, Mocha, or other 
 testing libraries if needed.
 Environment Variables: Use a package like dotenv to manage sensitive data such as credentials.

8. System Permissions:
 Ensure your system allows Node.js and browser processes to run without restrictions.

Additionally, you will need to set your username and password in the logIn.spec.js

 For run the script with UI Mode (Headed):

      set  headless: false, // Set to false for UI mode in main.spec.js
      Command for run: node main.spec.js 
 For run in background (Headless) need to make:

      headless: true in main.spec.js
      Command to run the script: : node main.spec.js 

**N.B** RT CMS is SSO login, need to give Authenticate code to login in the CMS portal

