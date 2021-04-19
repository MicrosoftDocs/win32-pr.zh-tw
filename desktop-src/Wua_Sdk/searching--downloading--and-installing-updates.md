---
description: 本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 來掃描、下載及安裝更新。
ms.assetid: 4b2b1898-64f1-4908-98b7-ea87a6fcb71d
title: 搜尋、下載及安裝更新
ms.topic: article
ms.date: 01/16/2020
ms.openlocfilehash: 289e0535bc39ca3fb39ddb33bbc67d009898b556
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106976530"
---
# <a name="searching-downloading-and-installing-updates"></a><span data-ttu-id="c79b8-103">搜尋、下載及安裝更新</span><span class="sxs-lookup"><span data-stu-id="c79b8-103">Searching, Downloading, and Installing Updates</span></span>

<span data-ttu-id="c79b8-104">本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 來掃描、下載及安裝更新。</span><span class="sxs-lookup"><span data-stu-id="c79b8-104">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to scan, download, and install updates.</span></span>

<span data-ttu-id="c79b8-105">此範例會搜尋所有適用的軟體更新，然後列出這些更新。</span><span class="sxs-lookup"><span data-stu-id="c79b8-105">The sample searches for all the applicable software updates and then lists those updates.</span></span> <span data-ttu-id="c79b8-106">接下來，它會建立要下載的更新集合，然後加以下載。</span><span class="sxs-lookup"><span data-stu-id="c79b8-106">Next, it creates a collection of updates to download and then downloads them.</span></span> <span data-ttu-id="c79b8-107">最後，它會建立要安裝的更新集合，然後加以安裝。</span><span class="sxs-lookup"><span data-stu-id="c79b8-107">Finally, it creates a collection of updates to install and then installs them.</span></span>

<span data-ttu-id="c79b8-108">如果您想要使用更新標題來搜尋、下載及安裝您識別的特定更新，請參閱 [搜尋、下載及安裝特定](searching--downloading--and-installing-specific-updates.md)更新。</span><span class="sxs-lookup"><span data-stu-id="c79b8-108">If you want to search, download, and install a specific update that you identify by using the update title, see [Searching, Downloading, and Installing Specific Updates](searching--downloading--and-installing-specific-updates.md).</span></span>

<span data-ttu-id="c79b8-109">在您嘗試執行此範例之前，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="c79b8-109">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="c79b8-110">電腦上必須安裝 WUA。</span><span class="sxs-lookup"><span data-stu-id="c79b8-110">WUA must be installed on the computer.</span></span> <span data-ttu-id="c79b8-111">如需如何判斷已安裝之 WUA 版本的詳細資訊，請參閱 [判斷 wua 的目前版本](determining-the-current-version-of-wua.md)。</span><span class="sxs-lookup"><span data-stu-id="c79b8-111">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="c79b8-112">此範例只能使用 WUA 來下載更新。</span><span class="sxs-lookup"><span data-stu-id="c79b8-112">The sample can download updates only by using WUA.</span></span> <span data-ttu-id="c79b8-113">它無法從軟體更新服務 (SUS) 1.0 伺服器下載更新。</span><span class="sxs-lookup"><span data-stu-id="c79b8-113">It cannot download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="c79b8-114">執行此範例需要 Windows Script Host (WSH) 。</span><span class="sxs-lookup"><span data-stu-id="c79b8-114">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="c79b8-115">如需有關 WSH 的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 的 WSH 區段。</span><span class="sxs-lookup"><span data-stu-id="c79b8-115">For more information about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="c79b8-116">如果將範例複製到名為 WUASearchDownloadInstall.vbs 的檔案 \_ ，您可以藉由開啟命令提示字元視窗，然後在命令提示字元中輸入下列命令，來執行此範例。</span><span class="sxs-lookup"><span data-stu-id="c79b8-116">If the sample is copied to a file named WUA\_SearchDownloadInstall.vbs, you can run the sample by opening a Command Prompt window and typing the following command at the command prompt.</span></span>

    <span data-ttu-id="c79b8-117">**cscript WUA \_SearchDownloadInstall.vbs**</span><span class="sxs-lookup"><span data-stu-id="c79b8-117">**cscript WUA\_SearchDownloadInstall.vbs**</span></span>

