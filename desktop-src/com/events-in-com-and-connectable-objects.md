---
title: COM 和可連線物件中的事件
description: 當程式偵測到發生的情況時，就會通知其用戶端。
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "104022962"
---
# <a name="events-in-com-and-connectable-objects"></a><span data-ttu-id="055bd-103">COM 和可連線物件中的事件</span><span class="sxs-lookup"><span data-stu-id="055bd-103">Events in COM and Connectable Objects</span></span>

<span data-ttu-id="055bd-104">當程式偵測到發生的情況時，就會通知其用戶端。</span><span class="sxs-lookup"><span data-stu-id="055bd-104">When a program detects something that has happened, it can notify its clients.</span></span> <span data-ttu-id="055bd-105">例如，如果股票報價方案偵測到股票價格的變化，它可以通知所有用戶端的變更。</span><span class="sxs-lookup"><span data-stu-id="055bd-105">For example, if a stock ticker program detects a change in the price of a stock, it can notify all clients of the change.</span></span> <span data-ttu-id="055bd-106">此通知處理常式稱為 *引發事件*。</span><span class="sxs-lookup"><span data-stu-id="055bd-106">This notification process is referred to as *firing an event*.</span></span>

<span data-ttu-id="055bd-107">使用 COM 時，伺服器物件可以使用 COM 事件來引發事件，而不需要通知物件的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="055bd-107">With COM, server objects can use COM events to fire events without any information about what objects will be notified.</span></span> <span data-ttu-id="055bd-108">物件也可以使用可連接的 *物件* 來維護已要求通知之用戶端的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="055bd-108">Objects can also use *connectable objects* to maintain detailed information about clients who have requested notifications.</span></span>

<span data-ttu-id="055bd-109">COM 可連線物件除了連入介面外，還提供外寄介面給其用戶端。</span><span class="sxs-lookup"><span data-stu-id="055bd-109">COM connectable objects provide outgoing interfaces to their clients in addition to their incoming interfaces.</span></span> <span data-ttu-id="055bd-110">因此，物件及其用戶端可以進行雙向通訊。</span><span class="sxs-lookup"><span data-stu-id="055bd-110">As a result, objects and their clients can engage in bidirectional communication.</span></span> <span data-ttu-id="055bd-111">傳入介面會在物件上執行，並接收來自物件外部用戶端的呼叫，而傳出介面則是在用戶端的接收上執行，並接收來自物件的呼叫。</span><span class="sxs-lookup"><span data-stu-id="055bd-111">Incoming interfaces are implemented on an object and receive calls from external clients of an object, while outgoing interfaces are implemented on the client's sink and receive calls from the object.</span></span> <span data-ttu-id="055bd-112">物件會定義它想要使用的介面，且用戶端會執行它。</span><span class="sxs-lookup"><span data-stu-id="055bd-112">The object defines an interface it would like to use, and the client implements it.</span></span>

<span data-ttu-id="055bd-113">物件會定義其傳入介面，並提供這些介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="055bd-113">An object defines its incoming interfaces and provides implementations of these interfaces.</span></span> <span data-ttu-id="055bd-114">連入介面可透過物件的 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法提供給用戶端。</span><span class="sxs-lookup"><span data-stu-id="055bd-114">Incoming interfaces are available to clients through the object's [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method.</span></span> <span data-ttu-id="055bd-115">用戶端會呼叫物件上的傳入介面方法，而物件會代表用戶端執行想要的動作。</span><span class="sxs-lookup"><span data-stu-id="055bd-115">Clients call the methods of an incoming interface on the object, and the object performs desired actions on behalf of the client.</span></span>

<span data-ttu-id="055bd-116">輸出介面也會由物件定義，但用戶端會在用戶端所建立的接收物件上提供傳出介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="055bd-116">Outgoing interfaces are also defined by an object, but the client provides the implementations of the outgoing interfaces on a sink object that the client creates.</span></span> <span data-ttu-id="055bd-117">然後，此物件會呼叫接收物件上之輸出介面的方法，以通知用戶端物件中的變更、在用戶端中觸發事件、從用戶端要求某個內容，或者，對於物件建立者所提出的任何目的。</span><span class="sxs-lookup"><span data-stu-id="055bd-117">The object then calls methods of the outgoing interface on the sink object to notify the client of changes in the object, to trigger events in the client, to request something from the client, or, in fact, for any purpose the object creator comes up with.</span></span>

<span data-ttu-id="055bd-118">輸出介面的其中一個範例是 IButtonSink 介面，這個介面是由推播按鈕控制項所定義，用來通知其事件的用戶端。</span><span class="sxs-lookup"><span data-stu-id="055bd-118">An example of an outgoing interface is an IButtonSink interface defined by a push button control to notify its clients of its events.</span></span> <span data-ttu-id="055bd-119">例如，當使用者按一下螢幕上的按鈕時，按鈕物件會在用戶端的接收物件上呼叫 IButtonSink：： OnClick。</span><span class="sxs-lookup"><span data-stu-id="055bd-119">For example, the button object calls IButtonSink::OnClick on the client's sink object when the user clicks the button on the screen.</span></span> <span data-ttu-id="055bd-120">按鈕控制項會定義輸出介面。</span><span class="sxs-lookup"><span data-stu-id="055bd-120">The button control defines the outgoing interface.</span></span> <span data-ttu-id="055bd-121">若要讓按鈕的用戶端處理事件，用戶端必須在接收物件上執行該輸出介面，然後將該接收連接到按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="055bd-121">For a client of the button to handle the event, the client must implement that outgoing interface on a sink object and then connect that sink to the button control.</span></span> <span data-ttu-id="055bd-122">然後，當事件發生在按鈕時，按鈕就會呼叫接收，此時用戶端可以執行任何想要指派給該按鈕的動作。</span><span class="sxs-lookup"><span data-stu-id="055bd-122">Then, when events occur in the button, the button will call the sink, at which time the client can execute whatever action it wishes to assign to that button click.</span></span>

<span data-ttu-id="055bd-123">可連線物件提供物件對用戶端通訊的一般機制。</span><span class="sxs-lookup"><span data-stu-id="055bd-123">Connectable objects provide a general mechanism for object-to-client communication.</span></span> <span data-ttu-id="055bd-124">任何想要公開任何類型之事件或通知的物件，都可以使用這項技術。</span><span class="sxs-lookup"><span data-stu-id="055bd-124">Any object that wishes to expose events or notifications of any kind can use this technology.</span></span> <span data-ttu-id="055bd-125">除了一般可連線物件技術之外，COM 也提供許多特殊用途的接收和網站介面，可供物件用來通知用戶端感興趣的特定事件。</span><span class="sxs-lookup"><span data-stu-id="055bd-125">In addition to the general connectable object technology, COM provides many special purpose sink and site interfaces used by objects to notify clients of specific events of interest to the client.</span></span> <span data-ttu-id="055bd-126">例如，物件可使用 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) 來通知用戶端資料，並查看物件中的變更。</span><span class="sxs-lookup"><span data-stu-id="055bd-126">For example, [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) may be used by objects to notify clients of data and view changes in the object.</span></span>

<span data-ttu-id="055bd-127">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="055bd-127">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="055bd-128">可連線物件的架構</span><span class="sxs-lookup"><span data-stu-id="055bd-128">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
-   [<span data-ttu-id="055bd-129">可連線物件介面</span><span class="sxs-lookup"><span data-stu-id="055bd-129">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)

 

 




