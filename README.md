# Selenium Basic Auth Tests

This repository contains automated tests for testing basic HTTP authentication using Selenium WebDriver and Python.

## Description

The test suite includes three test cases for basic authentication scenarios:
- **Correct credentials**: Tests successful login with valid username/password
- **Incorrect credentials**: Tests failed login with invalid credentials  
- **Empty credentials**: Tests behavior with empty username/password

The tests use the demo site at `https://the-internet.herokuapp.com/basic_auth` for testing basic authentication functionality.

## Prerequisites

- Python 3.7 or higher
- Chrome browser (tests use ChromeDriver)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/selenium-basic-auth-tests.git
cd selenium-basic-auth-tests
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Running the Tests

To run all tests with verbose output:
```bash
python basicauth.py
```

Or using unittest module:
```bash
python -m unittest basicauth.py -v
```

## Test Cases

### 1. `test_correct_credentials`
- **Purpose**: Verify successful authentication with correct credentials
- **Credentials**: admin/admin
- **Expected Result**: "Congratulations!" message appears

### 2. `test_incorrect_credentials` 
- **Purpose**: Verify authentication failure with wrong credentials
- **Credentials**: admin1/admin
- **Expected Result**: "Not authorized" message

### 3. `test_empty_credentials`
- **Purpose**: Verify authentication failure with empty credentials
- **Credentials**: empty username and password
- **Expected Result**: "Not authorized" message

## Dependencies

- **selenium**: Web automation framework
- **webdriver-manager**: Automatic ChromeDriver management

## Project Structure

```
selenium-basic-auth-tests/
├── basicauth.py         # Main test file
├── requirements.txt     # Python dependencies
└── README.md           # This file
```

## Notes

- Tests automatically download and manage ChromeDriver using webdriver-manager
- Each test includes a 2-second wait for page loading
- Browser window is maximized for better visibility during test execution
- Tests clean up by closing the browser after each test case