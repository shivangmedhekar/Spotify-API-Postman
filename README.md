# Spotify-API-Postman

Go to [Spotify Developers](https://developer.spotify.com/) Web Page and click on **Dashboard**, Login with your Spotify Account.

Click on **CREATE AN APP**

Give the app a name and description, Agree to Terms & Conditions and then Click on **Create**.
You will be taken to the Dashboard of the app you just created.
Click on **EDIT SETTINGS**
Scroll to **Redirect URIs** and the the following URI
```
https://oauth.pstmn.io/v1/callback
```

Then click on **ADD**

Now open Postman, and create a new collection.
Name the collection eg Spotify API
In the Authorization section select Type as **OAuth 2.0**
You will get all options to configure the authorization
Scroll to Callback URL under Configure New Token
Copy & Paste the same URL you did in your Spotify App you created in Redirect URI
```
https://oauth.pstmn.io/v1/callback
```
In Auth URL add the following URL
```
https://accounts.spotify.com/authorize
```

Access Token URL
```
https://accounts.spotify.com/api/token
```

Go to your app Dashboard on Spotify Developer and Copy and Paste Client ID and Client Secret

Go the [Authorization Scopes](https://developer.spotify.com/documentation/general/guides/authorization/scopes/) in Development Guide under Docs of Spotify Developer and copy the scopes you want and paste it under scopes of your collection in Postman. For multiple scopes keep a space between multiple scope names.
