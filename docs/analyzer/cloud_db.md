# Garage61 client

This window lets you access laps from the [Garage61](https://garage61.net) online
platform. You can browse, search, and load laps directly into the analyzer for review
and comparison.

Currently you can only access laps driven by you or your teammates due to Garage61 API
limitations. See
[Garage61 API docs](https://garage61.net/developer/endpoints/v1/findLaps) for more
details.

!!! note

    For your own sessions, it's better to import laps directly from `.ibt` files when
    possible, since they include significantly more detailed data than Garage61 provides.

![Garage61 client window](img/g61_overview.png "Garage61 client window")

## Main toolbar

![Garage61 toolbar overview](img/g61_toolbar_marks.png "Garage61 toolbar overview")

1. Authorize
1. Update metadata
1. Update laps (see below)
1. Download selected laps
1. Show only personal best laps (checkable)
1. Show only laps from the current iRacing season (checkable)

## Authorization

REC uses OAuth2 to access Garage61 data. OAuth2 is a secure authorization protocol - REC
never sees or stores your Garage61 password. Authentication happens through the Garage61
website, and REC only gets a temporary access token to fetch your data.

To see if your client is currently authorized to access Garage61 data, check bottom
right corner of the window. If it says "Status: Authorized", you're good to go. If it
doesn't, press the "Authorize" button on the main toolbar. A browser window will open
with a prompt to grant REC access to Garage61 data:

![Garage61 OAuth2 prompt](img/g61_oauth_prompt.png "Garage61 OAuth2 prompt")

Make sure "Read your driving data and that of your teammates" is checked. Pressing the
blue "Authorize" button should show you the following page which indicates that
authorization was successful. You can now browse and download laps from Garage61:

![Garage61 OAuth2 success](img/g61_oauth_success.png "Garage61 OAuth2 success")

## Selecting and downloading laps

The filter tree on the left side of the window shows all available cars, tracks and
drivers. You can search for cars, tracks and drivers using the search field on the top:

![Garage61 filter search](img/g61_filters_search.png "Garage61 filter search")

1. Select a track from the list of available tracks. Note that you can only select one
    track;
1. Select any number of cars from the list of available cars;
1. Select any number of drivers from the list of available drivers;
1. Optionally check "Only include personal best laps" to only include personal best
    laps;
1. Click "Update laps". This will fetch the lap info to allow you to specifically choose
    which laps to download for analysis;
1. Select laps you want to download and click "Download selected laps";

REC will request those laps from Garage61 and download them into your local lap library.
You can now load them into Analyzer for review as usual (see
[Lap library section](laplibrary.md##loading-laps-for-analysis) for details).

![Garage61 downloading laps](img/g61_client_workflow.gif "Garage61 downloading laps")
