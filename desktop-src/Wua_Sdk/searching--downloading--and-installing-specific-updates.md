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
# <a name="searching-downloading-and-installing-specific-updates"></a>搜尋、下載及安裝特定更新

本主題中的腳本範例說明如何使用 Windows Update Agent (WUA) 來掃描、下載及安裝特定更新。 更新可以依其標題來指定。

此範例會搜尋特定的軟體更新、下載更新，然後安裝更新。 例如，使用者可以使用這個方法來判斷電腦上是否已安裝重大安全性更新。 如果未安裝更新，使用者可以確保下載並安裝更新。 使用者也可以確保他們會收到安裝狀態的通知。

範例更新是以 [**IUpdate 的 Title 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title)中的更新標題來識別。 此範例中所建議的更新標題為「Windows 的更新 Rights Management 用戶端1.0」。

> [!Note]  
> 如需有關如何搜尋、下載及安裝適用于特定應用程式之所有更新的資訊，請參閱 [搜尋、下載及安裝更新](searching--downloading--and-installing-updates.md)。

 

在您嘗試執行此範例之前，請注意下列事項：

-   電腦上必須安裝 WUA。 如需如何判斷已安裝之 WUA 版本的詳細資訊，請參閱 [判斷 wua 的目前版本](determining-the-current-version-of-wua.md)。
-   此範例不會提供自己的使用者介面。 如果更新需要重新開機，WUA 會提示使用者重新開機電腦。
-   此範例只能從 WUA 下載更新。 它無法從軟體更新服務 (SUS) 1.0 伺服器下載更新。
-   執行此範例需要 Windows Script Host (WSH) 。 如需有關 WSH 的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 的 WSH 區段。 如果將範例複製到名為 WUASpecificUpdate.vbs 的檔案 \_ ，您可以藉由開啟命令提示字元視窗並輸入下列命令來執行它： **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>範例

> [!IMPORTANT]
> 此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。 此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。

 


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



 

 



