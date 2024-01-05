<div align="center">
  <h1>QA Tester Portfolio 👨‍💻</h1>
    <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/95b83f22-112f-463c-a577-d654d0677b8f" width=""> </a> 
</div>

----

### Quick access index

- [About Me](#about-me)
- [Projects](#projects)
  - [API Test](#api-test)
    - [POSTMAN](#basic-api-test-with-postman)
    - [Karate Framework](#api-test-with-karate-junit5-framework)
  - [Web Automation](#web-automation)
    - [Basic Assertion](#basic-test-case-assertion)

## About me

Hello there! 👋,

With three years of experience in merchandise operations, my primary focus has revolved around refining pricing strategies, accurate stock forecasting, and delivering comprehensive sales performance insights to suppliers. Nevertheless, I've always been naturally curious and have a strong desire to learn about technology and IT 👨‍💻.

I’ve recently embarked on a Quality Assurance Engineer mini boot camp where I learned to create detailed test cases, delved into basic programming in Java, and learned tools like Postman for API testing and Katalon for automation.

Transitioning into the realm of Quality Assurance excites me tremendously. I'm eager to apply these newfound skills and leverage my knowledge for a fulfilling career launch in this field. 🚀"

<h3 align="left">Languages and Tools:</h3>
  <p align="left"> 
      <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/24ddbcfd-fa53-4f3a-8b08-c4716ea30d86" alt="linux" width="50" height="50"/> </a> 
      <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="45" height="45"/> </a> 
      <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="50" height="50"/> </a>
      <a href="https://postman.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="postman" width="44" height="44"/> </a> 
      <a href="https://www.karatelabs.io/"> <img src="https://github.com/dannyhdyt/Katalon-Web-Automation-Assignment/assets/153344198/e2afc8e6-a168-43bd-8feb-c8ab70673b28" alt="Karate" width="50" height="50"/> </a> 
      <a href="https://www.selenium.dev" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/detain/svg-logos/780f25886640cef088af994181646db2f6b1a3f8/svg/selenium-logo.svg" alt="selenium" width="43" height="43"/> </a>  
      <a href="https://testng.org/doc/"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/8426927a-f787-459c-b99d-4e62a9ca1766" height="50"/></a>
  </p>

## Projects

### API Test

#### Basic API Test With POSTMAN

<a href="https://www.postman.com//"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c2/Postman_%28software%29.png" height="90"/></a>

In this project, our task was to develop an API test case encompassing the `POST` / `GET` / `DELETE` methods. Additionally, for the demonstration, I utilized the [Swagger Petstore](https://petstore.swagger.io/) within the **user** section.

  * `POST` : in this example, I'm sending a JSON body that contains the details of the new user and expect a response body and a `200 OK` response status code
    
    ![Screenshot_1](https://github.com/dannyhdyt/Portfolio/assets/153344198/fbdd3de8-c9a2-4d64-9b52-f4caf8bf2816)

  * `GET` : This method is to retrieves information or a resource from a server. 
    
    ![Screenshot_2](https://github.com/dannyhdyt/Portfolio/assets/153344198/0bd3ca4c-ee68-42b0-91d5-07ac1aae1290)

  * `DELETE` : This method is to Deletes a resource on the server. The request parameters are included in the URL. 

    ![Screenshot_3](https://github.com/dannyhdyt/Portfolio/assets/153344198/375ba6d7-820a-4253-bb4c-a7076feaa429)

This is an example test case to document and track API test results on a spreadsheet.

  * [Spreadsheet](https://docs.google.com/spreadsheets/d/1eLpPjI_5D1IEdw49UsH8nHmyad2dv57cKC8NnoGjQe8/edit?usp=sharing) API Test example
  * [Postman Workspaces](https://www.postman.com/mission-administrator-38568381/workspace/tugas-api-testing/request/31739919-7e18883c-7131-41bb-bb3a-7f6621a409c6)

#### API Test with Karate-JUnit5 Framework

<p align="left"> 
  <a href="https://github.com/karatelabs/karate"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/f876d1b9-49ab-455e-acdc-e3974bfcc4e4" alt="karate" height="80"/></a>
  <a href="https://junit.org/junit5/"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/2782ef17-338c-407f-b948-218e83d17cde" height="80"/></a>
</p>

Our task was to develop an API automation script utilizing the `POST` / `GET` / `DELETE` methods. For writing tests, we employed `Java` programming language and the `Karate-JUnit5` Framework. Karate, an open-source test automation tool, facilitates tests authored in the Behaviour Driven Development (BDD) style. In our demonstration, we interact with the [Swagger Petstore](https://petstore.swagger.io/) within the **user** section. Here is an example script: 

```Gherkin
Feature: User List

  Background: Setup
    Given url baseURL
    And print "--Create User Data--"

  Scenario: Create User With List
    * def body =
    """
    {
        "id": 100,
        "username": "blackout123",
        "firstName": "blackout",
        "lastName": "decepticon",
        "email": "blackout@gmail.com",
        "password": "password123",
        "phone": "080989999",
        "userStatus": 1
    }
    """
    * def header = {Accept: 'application/json'}

    When path "/user/createWithList"
    And request body
    And headers header
    And method post
    Then status 200
    And print response
    And match response == {code:200, type:'unknown', message:'ok'}
```

Behaviour-Driven Development (BDD) is a software development and testing approach that bridges the gap between technical and non-technical teams.

By integrating Karate with JUnit 5, we can write and execute Karate tests within the JUnit 5 framework, an example of using the JUnit Runner and `.html` reports that Karate outputs.

![l3LOnEAlvF](https://github.com/dannyhdyt/Katalon-Web-Automation-Assignment/assets/153344198/b757f029-96a4-4658-82ca-c16fd45769cd)

Feel free to explore my [repository](https://github.com/dannyhdyt/DannyHidayat-API-Automation) for more details on utilizing the Karate framework and configuring dependencies.

### Web Automation

<p align="left"> 
  <a href="https://www.selenium.dev/"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/77822598-d1b0-4dfd-bc55-c4d604a241ed" alt="selenium" height="80"/></a>
  <a href="https://testng.org/doc/"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/8426927a-f787-459c-b99d-4e62a9ca1766" height="95"/></a>
</p>

#### Basic Test Case Assertion

In this project, our objective is to create a scenario focusing on testing the login functionality of a web application. We're utilizing Selenium WebDriver and the TestNG framework for this task. To showcase the demonstration, we're interacting with [herokuapp.com](https://the-internet.herokuapp.com/login). 

The test navigates to a login page, performs login actions, and verifies the login was successful by getting the element with `xpath` then expect if the element contain a **"Secure Area"** text. Here's an example:"

```Java
@Test
public void loginTest(){
    // Open Browser
    WebDriverManager.firefoxdriver();
    driver = new FirefoxDriver();
    // open the browser fullscreen
    driver.manage().window().maximize();
    driver.get("https://the-internet.herokuapp.com/login");
    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));

    // Login
    wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("username")));
    // find element by id, name, xpath
    driver.findElement(By.id("username")).sendKeys("tomsmith");
    driver.findElement(By.name("password")).sendKeys("SuperSecretPassword!");
    driver.findElement(By.xpath("//button[@class='radius']")).click();
    // verifies the login was successful if the element contain "Secure Area" text
    String txtActualBerhasilLogin =  driver.findElement(By.xpath("//h2[contains(.,'Secure Area')]")).getText();
    String txtExpectedBerhasilLogin =  "Secure Area";
    Assert.assertEquals(txtActualBerhasilLogin, txtExpectedBerhasilLogin);
```

![IyC6N1y0Iw](https://github.com/dannyhdyt/Portfolio/assets/153344198/274d47c4-de3d-4fab-a94b-1b2370e7bc5a)

This is an example of the Negative Test Case for a failed login page, expected text that contains <br> **"Your password is invalid!"**

![failedLogin](https://github.com/dannyhdyt/Portfolio/assets/153344198/c2a79652-c61b-42af-84ab-67fd1665d2c6)

Please visit my repository for more web automation project

- **[Yopmail-Extract-Text](https://github.com/dannyhdyt/Yopmail-Extract-Text)**, This project focuses on extracting content from webpages utilizing the `<iframe>` switch..

- **[Web-Automation-Assignment](https://github.com/dannyhdyt/Web-Automation-Assignment)**, This repository is a web automation project that applies Object-Oriented Programming (OOP) principles and utilizes the TestNG framework, Maven for dependency management, and the Selenium automation tool.

## CV

Please kindly download my [CV](https://drive.google.com/file/d/1-9qC53XblKxrhgn6vHO8sZxNAeUBOTBT/view?usp=sharing) 
