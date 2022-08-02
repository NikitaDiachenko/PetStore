**Test Cases for POST "https://petstore.swagger.io/v2/pet".**

**Positive cases:**

1) **I want to check POST /pet status code is 200**

   _Preconditions:_
   - installed Postman
   - Postman is launched
   - PetStore collection imported
   - PetStore environments imported
   

   _Steps:_
   - Send out POST /pet request

   _Expected result:_
   - POST /pet status code is 200

2) **I want to check that content-type is .json in the POST /pet response headers**

	 _Preconditions:_
	 - installed Postman
   - Postman is launched
   - PetStore collection imported
   - PetStore environments imported
	 
	_Steps:_
   - Send out POST /pet request
   
   _Expected result:_
   - received content-type is .json

3) **I want to send the POST /pet request only with required fields (photoUrls, name)**

	 _Preconditions:_
	 - installed Postman
   - Postman is launched
   - PetStore collection imported
   - PetStore environments imported
	 
	_Steps:_
   - Send out POST /pet request **only** with required key&values (photoUrls, name)
   
   _Expected result:_
   - The pet object was created successfully only with the required fields sent in the request body

4) **I want to check pet id value in the POST /pet response is valid**

	 _Preconditions:_
	 - installed Postman
   - Postman is launched
   - PetStore collection imported
   - PetStore environments imported
	 
	_Steps:_
   - Send out POST /pet request with pet id
   
   _Expected result:_
   - pet id value was successfully set in the response body

5) **I want to check category.id value in the POST /pet response is valid**

   _Preconditions:_
   - installed Postman
   - Postman is launched
   - PetStore collection imported
   - PetStore environments imported
   
   _Steps:_ 
   - Send out POST /pet request with category.id
   
   _Expected result:_
   - category.id value was successfully set in the response body
 
 6) **I want to check category.name value in the POST /pet response is valid**
 
    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported
   
    _Steps:_ 
    - Send out POST /pet request with category.name
   
    _Expected result:_
    - category.name value was successfully set in the response body
   
  7) **I want to check tags.id value in the POST /pet response is valid**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out POST /pet request with tags.id
   
     _Expected result:_
     - tags.id value was successfully set in the response body

 8) **I want to check tags.name value in the POST /pet response is valid**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out POST /pet request with tags.name
   
     _Expected result:_
     - tags.name value was successfully set in the response body

 9) **I want to check status value in the POST /pet response is valid**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out POST /pet request with status
   
     _Expected result:_
     - status value was successfully set in the response body

 10) **I want to check that photoUrls values in array were set in the POST /pet response**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
    
     _Steps:_ 
     - Send out POST /pet request with status
     - Send out the https://petstore.swagger.io/#/pet/uploadFile request with attached .jpg file
     - Send out the https://petstore.swagger.io/#/pet/getPetById request with the id of created pet
   
     _Expected result:_
     - photoUrls array is filled by value in the response body with the link on the uploaded .jpg file 

**Negative cases:** (not a full list of negative cases)

 1) **I want to check the status code if POST /pet request was sent without pet id value**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported

    _Steps:_
    - Send out POST /pet request without value in the id key

    _Expected result:_
    - 400 Bad Request status code was shown

 2) **I want to check the response body if POST /pet request was sent without pet id value**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported

    _Steps:_
    - Send out POST /pet request without value in the id key

    _Expected result:_
    - error text in the response body is present

 3) **I want to send out the POST /pet request without required fields (photoUrls, name)**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported

    _Steps:_
    - Send out POST /pet request without required fields (photoUrls, name)

    _Expected result:_
    - 400 Bad Request status code was shown in the response, error text in the response body was shown

 4) **I want to send out the POST /pet request with invalid syntax in the request body**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported

    _Steps:_
    - Send out POST /pet request with invalid syntax in the request body

    _Expected result:_
    - 400 Bad Request status code was shown in the response, error text was shown
 

**Test Cases for GET "https://petstore.swagger.io/#/pet/getPetById".**

**Positive cases:**

 1) **I want to check GET /pet/{{petId}} status code is 200**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported

    _Steps:_
    - Send out GET /pet/{{petId}} request (the pet object will be created by POST /pet in the pre-request scripts)

    _Expected result:_
    - GET /pet status code is 200

 2) **I want to check that content-type is .json in the GET /pet/{{petId}} response headers**

	  _Preconditions:_
	  - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported
	 
	 _Steps:_
    - Send out GET /pet/{{petId}} request
   
    _Expected result:_
    - received content-type is .json

 4) **I want to check pet id value in the GET /pet/{{petId}} response is valid**

	  _Preconditions:_
	  - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported
	 
	 _Steps:_
    - Send out GET /pet/{{petId}} request
   
    _Expected result:_
    - pet id value was is present in the response body

 5) **I want to check category.id value in the GET /pet/{{petId}} response is valid**

    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported
   
   _Steps:_
    - Send out GET /pet/{{petId}} request
   
		
   _Expected result:_
    - category.id value is present in the response body
 
 6) **I want to check category.name value in the POST /pet/{{petId}} response is valid**
 
    _Preconditions:_
    - installed Postman
    - Postman is launched
    - PetStore collection imported
    - PetStore environments imported
   
    _Steps:_ 
    - Send out GET /pet/{{petId}} request 
   
    _Expected result:_
    - category.name value is present in the response body
   
  7) **I want to check tags.id value in the GET /pet/{{petId}} response is valid**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out GET /pet/{{petId}} request
   
     _Expected result:_
     - tags.id value is present in the response body

 8) **I want to check tags.name value in the GET /pet/{{petId}} response is valid**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out GET /pet/{{petId}} request
   
     _Expected result:_
     - tags.name value is present in the response body

**Negative cases:**

 1) **I want to check the status code if GET /pet/{{petId}} was sent with non-existing id**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out GET /pet/**123523523523** request
   
     _Expected result:_
     - 404 Not Found status code in the response

 2) **I want to check the response body if GET /pet/{{petId}} was sent with non-existing id**
 
     _Preconditions:_
     - installed Postman
     - Postman is launched
     - PetStore collection imported
     - PetStore environments imported
   
     _Steps:_ 
     - Send out GET /pet/**123523523523** request
   
     _Expected result:_
     - error text is present in the response body