## <a name="example"></a><span data-ttu-id="c79b8-118">範例</span><span class="sxs-lookup"><span data-stu-id="c79b8-118">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c79b8-119">此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。</span><span class="sxs-lookup"><span data-stu-id="c79b8-119">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="c79b8-120">此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。</span><span class="sxs-lookup"><span data-stu-id="c79b8-120">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Option Explicit

WScript.Echo "This script is provided by Microsoft Corporation to demonstrate techniques that can be used to search, download,"
WScript.Echo "and install updates through the Windows Update Agent API."
WScript.Echo ""
WScript.Echo "This script is not intended as production code."
WScript.Echo ""

' Supported parameters:
'    /AppName: Name to pass to the WUA API as the 'calling application';
'             this appears in the Windows Update logs
'             Default: "WUA API Sample Script"
'    /Criteria: Search criteria to be used (see the WUA documentation for
'             IUpdateSearcher::BeginSearch for examples)
'             Default: Search for all non-installed, non-hidden software
'    /Automate: Don't prompt the user for various actions
'             Default: Prompt the user
'    /IgnoreSupersedence: Display all applicable updates, even those
'             superseded by newer updates
'             Default: Ignore supersedes updates
'    /Offline: Path to WSUSSCN2.cab file that should be used for offline sync
'             Default: Don't do offline sync
'    /Service: Update service that script should scan against
'             Available values: WU, MU, WSUS, DCAT, STORE, or an
'             identifying GUID of another service
'             Default: Default service (WSUS if machine is configured to
'                 use it, or MU if opted in, or WU otherwise)
'             Ignored if /Offline is set
'    /Hide: Hide updates found by the scan. Hidden updates will not
'             normally be installed by Automatic Updates.
'    /Show: Unhide any hidden updates found by the scan.
'    /NoDownload: Do not download any updates that the scan detects
'    /NoInstall: Do not install any updates that the scan detects
'    /ShowDetails: Show details about the updates found by the scan
'    /ShowBundle: Output information about the child updates in the 
'             bundled updates that are found
'    /RebootToComplete: Restart the computer if necessary to complete
'             installation

Function InstallationResultToText(result)
    Select Case result
        Case 2
            InstallationResultToText = "Succeeded"
        Case 3
            InstallationResultToText = "Succeeded with errors"
        Case 4
            InstallationResultToText = "Failed"
        Case 5
            InstallationResultToText = "Cancelled"
        Case Else
            InstallationResultToText = "Unexpected (" & result & ")"
    End Select
End Function

Function DeploymentActionToText(action)
    Select Case action
        Case 0
            DeploymentActionToText = "None (Inherit)"
        Case 1
            DeploymentActionToText = "Installation"
        Case 2
            DeploymentActionToText = "Uninstallation"
        Case 3
            DeploymentActionToText = "Detection"
        Case 4
            DeploymentActionToText = "Optional Installation"
        Case Else
            DeploymentActionToText = "Unexpected (" & action & ")"
    End Select
End Function


Function UpdateDescription(update)
    Dim description
    Dim I
    Dim category
    description = update.Title & " {" & update.Identity.UpdateID & "." & update.Identity.RevisionNumber & "}"
    If update.IsHidden Then
        description = description & " (hidden)"
    End If
    If WScript.Arguments.Named.Exists("ShowDetails") Then
        if update.KBArticleIDs.Count > 0 Then
            description = description & " ("
            For I = 0 To update.KBArticleIDs.Count -1
                If I > 0 Then
                    description = description & ","
                End If
                description = description & "KB" & update.KBArticleIDs.Item(I)
            Next
            description = description & ")"
        End If
        description = description & " Categories: "
        For I = 0 to update.Categories.Count - 1
            Set category = update.Categories.Item(I)
            If I > 0 Then
                description = description & ","
            End If
            description = description & category.Name & " {" & category.CategoryID & "}"
        Next
        description = description & " Deployment action: " & DeploymentActionToText(update.DeploymentAction)
    End If
    UpdateDescription = description
