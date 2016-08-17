# UWP Advertising Sample

The sample attached in this code is a modified version of the one available @ [windows-universal-samples] repository. 

Before running this sample locally, please ensure the following: 
- Start, Run, Search for "Windows Powershell" and Launch it.
- Run get-appxpackage -name *advertising*
- Make note of the version (under resource id).
- Ensure that it is atleast 1605.12003 and above.
- If not, contact the Dev Center team for support.

## I am already using the Advertising Control (or the AdControl). Give me the 2 minute overview? 

- Find out the BigId (example: **9wzdncrdn95f**) for your application.
- Get the AdUnitId (example: **ctrl-9wzdncrdn95f-1**) from the Dev Center Team.

- In your app code, replace the values of the application id and the ad control id, with the following ids, as shown below – this is just an illustration and you can set the other attributes based on your need

              <ads:AdControl 
               ApplicationId="9wzdncrdn95f" AdUnitId="ctrl-9wzdncrdn95f-1" 
               Width="300" Height="250" 
               AdRefreshed="OnAdRefreshed" 
               ErrorOccurred="OnErrorOccurred"/> 

- Once you make this code change, please re-publish your app 

## Using the samples

### System Requirements: 
- Windows 10
- Visual Studio 2015
- Windows Software Development Kit (SDK) for Windows 10
- Any other updates prompted by Visual Studio 2015 (i have update 3)

>The easiest way to see what is going on without using GIT is to download the zip file containing the current version, unzip the entire archive and use the samples in Visual Studio 2015.

### Other tools:
- Fiddler2

>In Fiddler, go to Filters (in right hand side tab) and in the hosts tab add the following: adbroker.mp.dse.microsoft.com;. This will ensure that only requests to adbroker will be logged and you can now see the request-response sent to adbroker to get the ads.

## Understanding the sample: 

The sample contains 2 ways to use the Microsoft Advertising Control
- Through a XAML markup 
- Programmatically 

In both the cases, only the 2 following parameters are required: 

1. **Application Id**: This is the same as Big Id of the product.
2. **AdUnit Id**: Even though we will have a self-serve UX to do auto procure these Ids, you need to contact the Dev Center support for the same right now.

> We have 2 waterfall models right now. The AdUnitId in the XAML markup has Microsoft Advertising as the top priority followed by Smaato while the AdUnitId in the Programmatic sample has Smaato followed by Microsoft advertising.

[windows-universal-samples]: <https://github.com/oldnewthing/Windows-universal-samples>