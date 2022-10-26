# Commands Used

Create the resource group:
`az group create --name rg-func-test --location "Australia East"`

Create the storage account:
`az storage account create --name storfunctestjs --location "Australia East" --resource-group rg-func-test --sku Standard_LRS`

Create the function app:
`az functionapp create --resource-group rg-func-test --consumption-plan-location "AustraliaEast" --runtime dotnet-isolated --functions-version 4 --name func-test-js --storage-account storfunctestjs`

Publish the function app:
`func azure functionapp publish func-test-js`

Stream the logs:
`func azure functionapp logstream func-test-js`

```
Retrieving Function App...
2022-10-26T04:27:58  Welcome, you are now connected to log-streaming service. The default timeout is 2 hours. Change the timeout with the App Setting SCM_LOGSTREAM_TIMEOUT (in seconds).
2022-10-26T04:28:33.378 [Information] Host Status: {
  "id": "func-test-js",
  "state": "Running",
  "version": "4.13.0.19486",
  "versionDetails": "4.13.0+da9a765ed67be48c79440526f78fa1b5c6efdeea",
  "platformVersion": "99.0.7.639",
  "instanceId": "aad20288c3057649ca3dfd75ff611a1a69ab1512e24884e8b43115c061649c89",
  "computerName": "10-30-0-225",
  "processUptime": 5606,
  "functionAppContentEditingState": "Unknown"
}
2022-10-26T04:28:40.993 [Information] You must install or update .NET to run this application.
2022-10-26T04:28:40.993 [Information] App: C:\home\site\wwwroot\Func1.dll
2022-10-26T04:28:40.993 [Information] Architecture: x86
2022-10-26T04:28:40.994 [Information] Framework: 'Microsoft.NETCore.App', version '7.0.0-rc.2.22472.3' (x86)
2022-10-26T04:28:40.995 [Information] .NET location: C:\Program Files (x86)\dotnet\
2022-10-26T04:28:40.995 [Information] The following frameworks were found:
2022-10-26T04:28:40.995 [Information] 1.0.16 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:40.996 [Information] 1.1.13 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:40.996 [Information] 2.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:40.997 [Information] 2.1.30 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.000 [Information] 2.2.14 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.000 [Information] 3.0.3 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.000 [Information] 3.1.28 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.000 [Information] 3.1.29 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.001 [Information] 5.0.15 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.001 [Information] 5.0.17 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.002 [Information] 6.0.8 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.002 [Information] 6.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.002 [Information] 7.0.0-rc.1.22426.10 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T04:28:41.002 [Information] Learn about framework resolution:
2022-10-26T04:28:41.003 [Error] https://aka.ms/dotnet/app-launch-failed
2022-10-26T04:28:41.014 [Error] Exceeded language worker restart retry count for runtime:dotnet-isolated. Shutting down and proactively recycling the Functions Host to recover
2022-10-26T04:28:41.046 [Information] To install missing framework, download:
2022-10-26T04:28:41.046 [Information] https://aka.ms/dotnet-core-applaunch?framework=Microsoft.NETCore.App&framework_version=7.0.0-rc.2.22472.3&arch=x86&rid=win10-x86
2022-10-26T04:28:46.129 [Information] Stopping JobHost
2022-10-26T04:28:46.131 [Information] Job host stopped
2022-10-26T04:29:58  No new trace in the past 1 min(s).
```
