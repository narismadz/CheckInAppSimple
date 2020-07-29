# CheckInAppSimple - Location_Report

This one is the starting template for learning how to use map APIs

- Using SharePoint List to record data
- Create SPO List using Power Automate (one-time instant flow)
- Toggle map between Bing map and Google map
- Using Bing Map as connector 
- Bing API for Map feature (sign up and get key here https://www.bing.com/partners/developers#MapsAPIs) 
- Bing map reference https://docs.microsoft.com/en-us/bingmaps/rest-services/imagery/get-a-static-map?redirectedfrom=MSDN
- Also use Google map API (sign up, create project and get key here https://cloud.google.com/maps-platform/)
- Google map reference https://developers.google.com/maps/documentation/maps-static/overview

1 Get Bing Map key
 - Bing Map API key for dev/test (sign up and get key here https://www.bing.com/partners/developers#MapsAPIs) 
 
2. Get Google Map Key
 - Sign up using gmail account
 - create project and get map key https://www.bing.com/partners/developers#MapsAPIs

3 Create SPO List name Location_Report using Power Automate (You need to create your SharePoint Site first)
  - Go to https://flow.microsoft.com/manage/
  - Upload Flow template (CreateSPOList) as new and fix other dependencies
  - Edit the flow and input your SharePoint Site URL (Initialize variable)
  - Run the flow to create SPO List

4 Create Power Apps via template upload
  - Go to https://make.powerapps.com/
  - Import canvas app using as new and fix other dependencies
  - Edit this app
  - At data tab, edit SPO site to target your SPO List
  - At data tab, edit Bing Maps to insert your Own Key
  - Go to first screen app edit the image properties and input your Google API key 
