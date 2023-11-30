--> Complete implementation of Jwt token generation has be Done in Project
============================================================================

1 -> Jwt works on token based system like

    --> In the 1st we have to send our Users credential to authenticate

    --> the Users data should be in DB before sending for authenticate

1 --> To add user in the database follow the below steps

    --> In this project for creating new User ,we have the one RestEnd point called "registerNewUser" in the UserController

    --> with that url we have to send tha data from postman into the database like below

    --> localhost:9090/registerNewUser  POST MAPPING

    -->      {
                   "userName" : "userName",
                  "userFirstName" :"userFirstName",
                  "userLastName" :"userLastName",
                  "userPassword" :"userPassword"
    }


    --> this is add our data into db


2 --> After User has been added to the database then we can send our credentials for authentication to get jwt token

    --> PostMapping localhost:9090/authenticate

    --> in the body in json format send  our credentials

    {
        "userName" : "userName",
         "userPassword" :"userPassword"
    }

    --> if the credentials are correct then it we generate a jwt token

    --> take that jwt token


3 --> Send jwt in token in the headers

    --> localhost:9090/forUser  Get-mapping

    --> in key select Authorization

    --> in body Bearer paste jwt in the headers



