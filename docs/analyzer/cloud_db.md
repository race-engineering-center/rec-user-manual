# Garage61 client

This window lets you access laps from the [Garage61](https://garage61.net)  online platform. You can browse, search, and 
load laps directly into the analyzer for review and comparison.

Currently you can only access laps driven by yourself or your teammates due to Garage61 API limitations. See 
[Garage61 API docs](https://garage61.net/developer/endpoints/v1/findLaps) for more details.

!!! Note 
    For your own sessions, it's better to import laps directly from `.ibt` files when possible, since they include
    significantly more detailed data than Garage61 provides.

![Garage61 client window](img/g61_overview.png "Garage61 client window")

## Authorization

REC uses OAuth2 to access Garage61 data. OAuth2 is a secure authorization protocol - REC never sees or stores your 
Garage61 password. Authentication happens through the Garage61 website, and REC only gets a temporary access token to 
fetch your data.

To see if your client is currently authorized to access Garage61 data, check bottom right corner of the window. If it
says "Status: Authorized", you're good to go. If it doesn't, press an "Authorize" button on the main toolbar. Your 
default browser window will open with a prompt to grant REC access to Garage61 data:

![Garage61 OAuth2 prompt](img/g61_oauth_prompt.png "Garage61 OAuth2 prompt")

Pressing blue "Authorize" button should show you the following page which indicates that authorization was successful
and now you can browse and download laps from Garage61:

![Garage61 OAuth2 success](img/g61_oauth_success.png "Garage61 OAuth2 success")

## Selecting and downloading laps

Filter tree on the left side of the window shows you all available cars, tracks and drivers to download laps from. You
can search for the cars, tracks and drivers using search field on the top:

![Garage61 filter search](img/g61_filters_search.png "Garage61 filter search")

1. Select a track from the list of available tracks. Note that you can only select one track;
2. Select any number of cars from the list of available cars;
3. Select any number of drivers from the list of available drivers;
4. Optionally check "Only include personal best laps" to only include personal best laps;
5. Click "Update laps". This will fetch the lap info only to allow you to choose specifically, what laps to download 
for analysis;
6. Select laps you want to download and click "Download selected laps";

REC will request those laps from Garage61 and download them into your local lap library. You can now load them into 
Analyzer for review as usual (see [Lap library section](laplibrary.md##loading-laps-for-analysis) for details).

![Garage61 downloading laps](img/g61_client_workflow.gif "Garage61 downloading laps")

