---
description: 下列範例說明如何藉由建立和開啟已命名 mutex 來使用物件名稱。
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: 使用命名物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986956"
---
# <a name="using-named-objects"></a><span data-ttu-id="25b45-103">使用命名物件</span><span class="sxs-lookup"><span data-stu-id="25b45-103">Using Named Objects</span></span>

<span data-ttu-id="25b45-104">下列範例說明如何藉由建立和開啟已命名 mutex 來使用 [物件名稱](object-names.md) 。</span><span class="sxs-lookup"><span data-stu-id="25b45-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="25b45-105">第一個進程</span><span class="sxs-lookup"><span data-stu-id="25b45-105">First Process</span></span>

<span data-ttu-id="25b45-106">第一個進程會使用 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 函數來建立 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="25b45-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="25b45-107">請注意，即使現有的物件具有相同的名稱，此函式仍會成功。</span><span class="sxs-lookup"><span data-stu-id="25b45-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="25b45-108">第二個處理常式</span><span class="sxs-lookup"><span data-stu-id="25b45-108">Second Process</span></span>

<span data-ttu-id="25b45-109">第二個進程會使用 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) 函式來開啟現有 mutex 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="25b45-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="25b45-110">如果具有指定名稱的 mutex 物件不存在，這個函數就會失敗。</span><span class="sxs-lookup"><span data-stu-id="25b45-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="25b45-111">存取參數會要求對 mutex 物件的完整存取權，這是在任何等候函式中使用控制碼所需的功能。</span><span class="sxs-lookup"><span data-stu-id="25b45-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="25b45-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="25b45-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25b45-113">物件名稱</span><span class="sxs-lookup"><span data-stu-id="25b45-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="25b45-114">使用 Mutex 物件</span><span class="sxs-lookup"><span data-stu-id="25b45-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
