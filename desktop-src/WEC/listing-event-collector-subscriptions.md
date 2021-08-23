---
title: 列出事件收集器訂閱
description: 您可以取得在本機電腦上啟用的事件收集器訂用帳戶名稱清單。
ms.assetid: b44fc694-b94a-4fc5-95d1-72afb016ad72
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f67e888ba62b225603cd47293936b7010ce9f730238119d2b5d36ca9ed6dbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997918"
---
# <a name="listing-event-collector-subscriptions"></a>列出事件收集器訂閱

您可以取得在本機電腦上啟用的事件收集器訂用帳戶名稱清單。 您可以使用 [**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum) 函數取得訂用帳戶列舉值的控制碼。 建立控制碼之後， [**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription) 函數會用來列出本機電腦上的訂閱。

> [!Note]
>
> 您可以使用下列程式碼範例來取得訂用帳戶清單，或在命令提示字元中輸入下列命令：
>
> **>wecutil es**

 

下列 c + + 程式碼範例顯示如何列出事件收集器訂閱。


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    // Lists the Event Collector subscriptions that are available 
    // on the local computer.
    DWORD dwBufferSizeUsed, dwError = ERROR_SUCCESS;
    BOOL bRetVal = true;
    std::vector<WCHAR> buffer(MAX_PATH);
    EC_HANDLE hEnumerator;
    DWORD dwRetVal;

    // Create a handle to access the subscriptions.
    hEnumerator = EcOpenSubscriptionEnum(NULL);

    if (hEnumerator)
    {
        while (bRetVal)
        {
            // Get the next subscription.
            bRetVal = EcEnumNextSubscription(hEnumerator, 
                (DWORD) buffer.size(),
                (LPWSTR) &buffer[0],
                &dwBufferSizeUsed);
            dwError = GetLastError();

            // If the buffer is not large enough, resize it to accommodate the
            // subscription information.
            if (!bRetVal && ERROR_INSUFFICIENT_BUFFER == dwError)
            {
                dwError = ERROR_SUCCESS;
                buffer.resize(dwBufferSizeUsed);

                bRetVal = EcEnumNextSubscription(hEnumerator,
                    (DWORD) buffer.size(),
                    (LPWSTR) &buffer[0],
                    &dwBufferSizeUsed);
                dwError = GetLastError();
            }

            if (!bRetVal && ERROR_NO_MORE_ITEMS == dwError)
            {
                dwError = ERROR_SUCCESS;
                break;
            }

            if (bRetVal && ERROR_SUCCESS != dwError)
            {
                break;
            }
            
            // Output the subscription name.
            wprintf(L"%s\n", (LPCWSTR) &buffer[0]);    
        }
    }
    else
    {
        dwRetVal = GetLastError();
        LPVOID lpwszBuffer;

        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u. Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\nError Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }

    EcClose(hEnumerator);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows事件收集器參考](windows-event-collector-reference.md)
</dt> </dl>

 

 




