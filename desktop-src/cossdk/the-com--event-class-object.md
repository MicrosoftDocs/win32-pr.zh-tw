---
description: COM + 事件服務會使用事件類別物件來管理「發行者」與「訂閱者」之間的連接。
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: COM + 事件類別物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae397f647354ac24395fa073365160829a687a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936260"
---
# <a name="the-com-event-class-object"></a><span data-ttu-id="aa315-103">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="aa315-103">The COM+ Event Class Object</span></span>

<span data-ttu-id="aa315-104">COM + 事件服務會使用 *事件類別物件* 來管理「發行者」與「訂閱者」之間的連接。</span><span class="sxs-lookup"><span data-stu-id="aa315-104">The COM+ Events service uses an *event class object* to manage the connection between publisher and subscriber.</span></span> <span data-ttu-id="aa315-105">事件類別物件是由 COM + 事件系統管理和儲存的 COM + 元件，其中包含發行者用來引發事件的介面和方法。</span><span class="sxs-lookup"><span data-stu-id="aa315-105">The event class object is a COM+ component that is managed and stored by the COM+ Events system and contains the interfaces and methods used by a publisher to fire events.</span></span> <span data-ttu-id="aa315-106">它是一個持續性物件，指出可能發生的事件，並選擇性地識別發行者。</span><span class="sxs-lookup"><span data-stu-id="aa315-106">It is a persistent object that indicates the events that can occur and, optionally, identifies the publisher.</span></span> <span data-ttu-id="aa315-107">您可以藉由提供類型程式庫，指定要讓事件類別包含的介面和方法。</span><span class="sxs-lookup"><span data-stu-id="aa315-107">You specify the interfaces and methods you want an event class to contain by providing a type library.</span></span>

<span data-ttu-id="aa315-108">為了引發事件，發行者會藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 Microsoft Visual Basic **CreateObject** 方法來具現化事件類別物件，並要求傳回事件介面。</span><span class="sxs-lookup"><span data-stu-id="aa315-108">To fire an event, the publisher instantiates the event class object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method and requesting the event interface be returned.</span></span> <span data-ttu-id="aa315-109">具現化事件類別物件包含事件系統執行所要求介面的程式。</span><span class="sxs-lookup"><span data-stu-id="aa315-109">The instantiated event class object contains the event system's implementation of the requested interface.</span></span> <span data-ttu-id="aa315-110">有興趣的訂閱者也必須執行事件類別介面，以便從指定的發行者接收事件。</span><span class="sxs-lookup"><span data-stu-id="aa315-110">An interested subscriber must also implement the event class interface to receive events from a given publisher.</span></span> <span data-ttu-id="aa315-111">當事件類別物件具現化時，事件系統會將它與適當的訂閱者產生關聯。</span><span class="sxs-lookup"><span data-stu-id="aa315-111">When the event class object is instantiated, the event system associates it with the appropriate subscribers.</span></span> <span data-ttu-id="aa315-112">訂閱者的清單會在事件類別物件的存留期內進行維護。</span><span class="sxs-lookup"><span data-stu-id="aa315-112">The list of subscribers is maintained for the lifetime of the event class object.</span></span> <span data-ttu-id="aa315-113">事件可以依照順序或平行方式傳遞給多個訂閱者。</span><span class="sxs-lookup"><span data-stu-id="aa315-113">An event can be delivered to multiple subscribers either serially or in parallel.</span></span>

