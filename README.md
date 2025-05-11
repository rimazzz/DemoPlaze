# **Demoblaze**

Automated testing framework for LiteCart, utilizing Selenium, Postman, and JMeter to validate UI interactions, core functionalities, payment processing, and overall system performance on web application (https://www.demoblaze.com/) . Covers end-to-end testing, including add-to-cart workflows, checkout validation, API response verification, and load testing to ensure a seamless user experience, platform stability, and high reliability under varying traffic conditions. 🚀

## 🏗️ **Project Structure**

This project is structured to support scalable and maintainable test automation. Here's a quick breakdown of the folder structure:

```plaintext
LiteCartTestingSuite/  
│── 📜 README.md                # Project documentation & setup instructions  
│── 📜 LICENSE                  # MIT License details  
│── 📜 .gitignore                # Ignoring unnecessary files  
│  
├── 📂 config/                   # Configuration files  
│   ├── config.yaml              # Environment settings (URLs, credentials, timeouts)  
│   ├── test_data.json           # Sample test data for automation  
│  
├── 📂 tests/                    # Test cases for different categories  
│   ├── 📂 ui_tests/              # Selenium-based UI test cases  
│   │   ├── test_cart.py         # Add-to-cart functionality  
│   │   ├── test_checkout.py     # Checkout and payment validation  
│   │   ├── test_login.py        # User authentication tests  
│   │   ├── test_navigation.py   # Category & product navigation  
│   │  
│   ├── 📂 api_tests/             # Postman/Newman API test cases  
│   │   ├── cart_api_tests.json  # API tests for cart management  
│   │   ├── user_api_tests.json  # API tests for login/registration  
│   │   ├── payment_api_tests.json  # Payment processing tests  
│   │  
│   ├── 📂 performance_tests/     # JMeter/Gatling test scripts  
│   │   ├── litecart_load_test.jmx   # Load & stress testing script  
│   │   ├── checkout_performance.jmx  # Checkout performance testing  
│  
├── 📂 framework/                 # Core testing framework components  
│   ├── 📂 base/                  # Base classes for test automation  
│   │   ├── base_test.py          # Parent class for UI test cases  
│   │   ├── base_api_test.py      # Parent class for API tests  
│   │  
│   ├── 📂 pages/                 # Page Object Model (POM) classes  
│   │   ├── login_page.py         # Login page elements & actions  
│   │   ├── cart_page.py          # Cart page elements & actions  
│   │   ├── checkout_page.py      # Checkout & payment flow  
│  
├── 📂 reports/                   # Test execution reports  
│   ├── ui_test_report.html       # UI test execution summary  
│   ├── api_test_report.html      # API response validation results  
│   ├── performance_results.csv   # Load test results & analysis  
│  
├── 📂 logs/                      # Log files for debugging  
│   ├── test_execution.log        # General execution logs  
│   ├── error_logs.log            # Captured errors & failures  
│  
├── 📂 ci_cd/                     # Continuous integration setup  
│   ├── Jenkinsfile               # Jenkins pipeline script  
│   ├── github_actions.yml        # GitHub Actions workflow  
│  
├── 📂 docs/                      # Project documentation  
│   ├── test_plan.md              # Detailed test plan  
│   ├── bug_tracking_guide.md     # How to log issues in Jira  
│   ├── best_practices.md         # Coding & testing best practices  
│  
├── requirements.txt              # Python dependencies (if using Python)  
├── pom.xml                       # Maven dependencies (if using Java)  

```

## ✨ **Key Features**

### **1. UI Automation with Selenium** 🔍
Automates testing of navigation, add-to-cart, checkout, and payment workflows to ensure a seamless shopping experience including :
- Validates navigation, add-to-cart, checkout, and payment workflows.
- Ensures cross-browser compatibility and responsive design testing.
- Uses Page Object Model (POM) for structured and maintainable test scripts.
- 
### **2. API Testing with Postman & Newman** 🌐
Automates API validation for key functionalities like user authentication, product management, cart operations, and order processing including :
- Automates API validation for user authentication, product management, and order processing.
- Ensures API responses follow expected status codes, response times, and data integrity.
- Runs tests in Postman and via CLI using Newman for seamless automation.

### **3. Performance & Load Testing with JMeter/Gatling** 🚀
Simulates high-traffic conditions to test LiteCart’s stability and responsiveness including :
- Simulates high-traffic scenarios to test LiteCart's scalability & reliability.
- Analyzes response times, server load capacity, and potential bottlenecks.
- Ensures checkout and payment processing remain stable under heavy usage.

### **4. Test Reporting & Logging** 📊
Generates detailed test reports (HTML, JSON) to provide insights into test execution and results including :
- HTML & JSON-based reports for detailed execution summaries.
- JIRA integration for real-time bug tracking and issue management.
- Centralized logs for debugging UI, API, and performance test failures.

### **5.  CI/CD Integration for Continuous Testing** 🤖
Automates test execution with Jenkins & GitHub Actions, ensuring tests run automatically on every code change including :
- Automated test execution via Jenkins & GitHub Actions.
- Ensures every code update is tested before deployment.
- Streamlines test execution, reporting, and debugging in real-time.

### **6.  Well-Structured & Scalable Test Framework** 📂
Follows a modular test structure, making it easy to expand and maintain including :
- Organized project structure separating UI, API, and performance tests.
- Modular & reusable test scripts for better maintainability.
- Uses configurable test data to support multiple environments.

## 🚀 **Getting Started**

### **Prerequisites** :

Before setting up and running the LiteCart Automated Testing Suite, ensure you have the following dependencies and tools installed:

#### 1. **Development & Testing Environment :** 
- Operating System: Windows, macOS, or Linux
- Python 3.8+ (if using Python for Selenium & API testing)
- Java 8+ (if using Java-based Selenium scripts)

#### 2. **Automation & Testing Tools :**
- Selenium WebDriver – For automating UI tests
- Postman & Newman CLI – For API testing and automation
- JMeter or Gatling – For performance and load testing

#### 3. **Package & Dependency Management :** 
- pip (for Python) or Maven/Gradle (for Java) – To manage required libraries
- pytest, unittest, or TestNG/JUnit – For test case execution and reporting

#### 4. **CI/CD & Bug Tracking :** 
- JIRA – For bug tracking and test management
- Jenkins or GitHub Actions – For continuous integration & automated test execution

#### 5. **Browser & Web Drivers :**
- Google Chrome / Mozilla Firefox – Supported browsers for UI testing
- ChromeDriver / GeckoDriver – Required WebDriver for Selenium automation

Once these prerequisites are set up, you can proceed with configuring and executing the LiteCart
### Installation Steps:

1. **Clone the Repository**:
- First, download the project files from GitHub:
   ```bash
    git clone https://github.com/YourRepo/LiteCartTestingSuite.git  
    cd LiteCartTestingSuite  
   ```
   
2. **Install dependencies**:
  - Install the required libraries based on your testing framework:
   ```bash
   pip install -r requirements.txt  
   ```
  -  For Java-based setup (Maven users)
 ```bash
   mvn install  
   ```
-  For Java-based setup (Gradle users) :
 ```bash
   gradle build  
   ```
3. **Configure Your Environment**:
   - Modify the configuration files to match your testing environment:
      - Open `config/config.yaml`  (or `config.properties`) and update:
          - Browser settings (Chrome, Firefox, Edge, etc.)
          -API base URLs
          - Login credentials (if applicable)
          - Timeout settings

4. **Run the Tests**:
- 🔍 UI & Functional Tests (Selenium-based)
    - Run all UI test cases:
   ```bash
     pytest tests/ui_tests/   # For Python  
     mvn test -Dtest=YourTestClass  # For Java (TestNG/JUnit)  
     ```
- 🌐 API Tests (Postman & Newman) :
      - Run Postman API tests using Newman CLI:
   ```bash
     pytest tests/ui_tests/   # For Python  
     mvn test -Dtest=YourTestClass  # For Java (TestNG/JUnit)  
     ```
- 🚀 Performance Tests (JMeter/Gatling)
   - Run JMeter test cases:
       ```bash
      jmeter -n -t tests/performance_tests/litecart_load_test.jmx -l results.jtl  
     ```
  - Run Gatling performance tests (if using Java):
       ```bash
      mvn gatling:test  
     ```
5. **Generate Test Reports**:
-  HTML Reports for UI & API tests:
   ```bash
     HTML Reports for UI & API tests:
     ```
-  JMeter Performance Reports:
   ```bash
    jmeter -g results.jtl -o reports/performance/  
     ```
6. **CI/CD Integration (Optional but Recommended)**:
- For Jenkins: Add the `Jenkinsfile` to your pipeline.
- For GitHub Actions: Ensure the `github/workflows` folder has a valid YAML configuration.

#### ✅ Setup Complete!
Now you can run automated tests on Demoplaze to validate UI, API, and performance, ensuring a smooth and reliable shopping experience! 🛒🚀✅
       
### 🚨 **Reports for LiteCart Automated Testing Suite**:
The Demoplaze Automated Testing Suite generates various reports to track test execution, identify failures, and analyze system performance. These reports help maintain the stability, reliability, and efficiency of the platform.

## 🌟 **Visual Features**

### 1. **UI & Functional Test Reports (Selenium + TestNG/JUnit)** 📊
- Location: `reports/ui_test_report.html`
- Generated by: TestNG, JUnit, or Pytest
- Includes:
   - ✅ Test case execution results (Pass/Fail)
   - ✅ Screenshots of failed test cases
   - ✅ Time taken per test case
   - ✅ Error messages & stack traces for debugging
- Generate UI Test Reports:
   ```bash
      pytest --html=reports/ui_test_report.html  # Python-based
      mvn surefire-report:report  # Java-based (TestNG/JUnit)
     ```
  
### 2. **API Testing Reports (Postman + Newman)** 🌐
- Location: `reports/api_test_report.json` (or `reports/api_test_report.html`)
- Generated by: Newman CLI
- Includes:
   - ✅ API request & response details
   - ✅ Status codes & validation results
   - ✅ Response time analysis
- Generate API Test Reports:
   ```bash
      newman run tests/api_tests/litecart_api.postman_collection.json -r html,json --reporter-html-export reports/api_test_report.html
     ```
### 3. **Performance Test Reports (JMeter + Gatling)** 🚀
- Location: `reports/performance/` 
- Generated by: JMeter & Gatling
- Includes:
   - ✅ Response time, throughput, and error rates
   - ✅ Load & stress test results
   - ✅ Graphical analysis of system performance
- Generate Performance Reports (JMeter):
   ```bash
    jmeter -g results.jtl -o reports/performance/
     ```
- Generate Performance Reports (Gatling):
   ```bash
    mvn gatling:test
     ```
   ### 4. **Bug Tracking & Logging Reports** 🐞
- Location: `logs/test_execution.log` & Jira issues 
- Generated by: Selenium, API tests, and performance logs
- Includes:
   - ✅ Logged test execution details
   - ✅ Errors & stack traces for failures
   - ✅ Jira tickets for critical issues
     
### 📌 **Summary of Reports**
   - 📂  `reports/ui_test_report.html`– UI & functional test results ✅ 
   - 📂 `reports/api_test_report.html` – API validation results 🌐
   - 📂 `reports/performance/` – JMeter/Gatling performance reports 📈
   - 📂 `logs/test_execution.log` – Debugging & failure logs 🐞
     
## 💡 **Contributing to LiteCart Automated Testing Suite**
We welcome contributions! 🎉 Whether you're improving test cases, fixing bugs, or optimizing performance, your help makes this project better. Follow these steps to get started:

##  How to Contribute 🚀 :
- **1. Fork the Repository**
    - Click the Fork button at the top of this repo to create your own copy.
   
- **2. Clone Your Fork**
    ```bash
    git clone https://github.com/YourUsername/DemoplazeTestingSuite.git  
    cd LiteCartTestingSuite  
     ```
- **3. Create a New Branch**
    ```bash
    git checkout -b feature/your-feature-name   
     ```
- **4. Make Your Changes**
   - Add new test cases (UI, API, or performance).
   - Fix bugs or improve test automation.
   - Optimize existing test scripts.

- **5. Test Your Changes**
    ```bash
    pytest tests/  # Run all UI tests (Python)  
    mvn test  # Run all UI/API tests (Java)  
    jmeter -n -t tests/performance_tests/load_test.jmx -l results.jtl  # Run performance tests   
     ```

- **6. Commit Your Changes**
    ```bash
    git add .  
    git commit -m "Added new test for checkout functionality"  
    git push origin feature/your-feature-name    
     ```

- **7. Submit a Pull Request (PR)**
   - Go to GitHub and open a Pull Request against the `main` branch.
   - Add a clear description of your changes and improvements.
 
  ## 📌 Contribution Guidelines
- ✅ Follow best coding practices and maintain clear, structured test scripts.
- ✅ Write descriptive commit messages for better version control.
- ✅ Include test cases for any new features you add.
- ✅ Ensure all tests pass before submitting a PR.
- ✅ Log any issues in JIRA for better tracking.


    
## 📄 **License**

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

## 📞 **Contact Information**

For any questions or suggestions, feel free to reach out:

- **GitHub Issues**: Open an issue [here](https://github.com/Ezz-Kamel/E-Commerce-Site/issues)
- **Email**:ezz01143394446@gmail.com 📧

## 🧑‍🤝‍🧑 **Meet the Team**

This project is the result of collaborative work by an amazing team! 👏

- **Ezz Kamel**  
  📧 ezz01143394446@gmail.com

- **Abdulrahman Nageh**  
  📧 abdulrahman.nageh6071@gmail.com
  
- **Mohamed Ahmed Sayed**  
  📧 mo891828@gmail.com 

- **Rimaz Farhan**  
  📧 rimazfarhan@gmail.com 

- **Mohamed ahmed Mohamed Gaber**  
  📧 meshogaber1056@gmail.com

- **Mariam Ashraf**  
  📧 mariam2052003@gmail.com

---

## 🎉 **Enjoy Testing!** 🧑‍💻

This framework is built to make testing the LiteCart Shopping Demo more efficient, reliable, and seamless. With automated UI, API, and performance testing, we ensure a smooth shopping experience for all users. We hope you find it as valuable as we do! 🚀🛒✅

---
