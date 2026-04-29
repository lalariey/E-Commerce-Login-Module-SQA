Assignment No. 2
Test Plan and Test Case Writing


Project Module:   E-Commerce Website Login Module












Muhammad Bilal Ansari 

1.	Project Overview
2.	Learning Objectives
3.	User Story & Use Case
4.	Test Plan
5.	Detailed Test Cases
6.	Test Case Classification
7.	Test Execution Results
8.	Execution Summary Report
9.	Test Suite Maintenance
10.	Tools and Technologies Used
 

This assignment focuses on the fundamental practices of Software Quality Assurance (SQA) by creating a comprehensive test suite for an E-Commerce Website's Login Module.  The project involves analyzing user requirements, refining them into user stories, and developing a structured Test Plan.
 The primary goal is to ensure the security, usability, and reliability of the authentication process.  We will manage the lifecycle of test cases, from initial writing to execution and reporting, with the Testworthy management tool. This project simulates a real-world QA environment where thorough documentation is key to software success.





2.	Learning Objectives


By completing this project, the following competencies have been developed:
 • Ability to write effective, clear, and concise test cases for web applications.
 • Recognizing the components and structure of a professional Test Plan. •	Mastery of test case management, execution, and reporting using Testworthy.
• Proficiency in classifying test cases into Regression, Smoke, Negative, and Automation categories.
• Knowledge of creating and evaluating Execution Summary Reports for the purpose of displaying the state of software quality 

3.1	User Story

Title: User Authentication for E-Commerce Platform

Statement: As a registered customer, I want to securely log into my account using my email and password so that I can access my profile, view order history, and make purchases.
Acceptance Criteria:

•	System allows login with a valid registered email and password.
•	System displays error messages for invalid or empty credentials.
•	Users can reset their password via the "Forgot Password" link.
•	Users can securely log out to end their session.

3.2	Use Case

Use Case Name	User Login
Actor	Registered Customer
Preconditions	User has a registered account and is on the login page.
Primary Flow	1. User enters Email. 2. User enters Password. 3. User clicks Login. 4. System validates. 5. Redirects to Dashboard.
Post-condition	User gains access to their personal account dashboard.

4.	Test Plan


Introduction: The procedure for testing the E-Commerce application's Login Module is outlined in this Test Plan. It defines the scope, approach, and resources required. 
Scope of Testing:

 • Functional testing of the login form (Email, Password, Buttons).

 • Testing for input field validation •	Navigation testing (Forgot Password and Logout).

 Test Strategy:

 • Black Box Testing: Concentrating solely on the inputs and outputs without examining the internal code • Manual Testing: In Testworthy, the initial execution will be carried out manually. 

Below are the 10 professional test cases designed for the Login Module.

ID	Test Scenario	Steps	Expected Result	Status
TC-01	Valid Login	1.	Enter valid email
2.	Enter valid password
3.	Click Login	User is redirected to the Dashboard.	Pass
TC-02	Invalid Password	1.	Enter valid email
2.	Enter incorrect password
3.	Click Login	Error: "Invalid email or password."	Pass
TC-03	Unregistered Email	1.	Enter unregistered email
2.	Enter any password
3.	Click Login	Error: "Account does not exist."	Pass
TC-04	Empty Fields	1.	Leave both fields empty
2.	Click Login	Prompt: "Please fill in this field."	Pass
TC-05	Forgot Password Link	1.	Click "Forgot Password"	Redirected to Password Reset page.	Pass
TC-06	Password Masking	1.	Enter characters in password field	Characters are shown as dots/asterisks.	Pass
TC-07	Invalid Email Format	1.	Enter "user@invalid"
2.	Click Login	Validation error for incorrect email format.	Pass
TC-08	Logout Functionality	1.	Log in
2.	Click Logout button	Session ends, redirected to Login page.	Pass
TC-09	SQL Injection Attempt	1.	Enter ' OR '1'='1 in email field
2.	Click Login	Access denied; error message shown.	Pass
TC-10	Session Persistence	1.	Log in
2.	Close browser tab
3.	Re-open site	User should remain logged in (if 'Remember Me' is on).	Fail
 

To optimize testing cycles, test cases are classified into the following categories:

6.1	Smoke Testing

Focuses on core functionality. Includes: TC-01 (Valid Login) and TC-08 (Logout).

6.2	Regression Testing

Ensures updates haven't broken existing features. Includes: All test cases (TC-01 to TC-10).

6.3	Negative Testing

Ensures the system handles errors gracefully. Includes: TC-02, TC-03, TC-04, TC-07, and TC-09.

6.4	Automation Testing

Highly repetitive cases suitable for automation scripts. Includes: TC-01, TC-02, and TC-04.


7.	Test Execution Results

Execution was carried out on Testworthy. Below is the breakdown of the execution cycle for Build v1.0.

Metric	Details
Total Test Cases	10
Total Passed	9
Total Failed	1
Total Blocked	0
Pass Percentage	90%
 

 

With a pass rate of 90%, the Login Module testing for Build v1.0 is mostly successful. Observation: TC-10 failed as the session was cleared immediately after the tab was closed, despite the "Remember Me" checkbox being selected.  For session persistence, developers should investigate the cookie expiration settings. Aside from this minor issue, the module is stable for release.
 As the E-Commerce platform evolves, the test suite will be maintained by:
 •	Updating test data when user database schemas change.
 •	Adding new test cases for Multi-Factor Authentication (MFA) in future builds.
 •	Retiring obsolete test cases that no longer apply to the UI design.

10.	Tools and Technologies Used


•	Testworthy: Used for creating test plans, writing test cases, tracking execution, and generating reports.
•	Google Chrome: Browser platform for execution.

11.	Submission Requirements

As per the assignment instructions, the following items are provided in the submission portal:

•	Testworthy Link: [Link to the public test project]
•	PDF Report: This comprehensive documentation including Test Plan and Cases.
•	Execution Evidence: Screenshots of the Testworthy dashboard showing 90% completion.

12.	Screenshots

     