End Function

Dim appName
If WScript.Arguments.Named.Exists("AppName") Then
    appName = WScript.Arguments.Named.Item("AppName")
Else
    appName = "WUA API Sample Script"
End If

Dim criteria
If WScript.Arguments.Named.Exists("Criteria") Then
    criteria = WScript.Arguments.Named.Item("Criteria")
Else
    criteria = "IsInstalled=0 and Type='Software' and IsHidden=0"
End If

Dim isAutomated
isAutomated = WScript.Arguments.Named.Exists("Automate")

Dim ignoreSupersedence
ignoreSupersedence = WScript.Arguments.Named.Exists("IgnoreSupersedence")

Dim showBundle
showBundle = WScript.Arguments.Named.Exists("ShowBundle")

Dim serverSelection
Dim serviceId
serverSelection = 0
serviceId = ""

If WScript.Arguments.Named.Exists("Service") Then
    Select Case UCase(WScript.Arguments.Named.Item("Service"))
        Case "WU"
            serverSelection = 2
        Case "MU"
            serverSelection = 3
            serviceId = "7971f918-a847-4430-9279-4a52d1efe18d"
        Case "WSUS"
            serverSelection = 1
        case "DCAT"
            serverSelection = 3
            serviceId = "855E8A7C-ECB4-4CA3-B045-1DFA50104289"
        case "STORE"
            serverSelection = 3
            serviceId = "117cab2d-82b1-4b5a-a08c-4d62dbee7782"
        Case Else
            serverSelection = 3
            serviceId = WScript.Arguments.Named.Item("Service")
    End Select
End If

Dim noDownload
noDownload = WScript.Arguments.Named.Exists("NoDownload")

Dim noInstall
noInstall = WScript.Arguments.Named.Exists("NoInstall")

Dim hide
hide = WScript.Arguments.Named.Exists("Hide")

Dim show
show = WScript.Arguments.Named.Exists("Show")

Dim strInput
strInput = ""

Dim returnValue
returnValue = 0

Dim automaticUpdates
Dim updateSettings
Dim objWMIService
Dim colListOfServices
Dim objService

Dim secondInstallPass
secondInstallPass = false

Dim updateSession
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = appName

Dim updateServiceManager
Dim offlineService
If WScript.Arguments.Named.Exists("Offline") Then
    Set updateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
    Set offlineService = updateServiceManager.AddScanPackageService(appName, WScript.Arguments.Named.Item("Offline"), 0)
    serverSelection = 3
    serviceId = offlineService.ServiceID
    WScript.Echo "Registered offline scan cab, service ID " & serviceId & vbCRLF
End If
    
Dim updateSearcher
Set updateSearcher = updateSession.CreateUpdateSearcher()
updateSearcher.ServerSelection = serverSelection
If serverSelection = 3 Then
    updateSearcher.ServiceId = serviceId
End If
If ignoreSupersedence Then
    updateSearcher.IncludePotentiallySupersededUpdates = true
End If

WScript.Echo "Searching for updates..." & vbCRLF

Dim searchResult
Set searchResult = updateSearcher.Search(criteria)

WScript.Echo "List of applicable items found on the machine:"

Dim I
Dim B
For I = 0 To searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & UpdateDescription(update)
    If showBundle Then
        For B = 0 to update.BundledUpdates.Count-1
            WScript.Echo I+1 & "> " & B+1 & "> " & UpdateDescription(update.BundledUpdates.Item(B))
        Next
    End If
Next