<span data-ttu-id="aa315-114">當您執行事件類別物件時，您應該提供可匯出 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) 函數的自我註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="aa315-114">When you implement an event class object, you should provide a self-registering DLL that exports the [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) functions.</span></span> <span data-ttu-id="aa315-115">**DllRegisterServer** 函式會註冊 COM 類別，而 **DllUnregisterServer** 函式會取消註冊元件。</span><span class="sxs-lookup"><span data-stu-id="aa315-115">The **DllRegisterServer** function registers a COM class, and the **DllUnregisterServer** function unregisters the component.</span></span> <span data-ttu-id="aa315-116">事件類別物件是以「元件服務」管理工具或使用 [**ICOMAdminCatalog：： InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) 或 [**ICOMAdminCatalog：： InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) 介面的方法，以程式設計方式儲存在 com + 目錄中。</span><span class="sxs-lookup"><span data-stu-id="aa315-116">Event class objects are stored in the COM+ catalog, either by using the Component Services administration tool or programmatically by using the methods of the [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) or [**ICOMAdminCatalog::InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) interfaces.</span></span> <span data-ttu-id="aa315-117">如需註冊事件類別物件的詳細資訊，請參閱 [註冊事件類別](registering-an-event-class.md)。</span><span class="sxs-lookup"><span data-stu-id="aa315-117">For detailed information about registering event class objects, see [Registering an Event Class](registering-an-event-class.md).</span></span>

<span data-ttu-id="aa315-118">由於事件類別物件是設定的元件，因此可以使用元件服務管理工具或 COM + 系統管理 SDK 函式來設定其他屬性，例如佇列、交易、安全性等等。</span><span class="sxs-lookup"><span data-stu-id="aa315-118">Because event class objects are configured components, other attributes, such as queuing, transactions, security, and so on, can be configured for them by using either the Component Services administration tool or the COM+ Administrative SDK functions.</span></span>

> [!Note]  
> <span data-ttu-id="aa315-119">COM + 事件服務會使用類型程式庫封送處理。</span><span class="sxs-lookup"><span data-stu-id="aa315-119">The COM+ Events service uses type library marshaling.</span></span> <span data-ttu-id="aa315-120">這會對事件類別介面施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="aa315-120">This places some restrictions on event class interfaces.</span></span> <span data-ttu-id="aa315-121">例如，類型程式庫封送處理器不支援 MIDL 屬性 [**大小， \_**](/windows/desktop/Midl/size-is) 且 [**長度 \_ 為**](/windows/desktop/Midl/length-is)。</span><span class="sxs-lookup"><span data-stu-id="aa315-121">For example, the type library marshaler does not support the MIDL attributes [**size\_is**](/windows/desktop/Midl/size-is) and [**length\_is**](/windows/desktop/Midl/length-is).</span></span>

 

<span data-ttu-id="aa315-122">事件類別物件擁有決定事件發佈方式的發行集屬性，以及下列屬性：</span><span class="sxs-lookup"><span data-stu-id="aa315-122">An event class object possesses publication attributes that determine the way events are published, as well as the following properties:</span></span>

-   <span data-ttu-id="aa315-123">**EventCLSID**。</span><span class="sxs-lookup"><span data-stu-id="aa315-123">**EventCLSID**.</span></span> <span data-ttu-id="aa315-124">指定元件 CLSID 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa315-124">A unique identifier that specifies the CLSID of the component.</span></span>
-   <span data-ttu-id="aa315-125">**EventClassName**。</span><span class="sxs-lookup"><span data-stu-id="aa315-125">**EventClassName**.</span></span> <span data-ttu-id="aa315-126">指定元件 PROGID 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa315-126">A unique identifier that specifies the PROGID of the component.</span></span>
-   <span data-ttu-id="aa315-127">**類型程式庫**。</span><span class="sxs-lookup"><span data-stu-id="aa315-127">**TypeLibrary**.</span></span> <span data-ttu-id="aa315-128">提供事件類別物件所提供的介面清單。</span><span class="sxs-lookup"><span data-stu-id="aa315-128">Provides a list of interfaces offered by the event class object.</span></span> <span data-ttu-id="aa315-129">不需要執行類型程式庫中指定的引發介面。</span><span class="sxs-lookup"><span data-stu-id="aa315-129">There is no need to implement the firing interfaces specified in the type library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa315-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa315-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa315-131">COM + 事件安全性考慮</span><span class="sxs-lookup"><span data-stu-id="aa315-131">COM+ Events Security Considerations</span></span>](com--events-security-considerations.md)
</dt> <dt>

[<span data-ttu-id="aa315-132">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="aa315-132">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="aa315-133">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="aa315-133">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="aa315-134">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="aa315-134">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="aa315-135">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="aa315-135">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
