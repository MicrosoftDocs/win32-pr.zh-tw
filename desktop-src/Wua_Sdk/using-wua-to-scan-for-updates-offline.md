---
description: Windows Update Agent (WUA) 可以用來掃描電腦是否有安全性更新，而不需連線到 Windows Update 或 Windows Server Update Services (WSUS) 伺服器，這可讓未連線至網際網路的電腦進行安全性更新的掃描。 離線掃描更新需要從 Windows Update 下載已簽署的檔案（Wsusscn2.cab）。
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: 使用 WUA 離線掃描更新
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318064"
---
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="f0978-104">使用 WUA 離線掃描更新</span><span class="sxs-lookup"><span data-stu-id="f0978-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="f0978-105">Windows Update Agent (WUA) 可以用來掃描電腦是否有安全性更新，而不需連線到 Windows Update 或 Windows Server Update Services (WSUS) 伺服器，這可讓未連線至網際網路的電腦進行安全性更新的掃描。</span><span class="sxs-lookup"><span data-stu-id="f0978-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="f0978-106">離線掃描更新需要從 Windows Update 下載已簽署的檔案（Wsusscn2.cab）。</span><span class="sxs-lookup"><span data-stu-id="f0978-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="f0978-107">Wsusscn2.cab 檔案是由 Microsoft 簽署的封包檔。</span><span class="sxs-lookup"><span data-stu-id="f0978-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="f0978-108">此檔案包含 Microsoft 所發行之安全性相關更新的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f0978-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="f0978-109">您可以掃描未連線至網際網路的電腦，以查看這些安全性相關的更新是否存在或為必要。</span><span class="sxs-lookup"><span data-stu-id="f0978-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="f0978-110">Wsusscn2.cab 檔案本身不包含安全性更新，因此您必須透過其他方式取得和安裝任何所需的安全性相關更新。</span><span class="sxs-lookup"><span data-stu-id="f0978-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="f0978-111">在 Windows Update 網站上發行、移除或修改安全性相關的更新時，會定期發行 Wsusscn2.cab 檔案的新版本。</span><span class="sxs-lookup"><span data-stu-id="f0978-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="f0978-112">您可以從下列位置下載最新的 Wsusscn2.cab 檔案： [下載 Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="f0978-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="f0978-113">當您下載最新的 Wsusscn2.cab 之後，就可以將檔案提供給 [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) 方法，然後使用 WUA API 來搜尋離線電腦以取得安全性更新。</span><span class="sxs-lookup"><span data-stu-id="f0978-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="f0978-114">WUA 會驗證 Wsusscn2.cab 是由有效的 Microsoft 憑證簽署，然後再執行離線掃描。</span><span class="sxs-lookup"><span data-stu-id="f0978-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="f0978-115">根據我們的 [sha-1 淘汰計畫](https://aka.ms/sha1deprecation)，Wsusscn2.cab 檔案不再使用 SHA-1 和 sha-1 雜湊演算法套件進行雙重簽署， (特別是 sha-256) 。</span><span class="sxs-lookup"><span data-stu-id="f0978-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="f0978-116">這個檔案現在只會使用 SHA-256 進行簽署。</span><span class="sxs-lookup"><span data-stu-id="f0978-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="f0978-117">確認此檔案上數位簽章的系統管理員現在應該只預期單一的 SHA-256 簽章。</span><span class="sxs-lookup"><span data-stu-id="f0978-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="f0978-118">範例</span><span class="sxs-lookup"><span data-stu-id="f0978-118">Example</span></span>

<span data-ttu-id="f0978-119">下列範例會使用 Wsusscn2.cab 檔案來掃描電腦，並顯示遺失的更新。</span><span class="sxs-lookup"><span data-stu-id="f0978-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0978-120">此腳本旨在示範如何使用 Windows Update 代理程式 Api，並提供開發人員如何使用這些 Api 來解決問題的範例。</span><span class="sxs-lookup"><span data-stu-id="f0978-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="f0978-121">此腳本並不是用來作為生產程式碼，而且 Microsoft (不支援腳本本身，不過) 支援基礎 Windows Update 代理程式 Api。</span><span class="sxs-lookup"><span data-stu-id="f0978-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



