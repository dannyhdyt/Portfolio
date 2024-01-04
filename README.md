# Portfolio

## Quick access index

- [About Me](#about-me)
- [Projects](#projects)
  - [API Test](#api-test)
    - [POSTMAN](#basic-api-test-using-postman)
    - [Karate Framework](#api-test-with-karate-framework)
  - [Web Automation](#web-automation)

## About me

I'm a merchandise operation with three years of work experience, my primary focus has been on perfecting pricing strategies, accurate stock forecasting, and providing sales performance insights to suppliers. But I'm also a curious person, with a passion for learning technology.

I’ve recently embarked on a Quality Assurance Engineer 👨‍💻 mini boot camp where I learned to create detailed test cases, delved into basic programming in Java, and learned tools like Postman for API testing and Katalon for automation.

I am enthusiastic about transitioning into the realm of Quality Assurance and excited to apply these skills. The knowledge I have gained will be very useful for building a career in this field 🚀.

<h3 align="left">Languages and Tools:</h3>
    <p align="left"> 
        <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/24ddbcfd-fa53-4f3a-8b08-c4716ea30d86" alt="linux" width="50" height="50"/> </a> 
        <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="45" height="45"/> </a> 
        <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="50" height="50"/> </a>
        <a href="https://postman.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="postman" width="44" height="44"/> </a> 
        <a href="https://www.karatelabs.io/"> <img src="https://github.com/dannyhdyt/Katalon-Web-Automation-Assignment/assets/153344198/e2afc8e6-a168-43bd-8feb-c8ab70673b28" alt="Karate" width="50" height="50"/> </a> 
        <a href="https://www.selenium.dev" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/detain/svg-logos/780f25886640cef088af994181646db2f6b1a3f8/svg/selenium-logo.svg" alt="selenium" width="43" height="43"/> </a>  
    </p>

## Projects

### API Test

#### Basic API Test Using POSTMAN

  <a href="https://www.postman.com//"><img src="https://upload.wikimedia.org/wikipedia/commons/c/c2/Postman_%28software%29.png" height="90"/></a>

  - in this project, we were assigned to create an API test case with the method `POST` / `GET` / `DELETE`, and for the demo web I'm using [Swagger Petstore](https://petstore.swagger.io/) the `user` section

    * `POST` : in this example, I'm sending a JSON body that contains the details of the new user and expect a response body and a `200 OK` response status code
      
      ![Screenshot_1](https://github.com/dannyhdyt/Portfolio/assets/153344198/fbdd3de8-c9a2-4d64-9b52-f4caf8bf2816)

    * `GET` : This method is to retrieves information or a resource from a server. 
      
      ![Screenshot_2](https://github.com/dannyhdyt/Portfolio/assets/153344198/0bd3ca4c-ee68-42b0-91d5-07ac1aae1290)

    * `DELETE` : This method is to Deletes a resource on the server. The request parameters are included in the URL. 

      ![Screenshot_3](https://github.com/dannyhdyt/Portfolio/assets/153344198/375ba6d7-820a-4253-bb4c-a7076feaa429)

  - Creating a test case for the API Test result on a spreadsheet

    * [Spreadsheet](https://docs.google.com/spreadsheets/d/1eLpPjI_5D1IEdw49UsH8nHmyad2dv57cKC8NnoGjQe8/edit?usp=sharing) API Test example
    * [Postman Workspaces](https://www.postman.com/mission-administrator-38568381/workspace/tugas-api-testing/request/31739919-7e18883c-7131-41bb-bb3a-7f6621a409c6)

#### API Test with Karate-JUnit5 Framework

<p align="left"> 
  <a href="https://github.com/karatelabs/karate"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/f876d1b9-49ab-455e-acdc-e3974bfcc4e4" alt="selenium" height="80"/></a>
  <a href="https://junit.org/junit5/"><img src="https://github.com/dannyhdyt/Portfolio/assets/153344198/2782ef17-338c-407f-b948-218e83d17cde" height="80"/></a>
</p>

- We were assigned to create an API Automation script using the method `POST` / `GET` / `DELETE`, for tests written, we use the programming language `Java` and `Karate-JUnit5` Framework, Karate is an open-source test automation tool for tests written using Behaviour Driven Development (BDD). In the demo web, we are using [Swagger Petstore](https://petstore.swagger.io/) in the `user` section. Example script:

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

Please visit my [repository](https://github.com/dannyhdyt/DannyHidayat-API-Automation) on using the Karate framework and to setup the Dependency Configuration for more details.

### Web Automation

#### 

## CV

Please kindly download my [CV](https://drive.google.com/file/d/1-9qC53XblKxrhgn6vHO8sZxNAeUBOTBT/view?usp=sharing) 
