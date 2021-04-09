---
description: Windows 資源保護 (WRP) 防止取代安裝為 Windows Vista 或 Windows Server 2008 一部分的基本系統檔案、資料夾和登錄機碼。
ms.assetid: 1cb67b4a-dc75-4bd7-b314-d695c10d5558
title: 偵測資源取代
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1855b98ca5834ef9e13e2f48bf7cca492e94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694648"
---
# <a name="detecting-resource-replacement"></a><span data-ttu-id="235c3-103">偵測資源取代</span><span class="sxs-lookup"><span data-stu-id="235c3-103">Detecting Resource Replacement</span></span>

<span data-ttu-id="235c3-104">Windows 資源保護 (WRP) 防止取代安裝為 Windows Vista 或 Windows Server 2008 一部分的基本系統檔案、資料夾和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="235c3-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of Windows Vista or Windows Server 2008.</span></span>

<span data-ttu-id="235c3-105">WRP 藉由偵測並防止嘗試取代受保護的資源，來保護 Windows Vista 或 Windows Server 2008 上的檔案、資料夾和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="235c3-105">WRP protects files, folders, and registry keys on Windows Vista or Windows Server 2008 by detecting and preventing attempts to replace protected resources.</span></span> <span data-ttu-id="235c3-106">這項保護是根據 Windows 任意存取控制清單 (DACL) 和存取控制清單 (針對受保護資源定義的 ACL) 。</span><span class="sxs-lookup"><span data-stu-id="235c3-106">This protection is based on a Windows discretionary access control list (DACL) and access control lists (ACL) defined for protected resources.</span></span> <span data-ttu-id="235c3-107">修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。</span><span class="sxs-lookup"><span data-stu-id="235c3-107">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="235c3-108">WRP 保護的資源只能使用 [支援的資源取代機制](supported-file-replacement-mechanisms.md) 與 Windows 模組安裝程式服務進行變更。</span><span class="sxs-lookup"><span data-stu-id="235c3-108">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="235c3-109">嘗試修改受 WRP 保護之資源的應用程式永遠不會變更資源，而且可能會收到錯誤訊息，指出已拒絕資源的存取權。</span><span class="sxs-lookup"><span data-stu-id="235c3-109">Applications attempting to modify a WRP-protected resource never change the resource and may receive an error message that states that access to the resource was denied.</span></span>

<span data-ttu-id="235c3-110">應用程式和安裝程式可以使用 [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 和 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) 函數來判斷檔案或登錄機碼是否受到保護。</span><span class="sxs-lookup"><span data-stu-id="235c3-110">Applications and installers can use the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) functions to determine whether a file or registry key is protected.</span></span>

<span data-ttu-id="235c3-111">\* \* Windows Server 2003 和 Windows XP： \* \*</span><span class="sxs-lookup"><span data-stu-id="235c3-111">\*\*Windows Server 2003 and Windows XP:  \*\*</span></span>

<span data-ttu-id="235c3-112">Windows 檔案保護 (WFP) 藉由偵測取代受保護系統檔案的嘗試來保護系統檔案。</span><span class="sxs-lookup"><span data-stu-id="235c3-112">Windows File Protection (WFP) protects system files by detecting attempts to replace protected system files.</span></span> <span data-ttu-id="235c3-113">當 WFP 收到受保護目錄中檔案的目錄變更通知之後，就會觸發這項保護。</span><span class="sxs-lookup"><span data-stu-id="235c3-113">This protection is triggered after WFP receives a directory change notification for a file in a protected directory.</span></span> <span data-ttu-id="235c3-114">當 WFP 收到此通知時，它會判斷已變更的檔案。</span><span class="sxs-lookup"><span data-stu-id="235c3-114">When WFP receives this notification, it determines which file has changed.</span></span> <span data-ttu-id="235c3-115">如果檔案受到保護，則 WFP 會查閱目錄檔案中的檔案簽章，以判斷新的檔案是否為正確的版本。</span><span class="sxs-lookup"><span data-stu-id="235c3-115">If the file is protected, WFP looks up the file signature in a catalog file to determine if the new file is the correct version.</span></span> <span data-ttu-id="235c3-116">如果檔案版本不正確，系統會根據檔案是否位於快取中，以正確的版本取代檔案（從快取或散發媒體）。</span><span class="sxs-lookup"><span data-stu-id="235c3-116">If the file version is not correct, the system replaces the file with the correct version from either the cache or distribution media, depending on whether the file is located in the cache.</span></span> <span data-ttu-id="235c3-117">WFP 會依下列順序搜尋正確的檔案：</span><span class="sxs-lookup"><span data-stu-id="235c3-117">WFP searches for the correct file in the following order:</span></span>

