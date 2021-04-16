---
description: 事件是 TAPI 3 下呼叫處理的重要部分。 事件處理包含四個階段。
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: " (電話語音 API) 的事件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513376"
---
# <a name="events-telephony-api"></a><span data-ttu-id="20c08-104"> (電話語音 API) 的事件</span><span class="sxs-lookup"><span data-stu-id="20c08-104">Events (Telephony API)</span></span>

<span data-ttu-id="20c08-105">事件是 TAPI 3 下呼叫處理的重要部分。</span><span class="sxs-lookup"><span data-stu-id="20c08-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="20c08-106">事件處理包含四個階段。</span><span class="sxs-lookup"><span data-stu-id="20c08-106">Event handling includes four stages.</span></span>

<span data-ttu-id="20c08-107">**若要註冊並啟用事件的接收**</span><span class="sxs-lookup"><span data-stu-id="20c08-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="20c08-108">執行 [**ITTAPIEventNotification：：事件**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) 方法。</span><span class="sxs-lookup"><span data-stu-id="20c08-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="20c08-109"> (TAPI 會在事件發生時呼叫這個方法。 ) 通常，此實 **AddRef** 不會超過 **IDispatch** 介面指標，然後張貼至應用程式的訊息提取。</span><span class="sxs-lookup"><span data-stu-id="20c08-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="20c08-110">使用 COM 標準 [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)和 [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)介面註冊 [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)輸出介面，然後將 [**IConnectionPoint：： Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)方法的指標傳遞至 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)。</span><span class="sxs-lookup"><span data-stu-id="20c08-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="20c08-111">呼叫 [**ITTAPI：:p \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，讓 TAPI 知道應用程式將處理的事件。</span><span class="sxs-lookup"><span data-stu-id="20c08-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="20c08-112">事件篩選器包含 [**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)列舉的 **或** ed 成員。</span><span class="sxs-lookup"><span data-stu-id="20c08-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="20c08-113">您必須呼叫 **ITTAPI：:p 的 \_ >eventfilter** 方法來設定事件篩選器遮罩，並啟用事件的接收。</span><span class="sxs-lookup"><span data-stu-id="20c08-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="20c08-114">如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。</span><span class="sxs-lookup"><span data-stu-id="20c08-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="20c08-115">您也必須針對應用程式將處理呼叫的每個位址物件，呼叫 [**ITTAPI：： RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) 方法。</span><span class="sxs-lookup"><span data-stu-id="20c08-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="20c08-116">請參閱 [事件介面](./event-interfaces.md) ，以取得所有事件介面的清單。</span><span class="sxs-lookup"><span data-stu-id="20c08-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="20c08-117">如需示範註冊程式的程式碼範例，請參閱 [註冊事件](register-events.md) ，並接收顯示一次使用事件之程式碼範例的 [呼叫](receive-a-call.md) 。</span><span class="sxs-lookup"><span data-stu-id="20c08-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
