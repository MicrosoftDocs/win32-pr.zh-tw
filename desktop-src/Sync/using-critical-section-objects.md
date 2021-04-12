---
description: 下列範例顯示執行緒如何初始化、輸入和釋放重要區段。 它會使用 InitializeCriticalSectionAndSpinCount、EnterCriticalSection、LeaveCriticalSection 和 DeleteCriticalSection 函數。
ms.assetid: 3c96414b-97e7-4ebb-a629-bfdb7a77c576
title: 使用重要區段物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e280319e3eb3078ea67a1f96065598d4517766
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192932"
---
# <a name="using-critical-section-objects"></a>使用重要區段物件

下列範例顯示執行緒如何初始化、輸入和釋放 [重要區段](critical-section-objects.md)。 它會使用 [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount)、 [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection)、 [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection)和 [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) 函數。

``` syntax
// Global variable
CRITICAL_SECTION CriticalSection; 

int main( void )
{
    ...

    // Initialize the critical section one time only.
    if (!InitializeCriticalSectionAndSpinCount(&CriticalSection, 
        0x00000400) ) 
        return;
    ...

    // Release resources used by the critical section object.
    DeleteCriticalSection(&CriticalSection);
}

DWORD WINAPI ThreadProc( LPVOID lpParameter )
{
    ...

    // Request ownership of the critical section.
    EnterCriticalSection(&CriticalSection); 

    // Access the shared resource.

    // Release ownership of the critical section.
    LeaveCriticalSection(&CriticalSection);

    ...
return 1;
}
```

 

 
