---
title: 建立收集器起始的訂用帳戶
description: 您可以使用收集器起始的訂用帳戶，在本機電腦上訂閱接收事件 (從遠端電腦轉送的事件收集器)  (事件來源) 。
ms.assetid: 76f14e01-7a84-4c94-aea6-91189573eb89
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1359033b61d419f1147ca930f30d924b8429e31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186054"
---
# <a name="creating-a-collector-initiated-subscription"></a><span data-ttu-id="1a608-103">建立收集器起始的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="1a608-103">Creating a Collector Initiated Subscription</span></span>

<span data-ttu-id="1a608-104">您可以使用收集器起始的訂用帳戶，在本機電腦上訂閱接收事件 (從遠端電腦轉送的事件收集器)  (事件來源) 。</span><span class="sxs-lookup"><span data-stu-id="1a608-104">You can subscribe to receive events on a local computer (the event collector) that are forwarded from remote computers (the event sources) by using a collector-initiated subscription.</span></span> <span data-ttu-id="1a608-105">在收集器起始的訂用帳戶中，訂用帳戶必須包含所有事件來源的清單。</span><span class="sxs-lookup"><span data-stu-id="1a608-105">In a collector-initiated subscription, the subscription must contain a list of all the event sources.</span></span> <span data-ttu-id="1a608-106">在收集器電腦可以訂閱事件，且遠端事件來源可以轉寄事件之前，這兩部電腦都必須針對事件收集和轉送進行設定。</span><span class="sxs-lookup"><span data-stu-id="1a608-106">Before a collector computer can subscribe to events and a remote event source can forward events, both computers must be configured for event collecting and forwarding.</span></span> <span data-ttu-id="1a608-107">如需有關如何設定電腦的詳細資訊，請參閱 [設定電腦以轉送和收集事件](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))。</span><span class="sxs-lookup"><span data-stu-id="1a608-107">For more information about how to configure the computers, see [Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).</span></span>

<span data-ttu-id="1a608-108">下列程式碼範例會遵循一連串步驟來建立收集器起始的訂用帳戶：</span><span class="sxs-lookup"><span data-stu-id="1a608-108">The following code example follows a series of steps to create a collector initiated subscription:</span></span>

<span data-ttu-id="1a608-109">**建立收集器起始的訂用帳戶**</span><span class="sxs-lookup"><span data-stu-id="1a608-109">**To create a collector initiated subscription**</span></span>

