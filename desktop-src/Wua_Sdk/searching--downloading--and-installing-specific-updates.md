---
description: 本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 來掃描、下載及安裝特定更新。 更新可以依其標題來指定。
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: 搜尋、下載及安裝特定更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318499"
---
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="116c9-104">搜尋、下載及安裝特定更新</span><span class="sxs-lookup"><span data-stu-id="116c9-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="116c9-105">本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 來掃描、下載及安裝特定更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="116c9-106">更新可以依其標題來指定。</span><span class="sxs-lookup"><span data-stu-id="116c9-106">The update can be specified by its title.</span></span>

<span data-ttu-id="116c9-107">此範例會搜尋特定的軟體更新、下載更新，然後安裝更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="116c9-108">例如，使用者可以使用這個方法來判斷電腦上是否已安裝重大安全性更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="116c9-109">如果未安裝更新，使用者可以確保下載並安裝更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="116c9-110">使用者也可以確保他們會收到安裝狀態的通知。</span><span class="sxs-lookup"><span data-stu-id="116c9-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="116c9-111">範例更新是以 [**IUpdate 的 Title 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)中的更新標題來識別。</span><span class="sxs-lookup"><span data-stu-id="116c9-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="116c9-112">此範例中所建議的更新標題為「Windows 的更新 Rights Management 用戶端1.0」。</span><span class="sxs-lookup"><span data-stu-id="116c9-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="116c9-113">如需有關如何搜尋、下載及安裝適用于特定應用程式之所有更新的資訊，請參閱 [搜尋、下載及安裝更新](searching--downloading--and-installing-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="116c9-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="116c9-114">在您嘗試執行此範例之前，請注意下列事項：</span><span class="sxs-lookup"><span data-stu-id="116c9-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="116c9-115">電腦上必須安裝 WUA。</span><span class="sxs-lookup"><span data-stu-id="116c9-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="116c9-116">如需如何判斷已安裝之 WUA 版本的詳細資訊，請參閱 [判斷 wua 的目前版本](determining-the-current-version-of-wua.md)。</span><span class="sxs-lookup"><span data-stu-id="116c9-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="116c9-117">此範例不會提供自己的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="116c9-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="116c9-118">如果更新需要重新開機，WUA 會提示使用者重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="116c9-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="116c9-119">此範例只能從 WUA 下載更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="116c9-120">它無法從軟體更新服務 (SUS) 1.0 伺服器下載更新。</span><span class="sxs-lookup"><span data-stu-id="116c9-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="116c9-121">執行此範例需要 Windows Script Host (WSH) 。</span><span class="sxs-lookup"><span data-stu-id="116c9-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="116c9-122">如需有關 WSH 的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 的 WSH 區段。</span><span class="sxs-lookup"><span data-stu-id="116c9-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="116c9-123">如果將範例複製到名為 WUASpecificUpdate.vbs 的檔案 \_ ，您可以藉由開啟命令提示字元視窗並輸入下列命令來執行它： **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="116c9-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="116c9-124">範例</span><span class="sxs-lookup"><span data-stu-id="116c9-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="116c9-125">此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。</span><span class="sxs-lookup"><span data-stu-id="116c9-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="116c9-126">此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。</span><span class="sxs-lookup"><span data-stu-id="116c9-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



