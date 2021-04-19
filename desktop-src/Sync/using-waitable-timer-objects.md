---
description: 下列範例會建立會在10秒延遲後收到信號的計時器。
ms.assetid: 3c84c2ad-6bac-4f14-a633-51d4529314af
title: 使用可等候計時器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a23b0d9f6ab74df325be81eb9236bffe6a0c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985284"
---
# <a name="using-waitable-timer-objects"></a><span data-ttu-id="0ffd9-103">使用可等候計時器物件</span><span class="sxs-lookup"><span data-stu-id="0ffd9-103">Using Waitable Timer Objects</span></span>

<span data-ttu-id="0ffd9-104">下列範例會建立會在10秒延遲後收到信號的計時器。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-104">The following example creates a timer that will be signaled after a 10 second delay.</span></span> <span data-ttu-id="0ffd9-105">首先，程式碼會使用 [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) 函數來建立 [可等候計時器物件](waitable-timer-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-105">First, the code uses the [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) function to create a [waitable timer object](waitable-timer-objects.md).</span></span> <span data-ttu-id="0ffd9-106">然後，它會使用 [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) 函數來設定計時器。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-106">Then it uses the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function to set the timer.</span></span> <span data-ttu-id="0ffd9-107">程式碼會使用 [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) 函式來判斷計時器何時收到信號。</span><span class="sxs-lookup"><span data-stu-id="0ffd9-107">The code uses the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function to determine when the timer has been signaled.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

int main()
{
    HANDLE hTimer = NULL;
    LARGE_INTEGER liDueTime;

    liDueTime.QuadPart = -100000000LL;

    // Create an unnamed waitable timer.
    hTimer = CreateWaitableTimer(NULL, TRUE, NULL);
    if (NULL == hTimer)
    {
        printf("CreateWaitableTimer failed (%d)\n", GetLastError());
        return 1;
    }

    printf("Waiting for 10 seconds...\n");

    // Set a timer to wait for 10 seconds.
    if (!SetWaitableTimer(hTimer, &liDueTime, 0, NULL, NULL, 0))
    {
        printf("SetWaitableTimer failed (%d)\n", GetLastError());
        return 2;
    }

    // Wait for the timer.

    if (WaitForSingleObject(hTimer, INFINITE) != WAIT_OBJECT_0)
        printf("WaitForSingleObject failed (%d)\n", GetLastError());
    else printf("Timer was signaled.\n");

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="0ffd9-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ffd9-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ffd9-109">使用可等候計時器搭配非同步程序呼叫</span><span class="sxs-lookup"><span data-stu-id="0ffd9-109">Using Waitable Timers with an Asynchronous Procedure Call</span></span>](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
