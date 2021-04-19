---
description: 發行事件
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: 發行事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971960"
---
# <a name="publishing-an-event"></a><span data-ttu-id="0431c-103">發行事件</span><span class="sxs-lookup"><span data-stu-id="0431c-103">Publishing an Event</span></span>

<span data-ttu-id="0431c-104">若要發佈事件，只要呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或使用 EventClassID 或 EventClassName 作為引數的 Microsoft Visual Basic **CreateObject** 方法，即可將事件物件具現化。</span><span class="sxs-lookup"><span data-stu-id="0431c-104">To publish an event, just instantiate an event object by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or the Microsoft Visual Basic **CreateObject** method using EventClassID or EventClassName as an argument.</span></span> <span data-ttu-id="0431c-105">發行者會呼叫事件物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得事件類別物件所支援的介面，並透過介面，在事件物件上叫用方法來發佈事件。</span><span class="sxs-lookup"><span data-stu-id="0431c-105">The publisher calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the event object to obtain the interfaces supported by the event class object and invokes a method on the event object through the interface to publish the event.</span></span> <span data-ttu-id="0431c-106">然後，事件系統會在 \_ 具有介面識別碼 IID IEventObjectChange 的事件類別 CLSID EventObjectChange 上發佈事件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0431c-106">The event system then publishes events on the event class CLSID\_EventObjectChange with the interface ID IID\_IEventObjectChange.</span></span>

<span data-ttu-id="0431c-107">為了支援將事件傳遞給多個訂閱者，事件類別方法應該只包含在參數中。</span><span class="sxs-lookup"><span data-stu-id="0431c-107">To support delivery of events to multiple subscribers, event class methods should contain only in parameters.</span></span>

<span data-ttu-id="0431c-108">藉由使用 [事件類別](the-com--event-class-object.md) 物件的 FireInParallel 屬性，發行者可以要求事件系統使用多個執行緒，將事件傳遞給多個訂閱者。</span><span class="sxs-lookup"><span data-stu-id="0431c-108">By using the FireInParallel property of the [event class](the-com--event-class-object.md) object, publishers can request that the event system use multiple threads to deliver an event to more than one subscriber.</span></span> <span data-ttu-id="0431c-109">選取平行傳遞機制並不保證將事件同時傳遞給多個訂閱者，但它會指示 COM + 事件服務允許發生此情況。</span><span class="sxs-lookup"><span data-stu-id="0431c-109">Selecting an in-parallel delivery mechanism does not guarantee simultaneous delivery of the event to multiple subscribers, but it instructs the COM+ events service to permit this to happen.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0431c-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="0431c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0431c-111">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="0431c-111">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
