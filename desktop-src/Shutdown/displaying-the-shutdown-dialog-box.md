---
description: 下列範例會使用 InitiateSystemShutdown 函數重新開機本機系統。
ms.assetid: 928c2d48-daa5-4c27-816b-766adedba7eb
title: 顯示關機對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedfee9e96fa1e6183cbe1d9322a603b65ae4b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977904"
---
# <a name="displaying-the-shutdown-dialog-box"></a><span data-ttu-id="4c79d-103">顯示關機對話方塊</span><span class="sxs-lookup"><span data-stu-id="4c79d-103">Displaying the Shutdown Dialog Box</span></span>

<span data-ttu-id="4c79d-104">下列範例會使用 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) 函數重新開機本機系統。</span><span class="sxs-lookup"><span data-stu-id="4c79d-104">The following example reboots the local system using the [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) function.</span></span> <span data-ttu-id="4c79d-105">系統會顯示一個對話方塊，其中包含自訂訊息和訊息給使用者，以在指定的逾時間隔內關閉應用程式 (30 秒) 。</span><span class="sxs-lookup"><span data-stu-id="4c79d-105">The system displays a dialog box with a custom message and a message to the user to close applications within the specified time-out interval (30 seconds).</span></span> <span data-ttu-id="4c79d-106">經過逾時間隔之後，系統便會重新開機。</span><span class="sxs-lookup"><span data-stu-id="4c79d-106">After the time-out interval elapses, the system is restarted.</span></span>

<span data-ttu-id="4c79d-107">應用程式必須先啟用 SE \_ 關機 \_ 名稱許可權，才能呼叫 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)。</span><span class="sxs-lookup"><span data-stu-id="4c79d-107">The application must enable the SE\_SHUTDOWN\_NAME privilege before calling [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna).</span></span> <span data-ttu-id="4c79d-108">如需詳細資訊，請參閱 [許可權](../secauthz/privileges.md)。</span><span class="sxs-lookup"><span data-stu-id="4c79d-108">For more information, see [Privileges](../secauthz/privileges.md).</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL MySystemShutdown( LPTSTR lpMsg )
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   BOOL fResult;               // system shutdown flag 
 
   // Get the current process token handle so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
        TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
        &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
      (PTOKEN_PRIVILEGES) NULL, 0); 
 
   // Cannot test the return value of AdjustTokenPrivileges. 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Display the shutdown dialog box and start the countdown. 
 
   fResult = InitiateSystemShutdown( 
      NULL,    // shut down local computer 
      lpMsg,   // message for user
      30,      // time-out period, in seconds 
      FALSE,   // ask user to close apps 
      TRUE);   // reboot after shutdown 
 
   if (!fResult) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE; 
}
```



<span data-ttu-id="4c79d-109">如果 [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) 函式是在 [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)指定的超時時間內執行，系統就不會關閉。</span><span class="sxs-lookup"><span data-stu-id="4c79d-109">If the [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna) function is executed in the time-out period specified by [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna), the system does not shut down.</span></span> <span data-ttu-id="4c79d-110">例如，如果在 MySystemShutdown 之後呼叫 PreventSystemShutdown，系統就會關閉對話方塊，而不會重新開機系統。</span><span class="sxs-lookup"><span data-stu-id="4c79d-110">For example, if PreventSystemShutdown is called after MySystemShutdown, the system closes the dialog box and does not restart the system.</span></span>


```C++
#include <windows.h>

#pragma comment( lib, "advapi32.lib" )

BOOL PreventSystemShutdown()
{
   HANDLE hToken;              // handle to process token 
   TOKEN_PRIVILEGES tkp;       // pointer to token structure 
 
   // Get the current process token handle  so we can get shutdown 
   // privilege. 
 
   if (!OpenProcessToken(GetCurrentProcess(), 
         TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken)) 
      return FALSE; 
 
   // Get the LUID for shutdown privilege. 
 
   LookupPrivilegeValue(NULL, SE_SHUTDOWN_NAME, 
         &tkp.Privileges[0].Luid); 
 
   tkp.PrivilegeCount = 1;  // one privilege to set    
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 
 
   // Get shutdown privilege for this process. 
 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
        (PTOKEN_PRIVILEGES)NULL, 0); 
 
   if (GetLastError() != ERROR_SUCCESS) 
      return FALSE; 
 
   // Prevent the system from shutting down. 
 
   if ( !AbortSystemShutdown(NULL) ) 
      return FALSE; 
 
   // Disable shutdown privilege. 
 
   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, 
       (PTOKEN_PRIVILEGES) NULL, 0); 
 
   return TRUE;
}
```



 

 
