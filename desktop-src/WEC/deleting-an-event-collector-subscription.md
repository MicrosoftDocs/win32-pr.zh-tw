---
title: 刪除事件收集器訂用帳戶
description: 您可以從本機電腦刪除事件收集器訂用帳戶。
ms.assetid: d3102149-906d-4286-85c8-e5b1eb6dd382
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cec036625bbb94e33e71af0f1d9808ad9252a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672955"
---
# <a name="deleting-an-event-collector-subscription"></a><span data-ttu-id="09e24-103">刪除事件收集器訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="09e24-103">Deleting an Event Collector Subscription</span></span>

<span data-ttu-id="09e24-104">您可以從本機電腦刪除事件收集器訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="09e24-104">You can delete an Event Collector subscription from a local computer.</span></span> <span data-ttu-id="09e24-105">您必須知道訂用帳戶的名稱，才能將其刪除。</span><span class="sxs-lookup"><span data-stu-id="09e24-105">You must know the name of the subscription before you can delete it.</span></span> <span data-ttu-id="09e24-106">如需如何列出本機電腦上目前訂用帳戶的詳細資訊，請參閱 [列出事件收集器訂閱](listing-event-collector-subscriptions.md)，或在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="09e24-106">For more information about how to list the current subscriptions on a local computer, see [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or type the following command at the command prompt:</span></span>

<span data-ttu-id="09e24-107">**>wecutil es**</span><span class="sxs-lookup"><span data-stu-id="09e24-107">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="09e24-108">您可以使用此範例刪除事件收集器訂用帳戶，或在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="09e24-108">You can use this example to delete an Event Collector subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="09e24-109">**>wecutil ds** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="09e24-109">**wecutil ds** *SubscriptionName*</span></span>

 

<span data-ttu-id="09e24-110">在您取出要刪除的事件收集器訂用帳戶名稱之後，您可以提供訂用帳戶的名稱做為 [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)的參數。</span><span class="sxs-lookup"><span data-stu-id="09e24-110">After you retrieve the name of the Event Collector subscription to delete, you can provide the name of the subscription as a parameter to [**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription).</span></span>

<span data-ttu-id="09e24-111">下列 c + + 程式碼範例顯示如何刪除事件收集器訂閱。</span><span class="sxs-lookup"><span data-stu-id="09e24-111">The following C++ code example shows how to delete an Event Collector subscription.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="09e24-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="09e24-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09e24-113">列出事件收集器訂閱</span><span class="sxs-lookup"><span data-stu-id="09e24-113">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="09e24-114">Windows 事件收集器參考</span><span class="sxs-lookup"><span data-stu-id="09e24-114">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




