
![SHRAMEV](https://i.ibb.co/8mXj78j/v1-logo-blue-01.png  =170x)

## Environment Variable

1. `FIREBASE_WEB_API` 
2. `FIREBASE_API` :  **Base64**
3. `EMAIL`
4. `PASSWORD`
5. `HASH_PRIVATE_KEY` : **Base64**
6. `HASH_PUBLIC_KEY` : **Base64**
7. `ENCRPT_PUBLIC_KEY` : **Base64**
8. `ENCRPT_PUBLIC_KEY` : **Base64**

## Endpoints

 1. `/login` : post         
        <pre>     
                    
 * Request data : `{"emailAddress": "example@gmail.com","password":"Qwerty1@"}`
 * Success response : `OK 200`
 * Http error : 
	*  `{"detail":"INVALID_DATA"}, status_code : 422`
	 * `{"detail":"EMAIL_NOT_VERIFIED"}, status_code : 401`
	 * `{"detail":"INVALID_EMAIL_PASSWORD"}, status_code : 404`	
	 * `{"detail":"UNEXPECTED_ERROR"}, status_code : 500`
              

      </pre>
     

 2. `/signup` : post 
         <pre>
   * Request data :  `{"emailAddress":  "example@gmail.com","password":"Qwerty1@"}`
   *  Success response : `OK 200`
   *  Http error :
	    *  `{"detail":"INVALID_DATA"}, status_code : 422`
	    * `{"detail":"UNEXPECTED_ERROR"}, status_code : 500`
	    * `{"detail":"USER_ALREADY_EXIST"}, status_code : 409`
                 

   </pre>

 3. `/reset_password`  :  post
        <pre> 
* Request data: `Header : {"emailAddress": "example@gmail.com"}` **Only if service is exposed**
* Success response : `OK 200`
*  Http error : 
   * `{"detail":"UNEXPECTED_ERROR"}, status_code : 500`
</pre> 

4. `/renew_token` : post
       <pre> 
* Request data: `Header : {"emailAddress": "example@gmail.com", "userId":"123456789"}` **Only if service is exposed**
*  Success response : `OK 200`
*  Http error : `None`
</pre>


## Port

 - `dev : 8000`
 - `prod : 8000`

## Email Template

 - [ ] Email verification
 - [ ] Reset Password



  
