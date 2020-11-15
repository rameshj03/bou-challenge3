**Get all Phone numbers of all Customers**
----
  Returns json data for all available customers phone numbers.

* **URL**

  /api/v1/customers/phones

* **Method:**

  `GET`
  
* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
	"data": [{
		"cust_id": "1",
		"cust_name": "Ramesh Jambulingam",
		"phone": [{
			"phone_id": "1",
			"primary": "True",
			"value": "+10004447777",
			"label": "work"
		}, {
			"phone_id": "2",
			"primary": "False",
			"value": "+10009335555",
			"label": "home"
		}]
	}]
}`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "No customers exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

  OR

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Bad request." }`
    
      OR

  * **Code:** 500 INTERNAL SERVER SERVER <br />
    **Content:** `{ error : "Internal Server Error." }`
  
**Get all Phone numbers of a Single Customer**
----
  Returns json data for all available phone numbers of a single customer.

* **URL**

  /api/v1/customers/{cust_id}/phones

* **Method:**

  `GET`
  
  *  **URL Params**

   **Required:**
 
   `cust_id=[integer]`
   
   
* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ cust_id : 12, cust_name : "Michael Bloom", , phone : [{
		"primary": "True",
		"value": "+971 56 888888",
		"label": "mobile"
	} }`
 
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "Customer doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

  OR

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Bad request." }`
    
      OR

  * **Code:** 500 INTERNAL SERVER SERVER <br />
    **Content:** `{ error : "Internal Server Error." }`

 
**Activate a customer's Phone number**
----
  Returns json data for all available phone numbers of a single customer.

* **URL**

  /api/v1/customers/{cust_id}/{phone}

* **Method:**

  `PUT`
  
  *  **URL Params**

   **Required:**
 
   `cust_id=[integer]`
   
   **Required:**
 
   `phone=[integer]`
   
   
* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
	"data": {
		"cust_id": "1",
		"activated": "True",
		"phone": {
			"phone_id": 1,
			"phone": "+971 56 888888"
		}
	}
}
* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "Customer doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "You are unauthorized to make this request." }`

  OR

  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "Bad request." }`
    
      OR

  * **Code:** 500 INTERNAL SERVER SERVER <br />
    **Content:** `{ error : "Internal Server Error." }`
