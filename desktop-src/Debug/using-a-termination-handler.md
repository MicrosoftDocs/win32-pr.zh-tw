---
description: 下列範例將示範如何使用終止處理常式，以確保在執行受保護的程式碼主體終止時，會釋放資源。
ms.assetid: 442af2a3-d62a-4dd8-a934-da69c1d2a738
title: 使用終止處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6fe2d2ba8a7b8443eb164571a42347ce6cfb7e99c44f90da25c6fd57863e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655078"
---
# <a name="using-a-termination-handler"></a>使用終止處理常式

下列範例將示範如何使用終止處理常式，以確保在執行受保護的程式碼主體終止時，會釋放資源。 在此情況下，執行緒會使用 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) 函數來等候重要區段物件的擁有權。 當執行緒完成執行由重要區段保護的程式碼時，必須呼叫 [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) 函式，讓重要區段物件可供其他執行緒使用。 使用終止處理常式可確保發生此情況。 如需詳細資訊，請參閱 [重要區段物件](../sync/critical-section-objects.md)。


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



 

 
