---
description: 下列範例說明如何藉由建立和開啟已命名 mutex 來使用物件名稱。
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: 使用命名物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765127"
---
# <a name="using-named-objects"></a>使用命名物件

下列範例說明如何藉由建立和開啟已命名 mutex 來使用 [物件名稱](object-names.md) 。

## <a name="first-process"></a>第一個進程

第一個進程會使用 [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) 函數來建立 mutex 物件。 請注意，即使現有的物件具有相同的名稱，此函式仍會成功。


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



## <a name="second-process"></a>第二個處理常式

第二個進程會使用 [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) 函式來開啟現有 mutex 的控制碼。 如果具有指定名稱的 mutex 物件不存在，這個函數就會失敗。 存取參數會要求對 mutex 物件的完整存取權，這是在任何等候函式中使用控制碼所需的功能。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[物件名稱](object-names.md)
</dt> <dt>

[使用 Mutex 物件](using-mutex-objects.md)
</dt> </dl>

 

 
