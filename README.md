# Steps to get your bearer token with postman

- Create a new App-Registration in Azure and create a client-secret 
- Make a note of your tenant id

- edit this link and run it in your browser 
`https://login.microsoftonline.com/YOUR TENANT ID/oauth2/v2.0/authorize?client_id=YOUR CLIENT ID&response_type=code&redirect_uri=https%3A%2F%2Fjwt.ms&scope=YOUR SCOPES&grant_type=client_credential&response_mode=query`

- Sign up
- Copy the Code from the URL 
![image](https://user-images.githubusercontent.com/49363446/219376456-e3cb0fc7-01e0-4b8a-a94c-0001becaf38b.png)

**Now that we have the code, we have to prepare the next request in Postman**

- Create a new GET Request with the following URL `https://login.microsoftonline.com/YOUR TENANT ID/oauth2/v2.0/token` and following Body

  `client_id:YOUR CLIENT ID`

  `scope:YOUR SCOPES`

  `code: YOUR CODE`

  `redirect_uri:https://jwt.ms`

  `grant_type:authorization_code`

  `client_secret:YOUR SECRET`

- Click Send and get the token
![image](https://user-images.githubusercontent.com/49363446/219378326-4ae968e2-2f19-4c8a-9475-2ea489e47f72.png)