1.  <span data-ttu-id="235c3-118">搜尋快取目錄。</span><span class="sxs-lookup"><span data-stu-id="235c3-118">Search the cache directory.</span></span>
2.  <span data-ttu-id="235c3-119">如果系統是使用網路安裝安裝的，請搜尋網路安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="235c3-119">Search the network install path, if the system was installed using network install.</span></span>
3.  <span data-ttu-id="235c3-120">如果系統是從 CD-ROM 安裝，請在 Windows DVD-ROM 上搜尋。</span><span class="sxs-lookup"><span data-stu-id="235c3-120">Search on a Windows CD-ROM, if the system was installed from CD-ROM.</span></span>

<span data-ttu-id="235c3-121">如果 WFP 無法在前兩個位置自動尋找檔案，則會顯示下列訊息：</span><span class="sxs-lookup"><span data-stu-id="235c3-121">If WFP cannot automatically find the file in the first two locations, it displays the following message:</span></span>

![在快取目錄或網路安裝路徑中找不到檔案時顯示的 wfp 訊息](images/wfp-1.png)

<span data-ttu-id="235c3-123">如果是使用 CD-ROM 安裝系統，則 WFP 會顯示下列訊息：</span><span class="sxs-lookup"><span data-stu-id="235c3-123">If the system was installed using a CD-ROM, WFP displays the following message:</span></span>

![顯示為提示使用者插入 windows cd-rom 的 wfp 訊息](images/wfp-2.png)

<span data-ttu-id="235c3-125">如果系統管理員未登入，則 WFP 無法顯示其中一個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="235c3-125">If an administrator is not logged on, WFP cannot display either of these dialog boxes.</span></span> <span data-ttu-id="235c3-126">當系統管理員登入之後，WFP 會顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="235c3-126">WFP will display the dialog box after an administrator logs on.</span></span>

<span data-ttu-id="235c3-127">WFP 也會將檔案取代嘗試記錄在系統事件記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="235c3-127">WFP also logs the file replacement attempt in the system event log.</span></span> <span data-ttu-id="235c3-128">如果系統管理員已取消還原正確的檔案，則 WFP 會記錄取消。</span><span class="sxs-lookup"><span data-stu-id="235c3-128">If the administrator canceled restoration of the correct file, WFP logs the cancellation.</span></span>

## <a name="retrieving-the-list-of-protected-files"></a><span data-ttu-id="235c3-129">正在抓取受保護檔案的清單</span><span class="sxs-lookup"><span data-stu-id="235c3-129">Retrieving the List of Protected Files</span></span>

<span data-ttu-id="235c3-130">下列範例會顯示應用程式和安裝程式如何使用 [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) 函式來取得受保護檔案的完整清單。</span><span class="sxs-lookup"><span data-stu-id="235c3-130">The following example shows how applications and installers can use the [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) function to get the complete list of protected files.</span></span>


```C++
#include <windows.h>
#include <sfc.h>
#include <stdio.h>

#pragma comment(lib, "sfc")

void wmain (int argc, WCHAR ** argv)
{  UNREFERENCED_PARAMETER(argc);    
   PROTECTED_FILE_DATA pfd = {0};
   BOOL fResult;

   wprintf (L"List of protected files:\n\n", argv[1]);

   while (FALSE != (fResult = SfcGetNextProtectedFile (NULL, &pfd)))
   {
      wprintf (L"   %lu   %s\n", pfd.FileNumber, pfd.FileName);
   }

   if (GetLastError() == ERROR_NO_MORE_FILES)
   {
      wprintf (L"\nAll %lu protected files listed\n", pfd.FileNumber);
   }
   else
   {
      wprintf (L"\nerror %lu: SfcGetNextProtectedFile() failed unexpectedly\n", GetLastError());
   }

}
```



 

 



