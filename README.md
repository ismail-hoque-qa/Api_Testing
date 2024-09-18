### **Student Details API Testing with Postman Newman**
This project demonstrates API testing using Postman, providing a collection of tests to validate various endpoints of the API. 

### **Features**

- Tests for GET, POST, requests
- Collection of tests covering different API endpoints
- Environment setup for easy switching between environments
- Pre-request scripts for data setup
- Test scripts for assertions and validations

## API Documentation:
- https://feji.us/c8kwqu
  
### **Technology used:**
- Postman
- Newman

### **Prerequisite:**
- Node Js
- Newman
- Newman Html Report Library

### **Installation**

1. Postman: If you haven't already, [download and install Postman.](https://www.postman.com/downloads/)
2. Clone the repository:
 ```console 
  git clone https://github.com/ismail-hoque-qa/Api_Testing.git
```
3. Import the Postman collection:
    - Open Postman.
    - Click on the Import button.
    - Select the file from the repository.
4. Import the Postman environment:
    - In Postman, click on the gear icon in the top right corner.
    - Select **Import** and choose the file.
5. Newman and Report Installation Process:
    - Newman Install Command:
     ```console 
      npm install -g newman
    ```
    - Newman Html Report Install Command:
     ```console 
      npm install -g newman-reporter-htmlextra
    ```
### **Usage**
1. Select Environment:
    -   In Postman, select the appropriate environment (e.g., Development, Production) from the top-right dropdown.
3. Run Collection:
    -   Select the imported collection from the Collections sidebar.
    -   Click on the Runner button to open the collection runner.
    -   Select the desired environment.
    -   Click Start Test to run the collection.
8. View Results:
    -   Once the tests are complete, view the results in the Runner tab.
    -   Detailed test results can be viewed for each request.

## **Testing**

## Test Case Scenarios:

## _**1. Create Student **_

### Request URL: https://thetestingworldapi.com/api/studentsDetails
  **Request Body:** 
 ```console 
 { 
"first_name": "sample string 2", 
"middle_name": "sample string 3", 
"last_name": "sample string 4", 
"date_of_birth": "sample string 5" 
}
```
  **Response Body:**
 ```console 
   { 
"id": 526718, 
"first_name": "sample string 2", 
"middle_name": "sample string 3", 
"last_name": "sample string 4", 
"date_of_birth": "sample string 5" 
} 

```
 ## _**2. Get Specific student Details By ID**_
### Request URL: https://thetestingworldapi.com/api/studentsDetails/id 
### Request Method: GET
### Response Body:
 ```console  
"status": "true", 
"data": { 
"id": 526716, 
"first_name": "sample ", 
"middle_name": "sample ", 
"last_name": "sample ", 
"date_of_birth": "sample " 
} 

```
## _**3. Get Student **_
### Request URL: https://thetestingworldapi.com/api/studentsDetails 
### Request Method: GET
### Pre-request Script: None
### Request Body:None
  **Response Body:**
 ```console 
[ 
{ 
"id": 526717, 
"first_name": "Anna", 
"middle_name": "Banana", 
"last_name": null, 
"date_of_birth":"12/23/1990" 
},
{ 
"id": 526716, 
"first_name": "sample ", 
"middle_name": "sample ", 
"last_name": "sample ", 
"date_of_birth": "sample " 
},
{ 
"id": 526715, 
"first_name": "Anna", 
"middle_name": "Banana last_name=Uzumaki", 
"last_name": null, 
"date_of_birth": "12/23/1990" 
} ,
……………………………………………………..
] 

```

 ## _**4. Create Technical Skills **_
### Request URL: https://thetestingworldapi.com/api/technicalskills 
### Request Method: POST
  **Request Body:** 
 ```console 
  { 
"id": 1, 
"language": [ 
"sample string 1", 
"sample string 2" 
], 
"yearexp": "sample string 2", 
"lastused": "sample string 3", 
"st_id": id 
}

```
  **Response Body:**
 ```console 
  { 
"status": "true", 
"msg": "Add data success" 
}

```

 ## _**5. Create Student Address **_

### Request URL: https://thetestingworldapi.com/api/addresses
### Request Method: POST
**Request Body:**
```console
{ 
"Permanent_Address": { 
"House_Number": "sample string 1",
"City": "sample string 2",
 "State": "sample string 3", 
"Country": "sample string 4",
"PhoneNumber": [ 
{ 
"Std_Code": "sample string 1",
"Home": "sample string 2",
 "Mobile": "sample string 3" 
},
{ 
"Std_Code": "sample string 1",
"Home": "sample string 2", 
"Mobile": "sample string 3" 
} 
] 
},
"stId": id 
} 

```

**Response Body:**
```console
{ 
"status": "true", 
"msg": "Add data success" 
} 

``` 
## Run Command:  
- Run Command for Console: 
```console 
newman run Test.postman_collection.json -e Test.postman_environment.json 
```
- Run Command for Report: 
```console 
newman run Test.postman_collection.json -e Test.postman_environment.json -r cli,htmlextra
```

## Newman Report Summary:
![image](https://github.com/user-attachments/assets/62014367-5b04-4126-a262-41923e465c09)
![image](https://github.com/user-attachments/assets/3f33b126-a3c5-4a6f-80aa-1bc962a4aaad)
![image](https://github.com/user-attachments/assets/e61be1bf-3f8c-4402-ace1-614d5fb9818d)
![image](https://github.com/user-attachments/assets/62f7d90f-2a48-435e-add7-15fd3205218d)

