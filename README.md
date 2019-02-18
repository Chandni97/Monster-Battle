# Monster-Battle
An augmented reality battle game integrated with Watson SDK for AI capabilities


## Getting started 

1. Sign up for an [IBM Cloud account](https://console.bluemix.net/registration/)
1. Sign up for a [Vuforia account](https://developer.vuforia.com/vui/auth/register)
1. Sign up for a [PubNub account](https://dashboard.pubnub.com/signup)
1. Install [Unity 2018.3.3](https://unity3d.com/get-unity/download/archive)
1. Download the Assets and Project Settings Folder from [here]()
1. Print the image from the folder.


## Steps to create the game

1. Create a new project in Unity

### Set up your project for Vuforia
1. Login to the Vuforia account 
1. Navigate to License Manager and create a new development key. You will use this key later on to develop the application
1. To activate Vuforia in your unity project, access the player settings from Edit > Project Settings, then select the Player category, and select the tab for the mobile device you are building to. Under the XR Settings panel, enable the Vuforia Augmented Reality Support property.
1. Navigate to Target Manager and create a new database for unity editor.
1. Click on the database created.
1. Click on Add Target. Set the type to single image, select the image from the folder you downloaded from box, set the width, name and click add.
1. Click on Download Database and you will import the downloaded package later on.

### Create the speech to text service
1. Login to the IBM cloud account
1. Navigate to the catalog, search for speech to text and create the service in the Dallas region.
1. Create new credentials for the service from the service credential tab.
1. Take note of the iam_apikey, you will use this key later on to develop the application.

### Get the publish and subscribe keys from pubnub
1. Login to the pubnub application
1. Click on the Demo Project
1. Click on create new keyset
1. Take note of the publish and subscribe keys.

### Set up the unity project to work with different services created above.
1. Copy and replace the Asset and Project Settings Folder that you downloaded earlier. 
1. Double click on the image package that you downloaded from vuforia to import it in the project.
1. Open the Inspector Window by navigating to Window > General > Inspector (Shortcut - CTRL+3).
1. Open the Project Heirarchy by navigating to Window > General > Heirarchy (Shortcut - CTRL+4).
1. Select AR Camera, click on open vuforia engine configuration and paste the vuforia license key. Make sure the database that you created in vuforia is added under databases.
1. Select Image Target from the Hierarchy.
1. Under Image Target Behaviour, select your image target.
1. In the inspector window, scroll down to the Main 2 script and paste the pubnub publish key and pubnub subscribe key in the text box for pubnub_pub and pubnub_sub respectively.
1. Paste the speect to text api key in the Example Streaming Script.

### Click on run, point the camera at the image and enjoy the game.

### TO DO
1. Integrate IBM Watson Assistant for help with the game.
1. Allow player 1 and 2 to input an unique number to add it to the pubnub channels so that multiple players can play using the same pubunb account.
