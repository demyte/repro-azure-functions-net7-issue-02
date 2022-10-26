# Commands Used

`az group create --name rg-func-test --location "Australia East"`

`az storage account create --name storfunctestjs --location "Australia East" --resource-group rg-func-test --sku Standard_LRS`

A:
`az functionapp create --resource-group rg-func-test --consumption-plan-location "AustraliaEast" --runtime dotnet-isolated --functions-version 4 --name func-test-js --storage-account storfunctestjs`

B:
`az functionapp create --resource-group rg-func-test --consumption-plan-location "AustraliaEast" --runtime dotnet-isolated --runtime-version 7 --functions-version 4 --os-type Windows --name func-test-js --storage-account storfunctestjs --https-only`

`func azure functionapp publish func-test-js`

`func azure functionapp logstream func-test-js`

```
Retrieving Function App...
2022-10-26T03:54:21  Welcome, you are now connected to log-streaming service. The default timeout is 2 hours. Change the timeout with the App Setting SCM_LOGSTREAM_TIMEOUT (in seconds).
2022-10-26T03:54:25.495 [Information] You must install or update .NET to run this application.
2022-10-26T03:54:25.498 [Information] App: C:\home\site\wwwroot\Func1.dll
2022-10-26T03:54:25.498 [Information] Architecture: x86
2022-10-26T03:54:25.498 [Information] Framework: 'Microsoft.NETCore.App', version '7.0.0-rc.2.22472.3' (x86)
2022-10-26T03:54:25.498 [Information] .NET location: C:\Program Files (x86)\dotnet\
2022-10-26T03:54:25.498 [Information] The following frameworks were found:
2022-10-26T03:54:25.498 [Information] 1.0.16 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.499 [Information] 1.1.13 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 2.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 2.1.30 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 2.2.14 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 3.0.3 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 3.1.28 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 3.1.29 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 5.0.15 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 5.0.17 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.504 [Information] 6.0.8 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.505 [Information] 6.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.505 [Information] 7.0.0-rc.1.22426.10 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:25.505 [Information] Learn about framework resolution:
2022-10-26T03:54:25.505 [Error] https://aka.ms/dotnet/app-launch-failed
2022-10-26T03:54:25.521 [Error] Exceeded language worker restart retry count for runtime:dotnet-isolated. Shutting down and proactively recycling the Functions Host to recover
2022-10-26T03:54:25.607 [Information] To install missing framework, download:
2022-10-26T03:54:25.607 [Information] https://aka.ms/dotnet-core-applaunch?framework=Microsoft.NETCore.App&framework_version=7.0.0-rc.2.22472.3&arch=x86&rid=win10-x86
2022-10-26T03:54:29.322 [Information] Stopping JobHost
2022-10-26T03:54:29.322 [Information] Job host stopped
2022-10-26T03:54:32.135 [Error] Exceeded language worker restart retry count for runtime:dotnet-isolated. Shutting down and proactively recycling the Functions Host to recover
2022-10-26T03:54:32.088 [Information] You must install or update .NET to run this application.
2022-10-26T03:54:32.089 [Information] App: C:\home\site\wwwroot\Func1.dll
2022-10-26T03:54:32.089 [Information] Architecture: x86
2022-10-26T03:54:32.089 [Information] Framework: 'Microsoft.NETCore.App', version '7.0.0-rc.2.22472.3' (x86)
2022-10-26T03:54:32.090 [Information] .NET location: C:\Program Files (x86)\dotnet\
2022-10-26T03:54:32.090 [Information] The following frameworks were found:
2022-10-26T03:54:32.090 [Information] 1.0.16 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.091 [Information] 1.1.13 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.092 [Information] 2.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.092 [Information] 2.1.30 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.093 [Information] 2.2.14 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 3.0.3 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 3.1.28 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 3.1.29 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 5.0.15 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 5.0.17 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 6.0.8 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 6.0.9 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] 7.0.0-rc.1.22426.10 at [C:\Program Files (x86)\dotnet\shared\Microsoft.NETCore.App]
2022-10-26T03:54:32.130 [Information] Learn about framework resolution:
2022-10-26T03:54:32.130 [Error] https://aka.ms/dotnet/app-launch-failed
2022-10-26T03:54:32.305 [Information] Stopping JobHost
2022-10-26T03:54:32.305 [Information] Job host stopped
2022-10-26T03:56:21  No new trace in the past 1 min(s).
```
