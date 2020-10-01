# Matrix API Calls

1. List the versions supports:
    > /_matrix/client/versions

2. Get the home server’s login supported forms

    >GET /_matrix/client/r0/login

3. Login to the server and get the access token.

    * Post URL should be sent and this returns the user_id, access_token, home_server, devide_id, well_known
    > POST /_matrix/client/r0/login

    ```json
    {
     "type": "m.login.password",
     "identifier": {
       "type": "m.id.user",
       "user": "<user_name>"
     },
     "password": "<user_password>"
   }
    ```

   output:

   ```json
    {
        "user_id": "@sarath.oruganti:jbrec-gcp.ml",
        "access_token"  MDAxYWxvY2F0aW9uIGpicmVjLWdjcC5tbAowMDEzaWRlbnRpZmllciBrZXkKMDAxMGNpZCBnZW4gPSAxCjAwMzBjaWQgdXNlcl9pZCA9IEBzYXJhdGgub3J1Z2FudGk6amJyZWMtZ2NwLm1sCjAwMTZjaWQgdHlwZSA9IGFjY2VzcwowMDIxY2lkIG5vbmNlID0geGlld3dzMEhUVjFNRV9ZWQowMDJmc2lnbmF0dXJlIEzk9ny-iFm3nlcxQtjU4xLb59eMABlyqw6seeHw4Xe2Cg",
        "home_server": "jbrec-gcp.ml",
        "device_id": "TFFLJTASXI"
    }
    ```
