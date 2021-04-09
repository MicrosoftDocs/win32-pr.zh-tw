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
# <a name="detecting-resource-replacement"></a>偵測資源取代

Windows 資源保護 (WRP) 防止取代安裝為 Windows Vista 或 Windows Server 2008 一部分的基本系統檔案、資料夾和登錄機碼。

WRP 藉由偵測並防止嘗試取代受保護的資源，來保護 Windows Vista 或 Windows Server 2008 上的檔案、資料夾和登錄機碼。 這項保護是根據 Windows 任意存取控制清單 (DACL) 和存取控制清單 (針對受保護資源定義的 ACL) 。 修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。 WRP 保護的資源只能使用 [支援的資源取代機制](supported-file-replacement-mechanisms.md) 與 Windows 模組安裝程式服務進行變更。 嘗試修改受 WRP 保護之資源的應用程式永遠不會變更資源，而且可能會收到錯誤訊息，指出已拒絕資源的存取權。

應用程式和安裝程式可以使用 [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 和 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) 函數來判斷檔案或登錄機碼是否受到保護。

* * Windows Server 2003 和 Windows XP： * *

Windows 檔案保護 (WFP) 藉由偵測取代受保護系統檔案的嘗試來保護系統檔案。 當 WFP 收到受保護目錄中檔案的目錄變更通知之後，就會觸發這項保護。 當 WFP 收到此通知時，它會判斷已變更的檔案。 如果檔案受到保護，則 WFP 會查閱目錄檔案中的檔案簽章，以判斷新的檔案是否為正確的版本。 如果檔案版本不正確，系統會根據檔案是否位於快取中，以正確的版本取代檔案（從快取或散發媒體）。 WFP 會依下列順序搜尋正確的檔案：

1.  搜尋快取目錄。
2.  如果系統是使用網路安裝安裝的，請搜尋網路安裝路徑。
3.  如果系統是從 CD-ROM 安裝，請在 Windows DVD-ROM 上搜尋。

如果 WFP 無法在前兩個位置自動尋找檔案，則會顯示下列訊息：

![在快取目錄或網路安裝路徑中找不到檔案時顯示的 wfp 訊息](images/wfp-1.png)

如果是使用 CD-ROM 安裝系統，則 WFP 會顯示下列訊息：

![顯示為提示使用者插入 windows cd-rom 的 wfp 訊息](images/wfp-2.png)

如果系統管理員未登入，則 WFP 無法顯示其中一個對話方塊。 當系統管理員登入之後，WFP 會顯示對話方塊。

WFP 也會將檔案取代嘗試記錄在系統事件記錄檔中。 如果系統管理員已取消還原正確的檔案，則 WFP 會記錄取消。

## <a name="retrieving-the-list-of-protected-files"></a>正在抓取受保護檔案的清單

下列範例會顯示應用程式和安裝程式如何使用 [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) 函式來取得受保護檔案的完整清單。


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



 

 



