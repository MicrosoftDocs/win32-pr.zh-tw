---
description: 下列範例 x86 元件程式碼會取得與目前進程相關聯的終端機服務會話識別碼。
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: 取得目前進程的會話識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76865bcfe9144e8b95d4642385804aaf1af8fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110580"
---
# <a name="getting-the-session-id-of-the-current-process"></a><span data-ttu-id="e2773-103">取得目前進程的會話識別碼</span><span class="sxs-lookup"><span data-stu-id="e2773-103">Getting the Session ID of the Current Process</span></span>

<span data-ttu-id="e2773-104">\[此範例程式碼所指定的記憶體位址，在未來的 Windows 版本中可能會變更。</span><span class="sxs-lookup"><span data-stu-id="e2773-104">\[The memory addresses specified by this example code may change in future releases of Windows.</span></span> <span data-ttu-id="e2773-105">為確保您的應用程式會在未來繼續正常執行，您的應用程式必須呼叫 [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) ，然後 [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) ，而不是下列範例程式碼。\]</span><span class="sxs-lookup"><span data-stu-id="e2773-105">To ensure that your application will continue to run correctly in the future, your application must call [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) and then [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) instead of the following sample code.\]</span></span>

<span data-ttu-id="e2773-106">下列範例 x86 元件程式碼會取得與目前進程相關聯的終端機服務會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2773-106">The following example x86 assembly code gets the Terminal Services session ID associated with the current process.</span></span>

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
