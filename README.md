# OpWeave REST API Doc

`Version: 1`

`Starting URI**:** api/v1/*`

## There are several entry points on this API.

- `**auth**`
- `**users**`
- **`communities`**
- `**authority**`

1. Sign Up:
- **`POST`  `api/v1/signup`** `(create user account)`
    
    ### **Body**
    
    | Field Name | data type | description |
    | --- | --- | --- |
    | fullname | String | Your Full Name |
    | username | String | Your Username |
    | email | String | You Email |
    | password | String | Passowrd should be at least 8 characters |
    | gender | Male/Female | Your gender |
    
    ### **Response**
    
    | Http Code | Content-Type | Response |
    | --- | --- | --- |
    | 400 | application/json | User Data related errors |
    | 201 | application/json | {
      "id": "8193e97f-cf41-4c8b-a55a-44d3243df724",
      "fullname": "Brakus",
      "username": "gottlieb",
      "email": "fay.c9bf27e9431a@yahoo.com",
      "gender": "MALE",
      "token":new generated access token
    } |
    
    ### **Example URI**
    
    **`http://localhost:8000/api/v1/signup`**
    

1. Sign In:
- **`POST`  `api/v1/signin`** `(login to user account)`
    
    ### **Body**
    
    | Field Name | data type | description |
    | --- | --- | --- |
    | username | String | Your Username |
    | password | String | Passowrd should be at least 8 characters |
    
    ### **Response**
    
    | Http Code | Content-Type | Response |
    | --- | --- | --- |
    | 400 | application/json | User Data related errors |
    | 201 | application/json | {
      "id": "8193e97f-cf41-4c8b-a55a-44d3243df724",
      "fullname": "Brakus",
      "username": "gottlieb",
      "email": "fay.c9bf27e9431a@yahoo.com",
      "gender": "MALE",
      "avatar": "https://res.cloudinary.com/demo/image/upload/e_gen_recolor:prompt_(mug);to-color_ffd500/c_scale,h_292/samples/cup-on-a-table",
      "token":new generated access token
    } |
    
    ### **Example URI**
    
    **`http://localhost:8000/api/v1/signin`**
