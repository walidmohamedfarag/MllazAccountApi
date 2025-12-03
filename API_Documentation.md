

1. Register
URL: http://mllazaccount.runasp.net/api/Identity/Accounts
Method: POST
Endpoint: /accounts
Description: create new account
Body (JSON):
{
  "firstName": "",
  "lastName": "",
  "email": "",
  "password": "",
  "confirmPassword": ""
}
Response: 
**BadRequest contains error message if email is exsit already
**Ok contains success message Regisrter Successfully

_____________________________________________________

2. Login 
URL: http://mllazaccount.runasp.net/api/Identity/Accounts/Login
Method: POST
Endpoint: /Accounts/Login
Description: login by email and password
Body (JSON):
{
  "email": "",
  "password": "",
}
Response: 
**BadRequest contains error message if email is not found or password invalid
**Ok contains success message login Successfully

_____________________________________________________

3. ForgetPassword
URL: http://mllazaccount.runasp.net/api/Identity/Accounts/ForgetPassword
Method: GET
Endpoint: /Accounts/ForgetPassword
Description: order to reset password by email
Body (JSON):
{
  "email": "",
}
Response: 
**BadRequest contains error message if email is not found
**Ok contains success message valid email and user id 

________________________________________________


4. Reset Password
URL: http://mllazaccount.runasp.net/api/Identity/Accounts/ResetPassword
Method: POST
Endpoint: /Accounts/ResetPassword
Description: reset password by user id and password confirmpassword
Body (JSON):
{
  "userId": "",
  "password": "",
  "confirmPassword": ""
}
Response: 
**Ok contains success message Password Reset Successfully 


________________________________________________


5. Gust Login
URL: http://mllazaccount.runasp.net/api/Identity/Accounts/GustLogin
Method: POST
Endpoint: /Accounts/GustLogin
Description: login as a gust
Body: No body 
Response: 
**Ok contains success message Login Successfully as Gust 

