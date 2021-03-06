# Updated Information

This is copied from https://github.com/Autodesk-Forge/learn.forge.viewhubmodels/tree/netcore

Video showing the entire tutorial: https://www.youtube.com/watch?v=nMj_QMnspEk

Configuring Properties/Debug is better explained here: https://learnforge.autodesk.io/#/environment/setup/netcore_3legged

Listing hubs/projects https://learnforge.autodesk.io/#/datamanagement/hubs/readme

## Forge

https://github.com/Autodesk-Forge/forge-api-dotnet-client Forge API Client for .NET
  Open issue: https://github.com/Autodesk-Forge/forge-api-dotnet-client/issues/76

---
# Description

This sample is part of the [Learn Forge](http://learnforge.autodesk.io) tutorials. It includes authentication, listing and viewing files.

# Setup

## Prerequisites

1. **Forge Account**: Learn how to create a Forge Account, activate subscription and create an app at [this tutorial](http://learnforge.autodesk.io/#/account/). 
2. **Visual Studio**: Community edition.
3. **.NET Core** basic knowledge with C#
4. **JavaScript** basic knowledge with **jQuery**

For using this sample, you need an Autodesk developer credentials. Visit the [Forge Developer Portal](https://developer.autodesk.com), sign up for an account, then [create an app](https://developer.autodesk.com/myapps/create) that uses Data Management and Model Derivative APIs. For this new app, use `http://localhost:3000/api/forge/callback/oauth` as Callback URL, although is not used on 2-legged flow. Finally take note of the **Client ID** and **Client Secret**.

## Running locally

Clone this project or download it (this `netcore` branch only). It's recommended to install [GitHub desktop](https://desktop.github.com/). To clone it via command line, use the following (**Terminal** on MacOSX/Linux, **Git Shell** on Windows):

    git clone -b netcore https://github.com/Autodesk-Forge/learn.forge.viewhubmodels.git

For Visual Studio, go to project properties and specify the environment variables. For Visual Code, create a new Debug Configuration with the environment variables:

- `FORGE_CLIENT_ID`: your Forge Client ID
- `FORGE_CLIENT_SECRET`: your Forge Client Secret
- `FORGE_CALLBACK_URL`: `"http://localhost:3000/api/forge/callback/oauth"`

Compile the solution, Visual Studio should download the NUGET packages ([Autodesk Forge](https://www.nuget.org/packages/Autodesk.Forge/), [RestSharp](https://www.nuget.org/packages/RestSharp) and [Newtonsoft.Json](https://www.nuget.org/packages/newtonsoft.json/)).

# Further Reading

Documentation:

- [BIM 360 API](https://developer.autodesk.com/en/docs/bim360/v1/overview/) and [App Provisioning](https://forge.autodesk.com/blog/bim-360-docs-provisioning-forge-apps)
- [Data Management API](https://developer.autodesk.com/en/docs/data/v2/overview/)
- [Viewer](https://developer.autodesk.com/en/docs/viewer/v6) 

### Troubleshooting

1. **Cannot see my BIM 360 projects**: Make sure to provision the Forge App Client ID within the BIM 360 Account, [learn more here](https://forge.autodesk.com/blog/bim-360-docs-provisioning-forge-apps). This requires the Account Admin permission.

2. **error setting certificate verify locations** error: may happen on Windows, use the following: `git config --global http.sslverify "false"`

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.

## Written by

Augusto Goncalves [@augustomaia](https://twitter.com/augustomaia), [Forge Partner Development](http://forge.autodesk.com)