Dim updatesToDownload
Set updatesToDownload = CreateObject("Microsoft.Update.UpdateColl")

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
Else
    WScript.Echo vbCRLF & "Checking search results:"

    Dim update
    Dim description
    Dim addThisUpdate
    Dim hideThisUpdate
    Dim showThisUpdate
    Dim atLeastOneAdded
    Dim propertyTest
    atLeastOneAdded = false
    Dim exclusiveAdded
    exclusiveAdded = false
    If noDownload And Not hide And Not show Then
        WScript.Echo "Skipping downloads as requested."
    Else
        For I = 0 to searchResult.Updates.Count-1
            Set update = searchResult.Updates.Item(I)
            description = UpdateDescription(update)
            addThisUpdate = false
            If hide And Not update.IsHidden Then
                strInput = "Y"
                If Not isAutomated Then
                    WScript.Echo I + 1 & "> : " & description  & _
                    " is now shown; do you want to hide it? ([Y]/N)"
                    strInput = WScript.StdIn.Readline
                    WScript.Echo
                End If
                If (strInput = "Y" or strInput = "y") Then
                    WScript.Echo "Hiding update"
                    update.IsHidden = true
                End If
            ElseIf show And update.IsHidden Then
                strInput = "Y"
                If Not isAutomated Then
                    WScript.Echo I + 1 & "> : " & description  & _
                    " is now hidden; do you want to show it? ([Y]/N)"
                    strInput = WScript.StdIn.Readline
                    WScript.Echo
                End If
                If (strInput = "Y" or strInput = "y") Then
                    WScript.Echo "Showing update"
                    update.IsHidden = false
                End If
            End If
                
            If exclusiveAdded Then
                WScript.Echo I + 1 & "> skipping: " & description & _
                    " because an exclusive update has already been selected"
            ElseIf Not noDownload Then
                propertyTest = false
                On Error Resume Next
                propertyTest = update.InstallationBehavior.CanRequestUserInput
                On Error GoTo 0
                If propertyTest = true Then
                    WScript.Echo I + 1 & "> skipping: " & description  & _
                    " because it requires user input"
                Else
                    propertyTest = true
                    On Error Resume Next
                    propertyTest = update.EulaAccepted
                    On Error GoTo 0
                    If propertyTest = false Then
                        If isAutomated Then
                            WScript.Echo I + 1 & "> skipping: " & description  & _
                            " because it has a license agreement that has not been accepted"
                        Else
                            WScript.Echo I + 1 & "> note: " & description  & _
                            " has a license agreement that must be accepted:"
                            WScript.Echo update.EulaText
                            WScript.Echo "Do you accept this license agreement? (Y/[N])"
                            strInput = WScript.StdIn.Readline
                            WScript.Echo 
                            If (strInput = "Y" or strInput = "y") Then
                                update.AcceptEula()
                                addThisUpdate = true
                            Else
                                WScript.Echo I + 1 & "> skipping: " & description  & _
                                " because the license agreement was declined"
                            End If
                        End If
                    Else
                        addThisUpdate = true
                    End If
                End If
                If addThisUpdate Then
                    propertyTest = 0
                    On Error Resume Next
                    propertyTest = update.InstallationBehavior.Impact
                    On Error GoTo 0
                    If propertyTest = 2 Then
                        If atLeastOneAdded Then
                            WScript.Echo I + 1 & "> skipping: " & description  & _
                            " because it is exclusive and other updates are being installed first"
                            addThisUpdate = false
                        End If
                    End If
                End If
                If addThisUpdate Then
                    If Not isAutomated Then
                        WScript.Echo I + 1 & "> : " & description  & _
                        " is applicable; do you want to install it? ([Y]/N)"
                        strInput = WScript.StdIn.Readline
                        WScript.Echo
                        If (strInput = "N" or strInput = "n") Then
                            WScript.Echo "Skipping update"
                            addThisUpdate = false
                       End If
                    End If
                End If
                If addThisUpdate Then
                    WScript.Echo I + 1 & "> adding: " & description  
                    updatesToDownload.Add(update)
                    atLeastOneAdded = true
                    On Error Resume Next
                    propertyTest = update.InstallationBehavior.Impact
                    On Error GoTo 0
                    If propertyTest = 2 Then
                        WScript.Echo "This update is exclusive; skipping remaining updates"
                        exclusiveAdded = true
                    End If
                End If
            End If
        Next
    End If
