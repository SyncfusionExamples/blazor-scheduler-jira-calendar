# Blazor Scheduler with JIRA Calendar

This project contains that adding the JIRA calendar with Blazor Scheduler.

## Prerequisites

* Visual Studio 2022
* Visual Studio Code

## How to run the project

* Checkout this project to a location in your disk.
* Open the solution file using the Visual Studio 2022.
* Restore the NuGet packages by rebuilding the solution.
* Run the project.

To run this application, we have to add JIRA credentials and Rest API url in OnInitializedAsync method in Index.razor file.

## Add Credentials

Refer [link](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/)   to generate the token from your Atlassian account. 

Once token generated, specify your attlassian mail id and token in [Index page](https://github.com/SyncfusionExamples/blazor-scheduler-jira-calendar/blob/main/Pages/Index.razor#L81).

```
var byteArray = new UTF8Encoding().GetBytes("abc@xyz.com:qwertyuiop");
```

## Add Rest API Url

Add your Rest API Url string in [http request](https://github.com/SyncfusionExamples/blazor-scheduler-jira-calendar/blob/main/Pages/Index.razor#L83).

```
new HttpRequestMessage(HttpMethod.Get, "https://api.atlassian.com/ex/jira/:cloudId:/rest/agile/1.0/sprint/20387/issue")
```
