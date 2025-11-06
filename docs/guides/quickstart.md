# User API quick start

This API allows you to manage your users. The following options are available: 

## Show all users
**Example**

    curl GET https://api.example.com/v1/users    

**Response**: List of user objects

## Create user
**Example**

    curl -X POST \
	  -H "Content-Type: application/json" \
	  -d {"name":"John","email":"john@example.com"}' \
      https://api.example.com/v1/users 




Editors note:
* --body is not a valid curl argument