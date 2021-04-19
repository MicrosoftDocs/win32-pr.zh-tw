---
description: 下列範例會使用 ExitWindowsEx 函數來關閉系統。
ms.assetid: bf8723aa-1c7f-4761-9034-d5a9447a4bc4
title: 如何關機系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3880319e0ada6c82c6c6c12a7f3b5faf00415a93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976888"
---
# <a name="how-to-shut-down-the-system"></a><span data-ttu-id="a8130-103">如何關機系統</span><span class="sxs-lookup"><span data-stu-id="a8130-103">How to Shut Down the System</span></span>

<span data-ttu-id="a8130-104">下列範例會使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函數來關閉系統。</span><span class="sxs-lookup"><span data-stu-id="a8130-104">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to shut down the system.</span></span> <span data-ttu-id="a8130-105">關閉將清除檔案緩衝區至磁片，並將系統帶到可安全關閉電腦的情況。</span><span class="sxs-lookup"><span data-stu-id="a8130-105">Shutting down flushes file buffers to disk and brings the system to a condition in which it is safe to turn off the computer.</span></span> <span data-ttu-id="a8130-106">應用程式必須先啟用 SE \_ SHUTDOWN \_ 名稱許可權。</span><span class="sxs-lookup"><span data-stu-id="a8130-106">The application must first enable the SE\_SHUTDOWN\_NAME privilege.</span></span> <span data-ttu-id="a8130-107">如需詳細資訊，請參閱 [許可權](../secauthz/privileges.md)。</span><span class="sxs-lookup"><span data-stu-id="a8130-107">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


```C++
#include <windows.h>

#pragma comment(lib, "user32.lib")
#pragma comment(lib, "advapi32.lib")

BOOL MySystemShutdown()
{
   HANDLE hToken; 
   TOKEN_PRIVILEGES tkp; 
 
   // Get a token for this process. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return( FALSE ); 
 
   // Get the LUID for the shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get the shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Shut down the system and force all applications to close. 
 
   if (!ExitWindowsEx(EWX_SHUTDOWN | EWX_FORCE, 
               SHTDN_REASON_MAJOR_OPERATINGSYSTEM |
               SHTDN_REASON_MINOR_UPGRADE |
               SHTDN_REASON_FLAG_PLANNED)) 
      return FALSE; 

   //shutdown was successful
   return TRUE;
}
```



<span data-ttu-id="a8130-108">[**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)呼叫中的最後一個參數表示系統已關閉，以進行作業系統的規劃更新。</span><span class="sxs-lookup"><span data-stu-id="a8130-108">The final parameter in the call to [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) indicates that the system was shut down for a planning update of the operating system.</span></span> <span data-ttu-id="a8130-109">如需詳細資訊，請參閱 [系統關機原因代碼](system-shutdown-reason-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a8130-109">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8130-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8130-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8130-111">關閉</span><span class="sxs-lookup"><span data-stu-id="a8130-111">Shutting Down</span></span>](shutting-down.md)
</dt> </dl>

 

 