1.  <span data-ttu-id="1a608-110">藉由提供訂用帳戶名稱和存取權限作為 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函式的參數，來開啟訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="1a608-110">Open the subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="1a608-111">如需存取權限的詳細資訊，請參閱 [**Windows 事件收集器常數**](windows-event-collector-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="1a608-111">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="1a608-112">藉由呼叫 [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) 函數來設定訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="1a608-112">Set the properties of the subscription by calling the [**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) function.</span></span> <span data-ttu-id="1a608-113">如需可設定之訂用帳戶屬性的詳細資訊，請參閱 [**EC \_ 訂閱 \_ 屬性 \_ 識別碼**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) 列舉。</span><span class="sxs-lookup"><span data-stu-id="1a608-113">For more information about subscription properties that can be set, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="1a608-114">藉由呼叫 [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) 函數來儲存訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="1a608-114">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
4.  <span data-ttu-id="1a608-115">藉由呼叫 [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) 函數來關閉訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="1a608-115">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="1a608-116">如需新增事件來源的詳細資訊，請參閱 [將事件來源新增至事件收集器訂](adding-an-event-source-to-an-event-collector-subscription.md)用帳戶。</span><span class="sxs-lookup"><span data-stu-id="1a608-116">For more information about adding an event source, see [Adding an Event Source to an Event Collector Subscription](adding-an-event-source-to-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="1a608-117">下列 c + + 程式碼範例顯示如何建立收集器起始的訂用帳戶：</span><span class="sxs-lookup"><span data-stu-id="1a608-117">The following C++ code example shows how to create a collector-initiated subscription:</span></span>


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <string>
#include <xstring>
#include <conio.h>
#include <EvColl.h>
#include <vector>
#include <wincred.h>
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "wecapi.lib")

// Track properties of the Subscription.
typedef struct _SUBSCRIPTION_COLLECTOR_INITIATED
{
    std::wstring Name;
    std::wstring Description;
    std::wstring URI;
    std::wstring Query;
    std::wstring DestinationLog;
    std::wstring Password;
    std::wstring UserName;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    EC_SUBSCRIPTION_CREDENTIALS_TYPE CredentialsType;
    BOOL SubscriptionStatus;
} SUBSCRIPTION_COLLECTOR_INITIATED;

// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal = ERROR_SUCCESS;
    EC_HANDLE hSubscription = 0;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_COLLECTOR_INITIATED sub;

    sub.Name = L"TestSubscription-CollectorInitiated";
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them\n" \
        L"to the ForwardedEvents log.";
    sub.URI = L"http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog";
    sub.Query = L"<QueryList>" \
        L"<Query Path=\"Microsoft-Windows-TaskScheduler/Operational\">" \
        L"<Select>*</Select>" \
        L"</Query>" \
        L"</QueryList>";
    sub.DestinationLog = L"ForwardedEvents";
    sub.ConfigMode = EcConfigurationModeCustom;
    sub.MaxItems = 5;
    sub.MaxLatencyTime = 10000;
    sub.HeartbeatInerval = 10000;
    sub.DeliveryMode = EcDeliveryModePull;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.CredentialsType = EcSubscriptionCredDefault;
    sub.SubscriptionStatus = true;
    sub.SubscriptionType = EcSubscriptionTypeCollectorInitiated;

    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    PEC_VARIANT vEventSource = NULL;
    DWORD dwEventSourceCount;
    EC_VARIANT vSourceProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // The subscription name, URI, and query string must be defined to create 
    // the subscription.
    if ( sub.Name.empty() || sub.URI.empty() || sub.Query.empty() )
    {
        dwRetVal = ERROR_INVALID_PARAMETER;
        goto Cleanup;
    }

    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(sub.Name.c_str(),
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_CREATE_NEW);
    if ( !hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Define the subscription properties.
    // Set the Description property that contains a description
    // of the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Description.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionDescription,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the subscription type property (collector initiated).
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.SubscriptionType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionType,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the URI property that specifies the URI of all the event sources.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.URI.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionURI,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Query property that defines the query used by the event
    // source to select events that are forwarded to the event collector.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Query.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionQuery,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Log File property that specifies where the forwarded events
    // will be stored.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.DestinationLog.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionLogFile,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ConfigurationMode property that specifies the mode in which events 
    // are delivered.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ConfigMode;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionConfigurationMode,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // If the Configuration Mode is Custom, set the DeliveryMode, DeliveryMaxItems,
    // HeartbeatInterval, and DeliveryMaxLatencyTime properties.
    if ( sub.ConfigMode == EcConfigurationModeCustom)
    {
        // Set the DeliveryMode property that defines how events are delivered. 
        // Events can be delivered through either a push or pull model.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.DeliveryMode;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMode,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxItems property that specifies the maximum number of 
        // events that can be batched when forwarded from the event sources.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxItems;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxItems,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the HeartbeatInterval property that defines the time interval, in 
        // seconds, that is observed between the heartbeat messages.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.HeartbeatInerval;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionHeartbeatInterval,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxLatencyTime property that specifies how long, in 
        // seconds, the event source should wait before forwarding events.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxLatencyTime;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxLatencyTime,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // Set the ContentFormat property that specifies the format for the event content.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ContentFormat;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionContentFormat,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the CredentialsType property that specifies the type of credentials 
    // used in the event subscription.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.CredentialsType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCredentialsType,
        0, 
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Enabled property that is used to enable or disable the subscription
    // or to obtain the current status of a subscription.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.SubscriptionStatus;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionEnabled,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the user name and password used to connect to the event sources    
    wcout << "Enter credentials used to connect to the event sources. " << endl <<
        "Enter user name: " << endl;
    wcin >> sub.UserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && sub.Password.length() < 512)
    {sub.Password.append(1, c);}

    // Set the CommonUserName property that is used by the local and remote 
    // computers to authenticate the user with the source of the events. This 
    // property is used across all the event sources available for this subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.UserName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonUserName,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the CommonPassword property that is used by the local and remote 
    // computers to authenticate the user with the source of the events.
    // Use Credential Manager Functions to handle Password information.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Password.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionCommonPassword,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    //  When you have finished using the credentials,
    //  erase them from memory.
    sub.UserName.erase();
    sub.Password.erase();


    //----------------------------------------------
    // Add event sources.
    // Ensure that a handle to the event sources array has been obtained.

    //Initialize the Event Sources Array
    dwRetVal = GetProperty( hSubscription, 
        EcSubscriptionEventSources, 
        0, 
        buffer, 
        vEventSource);

    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vSourceProperty.Type = EcVarTypeString;
    vSourceProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vSourceProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vSourceProperty.Type = EcVarTypeBoolean;
    vSourceProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vSourceProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    //----------------------------------------------
    // Step 3: Save the subscription.
    // Save the subscription with the associated properties
    // This will create the subscription and store it in the 
    // subscription repository 
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Close the subscription.
Cleanup:
    if(hSubscription)
        EcClose(hSubscription);
    if(hArray)
        EcClose(hArray);

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
            L" Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}

DWORD GetProperty(EC_HANDLE hSubscription, 
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
        &dwBufferSize) )
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
```



<span data-ttu-id="1a608-118">**驗證訂用帳戶是否正確運作**</span><span class="sxs-lookup"><span data-stu-id="1a608-118">**Validate that the subscription works correctly**</span></span>

1.  <span data-ttu-id="1a608-119">在事件收集器電腦上，完成下列程式：</span><span class="sxs-lookup"><span data-stu-id="1a608-119">On the event collector computer complete the following procedure:</span></span>

    1.  <span data-ttu-id="1a608-120">從提升許可權的命令提示字元執行下列命令，以取得訂用帳戶的執行時間狀態：</span><span class="sxs-lookup"><span data-stu-id="1a608-120">Run the following command from an elevated privilege command prompt to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="1a608-121">\**>wecutil gr\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="1a608-121">**wecutil gr** *<subscriptionID>*</span></span>

    2.  <span data-ttu-id="1a608-122">確認事件來源已連接。</span><span class="sxs-lookup"><span data-stu-id="1a608-122">Verify that the event source has connected.</span></span> <span data-ttu-id="1a608-123">在您建立要連接之事件來源的訂用帳戶之後，您可能需要等候直到原則中指定的重新整理間隔結束為止。</span><span class="sxs-lookup"><span data-stu-id="1a608-123">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3.  <span data-ttu-id="1a608-124">執行下列命令以取得訂用帳戶資訊：</span><span class="sxs-lookup"><span data-stu-id="1a608-124">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="1a608-125">\**>wecutil gs\*\*\*<subscriptionID>*</span><span class="sxs-lookup"><span data-stu-id="1a608-125">**wecutil gs** *<subscriptionID>*</span></span>

    4.  <span data-ttu-id="1a608-126">從訂用帳戶資訊中取得 DeliveryMaxItems 值。</span><span class="sxs-lookup"><span data-stu-id="1a608-126">Get the DeliveryMaxItems value from the subscription information.</span></span>

2.  <span data-ttu-id="1a608-127">在事件來源電腦上，從事件訂用帳戶引發符合查詢的事件。</span><span class="sxs-lookup"><span data-stu-id="1a608-127">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="1a608-128">必須針對要轉送的事件引發事件的 DeliveryMaxItems 數目。</span><span class="sxs-lookup"><span data-stu-id="1a608-128">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3.  <span data-ttu-id="1a608-129">在事件收集器電腦上，驗證事件已轉送至 ForwardedEvents 記錄檔或訂用帳戶中指定的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="1a608-129">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a608-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a608-130">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1a608-131">[設定電腦以轉送和收集事件](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="1a608-131">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="1a608-132">將事件來源新增至事件收集器訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="1a608-132">Adding an Event Source to an Event Collector Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="1a608-133">Windows 事件收集器參考</span><span class="sxs-lookup"><span data-stu-id="1a608-133">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 