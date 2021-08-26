---
title: 刪除事件收集器訂用帳戶
description: 您可以從本機電腦刪除事件收集器訂用帳戶。
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9edf2f9dda2b6393ab147d5f58ff8f889952eaeb7f31f82080558697f117f3c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006088"
---
# <a name="deleting-an-event-collector-subscription"></a>刪除事件收集器訂用帳戶

您可以從本機電腦刪除事件收集器訂用帳戶。 您必須知道訂用帳戶的名稱，才能將其刪除。 如需如何列出本機電腦上目前訂用帳戶的詳細資訊，請參閱 [列出事件收集器訂閱](listing-event-collector-subscriptions.md)，或在命令提示字元中輸入下列命令：

**>wecutil es**

> [!Note]
>
> 您可以使用此範例刪除事件收集器訂用帳戶，或在命令提示字元中輸入下列命令：
>
> **>wecutil ds** *SubscriptionName*

 

在您取出要刪除的事件收集器訂用帳戶名稱之後，您可以提供訂用帳戶的名稱做為 [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)的參數。

下列 c + + 程式碼範例顯示如何刪除事件收集器訂閱。


```C++
#include <windows.h>
#include <EvColl.h>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

void __cdecl wmain()
{
    DWORD dwRetVal;
    LPWSTR lpSubname = L"MyTestSubscription";

    // Delete the specified Event Collector subscription.
    if (!EcDeleteSubscription(lpSubname, 0))
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." 
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n"
            L"Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[列出事件收集器訂閱](listing-event-collector-subscriptions.md)
</dt> <dt>

[Windows事件收集器參考](windows-event-collector-reference.md)
</dt> </dl>

 

 




