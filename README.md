# ITFlow exploratory testing

## Table of Contents
* [Test plan for ITFlow exploratory testing.](#Test-plan)
* [Test checklist.](#Test-Check)
* [Bug Reports.](#Bug-Reports)
* [Test summary report for ITFlow exploratory testing.](#Test-report)



<h1 id="Test-plan">Test plan for ITFlow exploratory testing.</h1>

### Description:
This project aims to verify the functionality and UX of the [ITFlow](https://itflow.org/) website through a combination of exploratory and manual testing. The main focus of the tests includes core user functionalities like login, registration, admin panel, ticketing, and billing. Testing will be conducted on a Windows 11 desktop machine using Google Chrome, Brave, and Internet Explorer to ensure compatibility across different browsers. Additionally, basic checks for security vulnerabilities and accessibility compliance will be included to assess overall user experience and system robustness.

### Scope of Testing:

- **Functional Testing**:
  * Verify core functionalities such as login, registration, admin panel access, ticketing, billing, client management, and data management.
  * Ensure accurate data processing.
  * Test various input combinations and edge cases.
  * Validate error handling and feedback messages.

- **Usability Testing**:
  * Evaluate the user interface design.
  * Assess the ease of navigation and workflow.
  * Identify any usability issues.
    
- **Compatibility Testing**:
  * Ensure compatibility with different browsers, operating systems, and devices.
  * Test responsiveness on various screen sizes and resolutions.
    
- **Security Testing**:
  * Identify and address potential security vulnerabilities.
  * Test authentication and authorization mechanisms.

### Testing Environment:

- **Operating System**: Windows 11 (Desktop machine)
- **Browser**: Google Chrome, Brave, Internet Explorer (IE)
  

### Test Schedule:
* **Start Date**: 10.10.2024
* **End Date**: 24.10.2024 

### Resources:

- **Manual tester**: Responsible for exploratory testing and creating test data.
- **Tools**: 
   * DevTools
   * ShareX and ScreenPal
   * BugMagnet

### Entry Criteria:
- Smoke tests are performed and the code is stable for testing.
- Test environment is set up and ready.
- Test plan is reviewed, and approved.
- Test data are designed.
  
  

### Exit Criteria:

- All tests from the check list are executed.
- All critical and major defects should be fixed or have a solution plan.
- Test coverage should be at least 80%.
- Test summary report is ready.

### Risks and Mitigations:
- **Risk**: Changes in requirements or specifications during testing.
  - **Mitigation**: Maintain constant contact with the product owner and monitor documentation changes.
- **Risk**: Lack of testers knowledge.
  - **Mitigation**: Ensure proper training and development to improve testing skills of team members.
- **Risk**: Delays in test execution.
  - **Mitigation**:  Prioritize critical test cases and conduct proper time estimation to avoid delays.

<h1 id="Test-Check">Test checklist.</h1>

**Functional**:

- Verify user login functionality.
- Test user registration process.
- Ensure proper logging and error reporting mechanisms.
- Verify password reset and recovery processes.
- Check admin panel access and functionalities.
- Verify user logout functionality.
- Validate error handling and feedback messages for incorrect inputs. 
- Validate ticket creation, updating, and closing.
- Test billing module for invoice generation and payment processing.
- Verify client management features (add, edit, delete clients).
- Test user profile management (update personal information, change password).
- Ensure data management functionalities (import/export data).
- Test various input combinations and edge cases for all forms.
- Check session management (login timeout, session persistence).
- Validate email notifications and alerts.
- Test search functionality across different modules.
- Verify file upload and download features.
- Check sorting in data tables.
- Check for any broken links or missing resources.

**Usability testing**:

- Evaluate the overall user interface design for consistency.
- Assess the visual appeal and readability of the interface.
- Assess the ease of navigation across different sections.
- Evaluate the responsiveness of the UI to user actions.
- Check RWD for different screen sizes and resolutions.
- Test the intuitiveness of the workflows.
- Check the clarity and helpfulness of on-screen instructions and tooltips.
- Test the application’s behavior with different input methods (mouse, keyboard, touch).
- Check for any distracting elements or unnecessary animations.
- Test the application’s onboarding process for new users.
- Evaluate the application’s help and support features (FAQs, contact support).

 **Accessibility**:
 - Test screen reader compatibility.
 - Test voice commands for navigation and interaction
 - Avoid using color as the sole method of conveying information.
 - Check if objects are cleary
 - Check transcripts, or audio descriptions for all sound and video content.
 - Ensure that all form fields have associated labels.

 **Security**:
 
 - Ensure all user inputs are validated on both client and server sides.
 - Ensure proper permission checks for all sensitive actions.
 - Check session timeout and inactivity logout.
 - Chek proper data encyption.
 - Ensure no sensitive information is exposed in error messages.
 - Test strong password policies (minimum length, complexity requirements).
 
 







<h1 id="Bug-Reports">Bug Reports.</h1>

<h2 id="Bug-Reports">1. Admin can't log out.</h2>

**Description**: When an admin attempts to log out of the application they are redirected to an empty page. It is possible to navigate back to the previous page using the browser's back button.

**Steps to Reproduce**:
- Navigate to the admin login page.
- Enter correct credentials and log in.
- Open the right-top panel and click on the "Logout" button.

**Expected Result**: The user should be successfully logged out and redirected to the login page or a designated logout page.

**Actual Result**: The user is redirected to an empty page and can navigate back to the previous page using the browser's back button.

**Priority**: High

**Browser Compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Internet Explorer.

https://github.com/user-attachments/assets/5c75dfc1-7717-4695-90b8-15c5a484e938



<h2 id="Bug-Reports">2. User can add new vendor with empty name (spacebar).</h2>

**Description**: A user is able to create a new vendor with only a spacebar as the name, bypassing the required field validation.

**Preconditions**: User is logged in with active account.

**Steps to Reproduce**:
- Navigate to the vendor management section.
- Click the "Add New Vendor" button.
- Enter a spacebar in the vendor name field.
- Leave other required fields blank.
- Click the "Create" button.

**Expected Result**: The system should display an error message indicating that the vendor name is required and cannot be empty. The user should not be able to proceed with the vendor creation process.

**Actual Result**: The user is allowed to create the vendor with an empty name, potentially leading to data inconsistencies and errors in subsequent operations.

**Priority**: Medium

**Browser Compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Internet Explorer.


https://github.com/user-attachments/assets/cbf8d4ad-607f-4360-892b-e48f037ad012



<h2 id="Bug-Reports">3. Missing option to directly add assets when creating new recurring ticket.</h2>

**Description**: When creating a new recurring ticket, there is no direct option to add assets immediately. Users have to create the ticket first and then go back to edit it to add assets.

**Preconditions**: User is logged in with active account.

**Steps to Reproduce**:
- Navigate to the recurring ticket section.
- Click the "Add New Recurring Ticket" button.
- Enter a spacebar in the vendor name field.
- Fill in the required fields.
- Select "Assets" tab.
  

**Expected Result**: There should be an option to add assets directly when creating the recurring ticket, just like there is one in edit options.

**Actual Result**: Assets tab have blank white space with missing dropdown menu.



**Priority**: Medium

**Browser Compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Internet Explorer.


https://github.com/user-attachments/assets/8fca0542-e4dc-438f-80cf-58da8641444d

<h2 id="Bug-Reports">4. Importing new client without providing any files leads to HTTP error 500.</h2>

**Description**: When attempting to import a new client without providing any associated files, the system returns an HTTP Error 500. 

**Preconditions**: User is logged in with active account.

**Steps to Reproduce**:
- Navigate to the client section.
- On the "Add New" click dropdown arrow and select "Import"
- Without adding any files click "Import" button

  

**Expected Result**: The system should display an error message indicating that at least one file is required for client import. The user should not be able to proceed with the import process.

**Actual Result**: An HTTP error 500 is returned.



https://github.com/user-attachments/assets/7d2d589c-9e23-4c47-a51b-e542efea6064



**Priority**: Medium

**Browser Compatibility**: This issue has been observed in all tested browsers: Google Chrome, Brave, and Internet Explorer.

<h1 id="Test-report">Test summary report for ITFlow exploratory testing.</h2>

## Test Summary Report
1. **Descripton**: 
2. **Test Period**:
3. **Test Coverage** : 
4. **Test Execution Summary:** 

5. **Key Findings**:



6. **Recommendations**:


7. **List of reported bugs:**
   
