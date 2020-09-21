# CheckInAppSimple - Location_Report

This one is the starting template for learning how to use map APIs

- Using SharePoint List to record data
- Create SPO List using Power Automate (one-time instant flow)
- Toggle map between Bing map and Google map
- Using Bing Map as connector 
- Bing API for Map feature (sign up and get key here https://www.bingmapsportal.com/) 
- Bing map reference https://docs.microsoft.com/en-us/bingmaps/rest-services/imagery/get-a-static-map?redirectedfrom=MSDN
- Also use Google map API (sign up, create project and get key here https://cloud.google.com/maps-platform/)
- Google map reference https://developers.google.com/maps/documentation/maps-static/overview

## 1 Get Bing Map key
 - Bing Map API key for dev/test (sign up and get key here https://www.bing.com/partners/developers#MapsAPIs) 
 ![Bingmap](/images/bingmap.jpg)
 
## 2. Get Google Map Key
 - Sign up using gmail account
 - create project and get map key https://developers.google.com/maps/documentation/static-maps/get-api-key (see this link)
  ![googlemap](/images/googlemap.jpg)

## 3 Create SPO List name Location_Report using Power Automate (CreateSPOList.zip)
  - You need to create your SharePoint Site first
  - Go to https://flow.microsoft.com/manage/
  - Upload Flow template (CreateSPOList) as new and fix other dependencies
  - Edit the flow and input your SharePoint Site URL (Initialize variable) (Pic1)
  - Run the flow to create SPO List
  - SPO List for this one will name as Location_Report
  
  ![flow](/images/Pic1.jpg)

## 4 Create Power Apps via template upload (CheckInAppSimple-Location_Report.zip)
  - Go to https://make.powerapps.com/
  - Import canvas app using as new and fix other dependencies
  - Edit this app
  - Go to first screen app edit the image properties and input your Google API key (Pic2)
  - At data tab, edit SPO site to target your SPO List (Pic3 and Pic4)
  - At data tab, edit Bing Maps to insert your Own Key (Pic5)
  
  ![Google API](/images/Pic2.jpg)
  ![ADD SPO list](/images/Pic3.jpg)
  ![ADD SPO list2](/images/Pic4.jpg)
  ![Bing API](/images/Pic5.jpg)
  
**In city field, I hardcoded as "Bangkok" since API doesn't support. But you still can get city name in "address" field**

  ![flow](/images/hardcode.jpg)
  
**** Update Sep 2020, I'm using PowerApps Formula inorder to extract to provice only just replace "Bangkok" with Left(First(LastN(Split(BingMaps.GetLocationByPoint(Location.Latitude, Location.Longitude).name, ","), 2)).Result,Len(First(LastN(Split(BingMaps.GetLocationByPoint(Location.Latitude, Location.Longitude).name, ","), 2)).Result)-5)

![flow](/images/hardcode-fixed.jpg)



  
  
