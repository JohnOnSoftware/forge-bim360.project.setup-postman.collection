# BIM360 Project Setup Step-by-Step Tutorial

![Platforms](https://img.shields.io/badge/Web-Windows|MacOS-lightgray.svg)
[![oAuth2](https://img.shields.io/badge/Authentication-v1-green.svg)](http://developer.autodesk.com/)
[![Data-Management](https://img.shields.io/badge/Data%20Management-v2-green.svg)](http://developer.autodesk.com/)
[![BIM360-Account-Admin](https://img.shields.io/badge/BIM360%20Account%20Admin-V1-green.svg)](http://developer.autodesk.com/)

[![Postman](https://img.shields.io/badge/Postman-v7-orange.svg)](https://www.getpostman.com/)

![Beginner](https://img.shields.io/badge/Level-Beginner-green.svg)
[![License](https://img.shields.io/:license-MIT-blue.svg)](http://opensource.org/licenses/MIT)

This folder contains a Postman Collection to setup BIM360 project, it provides the functionalities as follow:
1. Create BIM360 Project.
2. Activate Project services by adding project service admin.
3. Add users to document management and project administration module.
![Collection](Img/collection.png)

## Demonstration
[![https://youtu.be/GdJO3dPNXdY](http://img.youtube.com/vi/GdJO3dPNXdY/0.jpg)](https://youtu.be/GdJO3dPNXdY "BIM 360 project setup postman collection tutorial")

## Preparation before you begin:
- [Create Forge App, get access to a BIM 360 Account](https://forge.autodesk.com/en/docs/bim360/v1/tutorials/getting-started/get-access-to-account/)


## Instructions to run the Postman tutorial are as below:

**Please watch the [Video](https://youtu.be/GdJO3dPNXdY) for the detail workflow, or follow the steps:**

### Setup Postman environment variables:
- Import Postman collection, and setup the following environment vialables
    - in Step 0, Pre-request Script: 
        1. Forge Client Key, please change to your Forge Client Id and Secret.
        2. Admin email list, use comma to seperate mulitple admin emails, all the admin in the list will be added as project service admin for avialable service types.
        3. User email list, use comma to seperate mulitple user emails, all the user in the list will be added to document_management and project_administration modules as admin.
        4. Base domain, should be https://developer.api.autodesk.com/ by default.
        5. Service type list, use comma to seperate mulitple service types, all the service type in the list will be activated by adding project service admin.
        6. admin_index, user_index, service_index, these index will be kept to iterate the item in the corresponding list.

    - in Step 3, Pre-request Script:
        - Specify the project name that you want to create.

### Tutorials of BIM360 project setup workflow
- Step 0: Reset the environment variables as follow:
    1. Forge Client Key, please change to your Forge Client Id and Secret.
    2. Admin email list, use comma to seperate mulitple admin emails, all the admin in the list will be added as project service admin for avialable service types.
    3. User email list, use comma to seperate mulitple user emails, all the user in the list will be added to document_management and project_administration modules as admin.
    4. Base domain, should be https://developer.api.autodesk.com/ by default.
    5. Service type list, use comma to seperate mulitple service types, all the service type in the list will be activated by adding project service admin.
    6. admin_index, user_index, service_index, these index will be kept to iterate the item in the corresponding list.
- Step 1: Get 2 Legged Token to operate within BIM360 Admin.
- Step 2: Setup BIM360 Hub and Account Id.
- Step 3: Create a new project.
- Step 4: Get company list and setup the company Id.
- Step 5: Activate each project service by adding project admin. Iterate this step until all the listed project service are activated with all the listed admin. 
- Step 6: Find and setup project admin.
- Step 7: Find and setup industry role.
- Step 8: Add more users to the project, again, iterate to run this step until all the users in the list are added.

Until now, you should have successfully created a project with all the avialable project services activated, and all the listed users are imported. But to operate the project services, still have to wait for the project service admin to activate the service from email manually, then you can actually access the project services.


## Further Reading
### Automate Workflow with Postman Collection Runner
**With the help of the Postman Collection Runner, you can actually automate the workflow, it helps you to quick verify your workflow with BIM 360 Project Setup process, or to do automation test to catch all the API issues|regresions**

![bim360 workflow automation test](Img/automationtest.png)

**Please refer the [Video](https://youtu.be/tbd) for how to use postman runner, and follow the steps:**

### Tutorials about workflow

- Import the Postman **Collection**.
- Setup the environment variables as mentioned before.
- Run Postman **Collection Runner**, select the collection.
- Click **Run BIM360 Proje...** button to start, you will see the result of the workflow.

**Note:** The collection will firstly automatically create a project, then activate the avialable project services for all the admins, after that, import all the users to the project as admin of document management and project administration.   

## License
This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.

## Written by
Zhong Wu [@johnonsoftware](https://twitter.com/johnonsoftware), [Forge Partner Development](http://forge.autodesk.com)
