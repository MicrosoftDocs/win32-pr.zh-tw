---
title: 從收集器起始的訂用帳戶中移除事件來源
description: 您可以從收集器起始的訂用帳戶中移除事件來源，而不需要刪除整個訂用帳戶。
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840331"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a><span data-ttu-id="10794-103">從收集器起始的訂用帳戶中移除事件來源</span><span class="sxs-lookup"><span data-stu-id="10794-103">Removing an Event Source from a Collector Initiated Subscription</span></span>

<span data-ttu-id="10794-104">您可以從收集器起始的訂用帳戶中移除事件來源，而不需要刪除整個訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="10794-104">You can remove an event source from a collector initiated subscription without deleting the entire subscription.</span></span> <span data-ttu-id="10794-105">您必須知道您想要刪除之事件來源的位址。</span><span class="sxs-lookup"><span data-stu-id="10794-105">You must know the address of the event source that you want to delete.</span></span> <span data-ttu-id="10794-106">您可以使用 [顯示事件收集器訂](displaying-the-properties-of-an-event-collector-subscription.md)用帳戶屬性的 c + + 範例，來尋找與訂用帳戶相關聯之事件來源的位址，也可以在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="10794-106">You can find the address of an event source that is associated to a subscription by using the C++ example shown in [Displaying the Properties of an Event Collector Subscription](displaying-the-properties-of-an-event-collector-subscription.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="10794-107">**>wecutil gs** *SubscriptionName*</span><span class="sxs-lookup"><span data-stu-id="10794-107">**wecutil gs** *SubscriptionName*</span></span>

<span data-ttu-id="10794-108">若要列出本機電腦上目前的訂用帳戶，您可以使用 [列出事件收集器](listing-event-collector-subscriptions.md)訂用帳戶中顯示的 c + + 程式碼範例，也可以在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="10794-108">To list the current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="10794-109">**>wecutil es**</span><span class="sxs-lookup"><span data-stu-id="10794-109">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="10794-110">您可以使用此範例從收集器起始的訂用帳戶中移除事件來源，或者您可以在命令提示字元中輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="10794-110">You can use this example to remove an event source from a collector initiated subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="10794-111">**>wecutil ss** *SubscriptionName*  \* */esa： \* \* \* EventSourceAddress* **/res**</span><span class="sxs-lookup"><span data-stu-id="10794-111">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/res**</span></span>
>
> <span data-ttu-id="10794-112">*EventSourceAddress* 可以是本機電腦的 localhost 或遠端電腦的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="10794-112">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="10794-113">此範例會遵循一連串的步驟，從收集器起始的訂用帳戶中移除事件來源。</span><span class="sxs-lookup"><span data-stu-id="10794-113">This example follows a series of steps to remove an event source from a collector-initiated subscription.</span></span>

<span data-ttu-id="10794-114">**從收集器起始的訂用帳戶中移除事件來源**</span><span class="sxs-lookup"><span data-stu-id="10794-114">**To remove an event source from a collector-initiated subscription**</span></span>

1.  <span data-ttu-id="10794-115">藉由提供訂用帳戶名稱和存取權限作為 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函式的參數，來開啟現有的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="10794-115">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="10794-116">如需存取權限的詳細資訊，請參閱 [**Windows 事件收集器常數**](windows-event-collector-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="10794-116">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="10794-117">藉由呼叫 [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) 函數來取得訂用帳戶的事件來源陣列。</span><span class="sxs-lookup"><span data-stu-id="10794-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="10794-118">如需可抓取之訂用帳戶屬性的詳細資訊，請參閱 [**EC \_ 訂閱 \_ 屬性 \_ 識別碼**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) 列舉。</span><span class="sxs-lookup"><span data-stu-id="10794-118">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="10794-119">藉由呼叫 [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) 函數，在訂用帳戶的事件來源陣列中搜尋指定的事件來源。</span><span class="sxs-lookup"><span data-stu-id="10794-119">Search for the specified event source in the event sources array of the subscription by calling the [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) function.</span></span> <span data-ttu-id="10794-120">**EcSubscriptionEventSourceAddress** 屬性的值將是本機電腦的 Localhost，或是遠端電腦的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="10794-120">The value of the **EcSubscriptionEventSourceAddress** property will be either Localhost for the local computer or will be a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="10794-121">如需可抓取之事件來源屬性的詳細資訊，請參閱 **EC \_ 訂閱 \_ 屬性 \_ 識別碼** 列舉。</span><span class="sxs-lookup"><span data-stu-id="10794-121">For more information about event source properties that can be retrieved, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
4.  <span data-ttu-id="10794-122">藉由呼叫 [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) 函數，從訂用帳戶中刪除事件來源。</span><span class="sxs-lookup"><span data-stu-id="10794-122">Delete the event source from the subscription by calling the [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) function.</span></span>
5.  <span data-ttu-id="10794-123">藉由呼叫 [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) 函數來儲存訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="10794-123">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="10794-124">藉由呼叫 [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) 函數來關閉訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="10794-124">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="10794-125">下列 c + + 程式碼範例顯示如何從事件收集器訂用帳戶中移除事件來源。</span><span class="sxs-lookup"><span data-stu-id="10794-125">The following C++ code example shows how to remove an event source from an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
    Cleanup:
        if (hArray)
            EcClose(hArray);
        if (hSubscription)
            EcClose(hSubscription);

        if (dwRetVal != ERROR_SUCCESS)
        {
            FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
                NULL,
                dwRetVal,
                0,
                (LPWSTR) &lpwszBuffer,
                0,
                NULL);
            
            if (!lpwszBuffer)
            {
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
    return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID,
        flags,
        (DWORD) buffer.size(),
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



## <a name="related-topics"></a><span data-ttu-id="10794-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="10794-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10794-127">顯示事件收集器訂用帳戶的屬性</span><span class="sxs-lookup"><span data-stu-id="10794-127">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="10794-128">列出事件收集器訂閱</span><span class="sxs-lookup"><span data-stu-id="10794-128">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="10794-129">Windows 事件收集器參考</span><span class="sxs-lookup"><span data-stu-id="10794-129">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




