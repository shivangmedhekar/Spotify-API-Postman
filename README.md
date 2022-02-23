# Spotify API Postman Desktop

Go to [Spotify Developers](https://developer.spotify.com/) Web Page and click on **DASHBOARD**.

Login with your Spotify Account.

Click on **CREATE AN APP**

Give the app a *name* and *description*. 
Agree to Terms & Conditions and then Click on **Create**.

You will be taken to the Dashboard of the app you just created.

Click on **EDIT SETTINGS**

Scroll to **Redirect URIs** and paste the following URL
```
https://oauth.pstmn.io/v1/callback
```

Then click on **ADD**.

Now open Postman, and create a new collection.

Name the collection. *eg Spotify API*

In the Authorization section select Type as **OAuth 2.0**

After that you will get all options to configure the authorization.

Scroll to *Callback URL* under *Configure New Token*

Paste the same URL you did in your Spotify App you created in Redirect URI
```
https://oauth.pstmn.io/v1/callback
```
In Auth URL add the following URL
```
https://accounts.spotify.com/authorize
```

In Access Token URL add the following URL
```
https://accounts.spotify.com/api/token
```

Go to your app's Dashboard on Spotify Developer and Copy and Paste Client ID and Client Secret in respective fields Postman.

Go the [Authorization Scopes](https://developer.spotify.com/documentation/general/guides/authorization/scopes/) in Development Guide under Docs of Spotify Developer and copy the scopes you want and paste it under scopes of your collection in Postman. For multiple scopes keep a space between multiple scope names.

Example: 
```
playlist-read-private playlist-modify-public user-follow-read user-library-read
```
After that click on Get **New Access Token**
Spotify login page will open, login and authorize permissions.

Spotify page will close and you will get the Access Token, click on **Use Token**.

Now under your collections you will see **Add a request**. Click on it.

Use requests from [Spotify Console](https://developer.spotify.com/console/)

Remember to set Authorization Type of your request is **Inherit from parent**
