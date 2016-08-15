# UWP Advertising Sample

The sample attached in this code is a modified version of the one available @ [windows-universal-samples] repository. 

Before running this sample locally, please ensure the following: 
- Start, Run, Search for "Windows Powershell" and Launch it.
- Run get-appxpackage -name *advertising*
- Make note of the version (under resource id).
- Ensure that it is atleast 1605.12003 and above.
- If not, contact the Dev Center team for support.

# Using the samples

### System Requirements: 
- Windows 10
- Visual Studio 2015
- Windows Software Development Kit (SDK) for Windows 10
- Any other updates prompted by Visual Studio 2015 (i have update 3)

>The easiest way to see what is going on without using GIT is to download the zip file containing the current version, unzip the entire archive and use the samples in Visual Studio 2015.

### Other tools:
- Fiddler2

>In Fiddler, go to Filters (in right hand side tab) and in the hosts tab add the following: adbroker.mp.dse.microsoft.com;. This will ensure that only requests to adbroker will be logged and you can now see the request-response sent to adbroker to get the ads.

# Understanding the sample: 

The sample contains 2 ways to use the Microsoft Advertising Control
- Through a XAML markup 
- Programmatically 

In both the cases, only the 2 following parameters are required: 

1. **Application Id**: This is the same as Big Id of the product.
2. **AdUnit Id**: Even though we will have a self-serve UX to do auto procure these Ids, you need to contact the Dev Center support for the same right now.

> We have 2 waterfall models right now. The AdUnitId in the XAML markup has Microsoft Advertising as the top priority followed by Smaato while the AdUnitId in the Programmatic sample has Smaato followed by Microsoft advertising.

[windows-universal-samples]: <https://github.com/oldnewthing/Windows-universal-samples>