End If

Dim updatesToInstall
Set updatesToInstall = CreateObject("Microsoft.Update.UpdateColl")

Dim rebootMayBeRequired
rebootMayBeRequired = false

If (Not noDownload) And (updatesToDownload.Count > 0) Then
    WScript.Echo vbCRLF & "Downloading updates..."

    Dim downloader
    Set downloader = updateSession.CreateUpdateDownloader() 
    downloader.Updates = updatesToDownload
    downloader.Download()

    WScript.Echo vbCRLF & "Successfully downloaded updates:"

    For I = 0 To updatesToDownload.Count-1
        Set update = updatesToDownload.Item(I)
        If update.IsDownloaded = true Then
            WScript.Echo I + 1 & "> " & UpdateDescription(update) 
            updatesToInstall.Add(update) 
            propertyTest = 0
            On Error Resume Next
            propertyTest = update.InstallationBehavior.RebootBehavior
            On Error GoTo 0
            If propertyTest > 0 Then
                rebootMayBeRequired = true
            End If
        End If
    Next
End If

strInput = "N"
If noInstall Then
    WScript.Echo "Skipping install as requested."
Else
    If updatesToInstall.Count > 0 Then
        strInput = "Y"
        If rebootMayBeRequired = true Then
            WScript.Echo vbCRLF & "These updates may require a reboot."
        End If
        If Not isAutomated Then
            WScript.Echo  vbCRLF & "Would you like to install updates now? (Y/[N])"
            strInput = WScript.StdIn.Readline
            WScript.Echo 
        End If
    End If

    If (strInput = "Y" or strInput = "y") Then
        WScript.Echo "Installing updates..."
        Dim installer
        Set installer = updateSession.CreateUpdateInstaller()
        installer.Updates = updatesToInstall
        Dim installationResult
        Set installationResult = installer.Install()
 
        returnValue = 1
        'Output results of install
        WScript.Echo "Installation Result: " & _
        InstallationResultToText(installationResult.ResultCode) 
        WScript.Echo "Reboot Required: " & _ 
        installationResult.RebootRequired & vbCRLF 
        WScript.Echo "Listing of updates installed " & _
        "and individual installation results:" 
 
        For I = 0 to updatesToInstall.Count - 1
            WScript.Echo I + 1 & "> " & _
            UpdateDescription(updatesToInstall.Item(i)) & ": " & _
            InstallationResultToText(installationResult.GetUpdateResult(I).ResultCode) & _
            " HRESULT: " & installationResult.GetUpdateResult(I).HResult
            If installationResult.GetUpdateResult(I).HResult = -2145116147 Then
                WScript.Echo "An update needed additional downloaded content. Please rerun the script."
            End If
        Next
       
        If installationResult.RebootRequired And WScript.Arguments.Named.Exists("RebootToComplete") Then
            strInput = "Y"
            If Not isAutomated Then
                WScript.Echo  vbCRLF & "Would you like to reboot now to complete the installation? (Y/[N])"
                strInput = WScript.StdIn.Readline
                WScript.Echo 
            End If
            If (strInput = "Y" or strInput = "y") Then
                WScript.Echo "Committing installation..." & vbCRLF
                installer.Commit(0)
                WScript.Echo "Triggering restart in 30 seconds..." & vbCRLF
                Dim oShell
                Set oShell = WScript.CreateObject("WScript.Shell")
                oShell.Run "shutdown /r /t 30", 1
            End If     
        End If
    End If
End If

WScript.Quit (returnValue)
```



 

 



