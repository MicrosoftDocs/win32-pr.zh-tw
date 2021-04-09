---
description: 下列範例將示範如何使用終止處理常式，以確保在執行受保護的程式碼主體終止時，會釋放資源。
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: 使用終止處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cbe73eda8533ed5805159d5386b69daa4d03194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936281"
---
# <a name="using-a-termination-handler"></a><span data-ttu-id="68cfb-103">使用終止處理常式</span><span class="sxs-lookup"><span data-stu-id="68cfb-103">Using a Termination Handler</span></span>

<span data-ttu-id="68cfb-104">下列範例將示範如何使用終止處理常式，以確保在執行受保護的程式碼主體終止時，會釋放資源。</span><span class="sxs-lookup"><span data-stu-id="68cfb-104">The following example shows how a termination handler is used to ensure that resources are released when execution of a guarded body of code terminates.</span></span> <span data-ttu-id="68cfb-105">在此情況下，執行緒會使用 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) 函數來等候重要區段物件的擁有權。</span><span class="sxs-lookup"><span data-stu-id="68cfb-105">In this case, a thread uses the [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) function to wait for ownership of a critical section object.</span></span> <span data-ttu-id="68cfb-106">當執行緒完成執行由重要區段保護的程式碼時，必須呼叫 [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) 函式，讓重要區段物件可供其他執行緒使用。</span><span class="sxs-lookup"><span data-stu-id="68cfb-106">When the thread is finished executing the code that is protected by the critical section, it must call the [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) function to make the critical section object available to other threads.</span></span> <span data-ttu-id="68cfb-107">使用終止處理常式可確保發生此情況。</span><span class="sxs-lookup"><span data-stu-id="68cfb-107">Using a termination handler guarantees that this will happen.</span></span> <span data-ttu-id="68cfb-108">如需詳細資訊，請參閱 [重要區段物件](../sync/critical-section-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="68cfb-108">For more information, see [critical section objects](../sync/critical-section-objects.md).</span></span>


```C++
LPTSTR lpBuffer = NULL; 
CRITICAL_SECTION CriticalSection; 

// EnterCriticalSection synchronizes code with other threads. 
EnterCriticalSection(&CriticalSection); 
 
__try 
{ 
    // Perform a task that may cause an exception. 
    lpBuffer = (LPTSTR) LocalAlloc(LPTR, 10); 
    StringCchCopy(lpBuffer, 10, TEXT("Hello"));

    _tprintf(TEXT("%s\n"),lpBuffer); 
    LocalFree(lpBuffer); 
} 
__finally 
{ 
    // LeaveCriticalSection is called even if an exception occurred. 
    LeaveCriticalSection(&CriticalSection); 
}
```



 

 
