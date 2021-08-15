---
description: Windows更新代理程式 (WUA) 可以用來掃描電腦是否有安全性更新，而不需連線到 Windows Update 或 Windows Server Update Services (WSUS) 伺服器，這可讓未連線至網際網路的電腦進行安全性更新的掃描。 離線掃描更新需要從 Windows Update 下載已簽署的檔案（Wsusscn2.cab）。
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: 使用 WUA 離線掃描更新
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 54da554eca4e2320ecb8644ffb7ae274ed929d897f6e17e28b271a682f9fdc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410758"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>使用 WUA 離線掃描更新

Windows更新代理程式 (WUA) 可以用來掃描電腦是否有安全性更新，而不需連線到 Windows Update 或 Windows Server Update Services (WSUS) 伺服器，這可讓未連線至網際網路的電腦進行安全性更新的掃描。

離線掃描更新需要從 Windows Update 下載已簽署的檔案（Wsusscn2.cab）。

Wsusscn2.cab 檔案是由 Microsoft 簽署的封包檔。 此檔案包含 Microsoft 所發行之安全性相關更新的相關資訊。 您可以掃描未連線至網際網路的電腦，以查看這些安全性相關的更新是否存在或為必要。 Wsusscn2.cab 檔案本身不包含安全性更新，因此您必須透過其他方式取得和安裝任何所需的安全性相關更新。 在 Windows Update 網站上發行、移除或修改安全性相關的更新時，會定期發行 Wsusscn2.cab 檔案的新版本。 您可以從下列位置下載最新的 Wsusscn2.cab 檔案： [下載 Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

當您下載最新的 Wsusscn2.cab 之後，就可以將檔案提供給 [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) 方法，然後使用 WUA API 來搜尋離線電腦以取得安全性更新。 WUA 會驗證 Wsusscn2.cab 是由有效的 Microsoft 憑證簽署，然後再執行離線掃描。

> [!NOTE]
> 根據我們的 [sha-1 淘汰計畫](https://aka.ms/sha1deprecation)，Wsusscn2.cab 檔案不再使用 SHA-1 和 sha-1 雜湊演算法套件進行雙重簽署， (特別是 sha-256) 。 這個檔案現在只會使用 SHA-256 進行簽署。 確認此檔案上數位簽章的系統管理員現在應該只預期單一的 SHA-256 簽章。

## <a name="example"></a>範例

下列範例會使用 Wsusscn2.cab 檔案來掃描電腦，並顯示遺失的更新。

> [!IMPORTANT]
> 此腳本旨在示範如何使用 Windows Update 代理程式 api，並提供開發人員如何使用這些 api 來解決問題的範例。 此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 api。

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



