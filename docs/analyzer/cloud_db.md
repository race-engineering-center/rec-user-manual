# Garage61 client

This window lets you access laps from the Garage61 online platform. You can browse, search, and load laps directly into 
the analyzer for review and comparison.

Currently you can only access laps driven by yourself or your teammates due to Garage61 API limitations. See 
[Garage61 API docs](https://garage61.net/developer/endpoints/v1/findLaps) for more details.

For your own sessions, it's better to import laps directly from `.ibt` files when possible, since they include
significantly more detailed data than Garage61 provides.

![Garage61 client window](img/g61_overview.png "Garage61 client window")

## Authorization

REC uses OAuth2 to access Garage61 data. OAuth2 is a secure authorization protocol - REC never sees or stores your 
Garage61 password. Authentication happens through the Garage61 website, and REC only gets a temporary access token to 
fetch your data.

To see if your client is currently authorized to access Garage61 data, check bottom right corner of the window. If it
says "Status: Authorized", you're good to go. If it doesn't, press an "Authorize" button on the main toolbar. Your 
browser window will open with a prompt to grant REC access to Garage61 data:

![Garage61 OAuth2 prompt](img/g61_oauth_prompt.png "Garage61 OAuth2 prompt")

Pressing blue "Authorize" button should show you the following page which indicates that authorization was successful
and now you can browse and download laps from Garage61:

![Garage61 OAuth2 success](img/g61_oauth_success.png "Garage61 OAuth2 success")

## Selecting and downloading laps

...
