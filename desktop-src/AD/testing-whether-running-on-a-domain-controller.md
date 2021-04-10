---
title: 測試是否正在網域控制站上執行
description: 下列程式碼會使用 VerifyVersionInfo 函數來判斷呼叫進程是否正在 Windows 2000 伺服器網域控制站上執行。
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092617"
---
# <a name="testing-whether-running-on-a-domain-controller"></a><span data-ttu-id="2f45e-103">測試是否正在網域控制站上執行</span><span class="sxs-lookup"><span data-stu-id="2f45e-103">Testing Whether Running on a Domain Controller</span></span>

<span data-ttu-id="2f45e-104">下列程式碼會使用 [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) 函數來判斷呼叫進程是否正在 Windows 2000 伺服器網域控制站上執行。</span><span class="sxs-lookup"><span data-stu-id="2f45e-104">The following code uses the [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) function to determine whether the calling process is running on a Windows 2000 Server domain controller.</span></span> <span data-ttu-id="2f45e-105">您的服務安裝程式可以使用這種測試，再于 LocalSystem 帳戶下安裝服務。</span><span class="sxs-lookup"><span data-stu-id="2f45e-105">Your service installation program could use this test before installing a service under the LocalSystem account.</span></span> <span data-ttu-id="2f45e-106">如果測試指出您是在網域控制站上執行，您可以安裝要在使用者帳戶下執行的服務，或是在網域控制站上，顯示以 LocalSystem 身分執行的危險的對話方塊， (這種情況下，服務會有不受限制地存取 Active Directory Domain Services，這是順序都非常強大的安全性內容，可能會破壞整個網路) 。</span><span class="sxs-lookup"><span data-stu-id="2f45e-106">If the test indicates that you are running on a domain controller, you either install the service to run under a user account, or display a dialog box warning of the dangers in running as LocalSystem on a domain controller (which are that the service would then have unrestricted access to Active Directory Domain Services, a supremely powerful security context that has the potential to damage the entire network).</span></span>


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 