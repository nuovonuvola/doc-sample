# Reference

## API requests

### GET
GET will list all users in a directory.   

Example: `curl GET https://example.com/v1/users `   

Response: 200   

Description: OK   

Content: List of users. The data delivered for each user is defined in the **scheme user** in this article.   

Content Type: json

### POST
POST will create a new user.   

Example: `curl POST https://example.com/v1/users?id=123&name=musterman,max `   

Response: 201   

Description: User created   

Content: Creates a user. The data needed for a new user is defined in the **scheme user** in this article.   

Content Type: json

## Schemes

### User
The scheme *user* defines the properties available for a user.
Type: object
* **id**: A random number to identify the user. (Type: string)
* **name**: The username in the format *last name,first name*. (Type: string) 




Editors note:
* The responses for the requests only cover success. I would also list responses for failures. For Example, when no users are available in the directory (response "204" that states "No content"). 
* I would remove the last line in the snippet "# email field missing description" as I would not bother a reader with a information that has no use for him (failure on our side). 
* To make it "complete" I would add requests for updating and deleting users.