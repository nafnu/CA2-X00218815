# Project Name 
CA2 Basic calculator - CI Pipeline
 ### Student:
     Nathalie Flores  

## Overview
This is a simple calculator application created in Python that supports basic arithmetic operations like addition and subtraction. This project aims to demonstrate CI practices, including automated testing and building pipelines.

## Technologies Used
- **Python**: Programming language.
- **unittest**: For testing.
- **Azure DevOps**: CI/CD pipeline.
- **GitHub**: Version control platform for source code management.

## Local Development Setup

### Prerequisites
In order to set up and run the project locally, it is neccessary:
- **Python** installed
- **Git** for version control.

### Steps to Set Up Locally
1. Clone the repository:
   ```bash
   git clone < https://github.com/nafnu/CA2-X00218815.git >
   calculator

## Application Features
- Add two numbers.
- Subtract two numbers.

This project the code was taken from:
- Reference: https://www.geeksforgeeks.org/make-simple-calculator-using-python/?ref=header_outind

## Branch Policies and Protection
- Protected main branch:
Navigate to Settings > Branches > Branch Protection Rules

- Enable:
![image](https://github.com/user-attachments/assets/bd3c3d12-6d88-4661-b6f0-ee1dd6f36296)
This rules were picked because: 
* Code quality assurance: It helps that all changes are vetted for potential issues such as bugs, security vulnerabilities, or poor code.
* Collaboration: By encouraging teamwork and knowledge sharing, you can see the contributions of other team members when suggesting improvements, pointing out bugs, or identifying best practices.
* Bug prevention: It helps to catch issues early before they are merged into the main branch.
* Compliance and accountability: In regulated industries, enforcing reviews ensures a documented approval process.

## Testing Strategy
The unittest framework is Python's built-in unit testing library, making it an ideal choice for testing a simple Python project like this calculator. It has very significant key advantages: the standard library, so there is no need for additional installations or dependencies; also automatic test discovery and easy structure/integration into the project. In this particular case also, works seamlessly with Azure DevOps to automate testing in the pipeline.

![image](https://github.com/user-attachments/assets/67060569-387c-4417-bd11-2ab3a5edc424)

With this testing framework it is possible for each test method to be executed in isolation, ensuring that the result of one test does not affect the others. The module being tested, with functions add and subtract.

- Test Class: TestCalculator is a subclass of unittest.TestCase, which provides the framework for writing test cases.
- Assertions: self.assertEqual(actual, expected) verifies that the function’s output matches the expected value.
- Running the Tests: The unittest.main() method runs all the test cases when the file is executed directly.


## CI Pipeline Implementation
Pipeline Tool: Azure DevOps
Triggers were automatic build on commits to development in the azure-pipeline.yml document from Azure DevOps. 

![image](https://github.com/user-attachments/assets/b0d1a671-b318-426b-9b28-b06c8d0d08bb)


## Troubleshooting Guide 
1. The pipeline didn't work.
![image](https://github.com/user-attachments/assets/c9d11c54-ac2f-4904-905a-83b269611025)
- Solution: Verify azure-pipelines.yml syntax. And I fill out the form at https://aka.ms/azpipelines-parallelism-request to request free parallelism for your Azure DevOps account.

2. The rule
To apply the rules, you must be a public or private organization.
![image](https://github.com/user-attachments/assets/1aeeb4a6-9810-47ef-8f74-b5a95ea3c2cd)
- Solution: I paid for the private organization. However, I didn't know how to change all the projects without disconnecting the Github pipeline from Azure DevOps. Therefore, the project preferences were changed to public, just for the main purpose of demonstrating the rules applied to the repository. 