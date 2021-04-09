---
description: 建立發行者篩選
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: 建立發行者篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997fe37cf0021bcb2aa153c2dc4b73597e0c43cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111440"
---
# <a name="creating-a-publisher-filter"></a><span data-ttu-id="1a552-103">建立發行者篩選</span><span class="sxs-lookup"><span data-stu-id="1a552-103">Creating a Publisher Filter</span></span>

<span data-ttu-id="1a552-104">有兩種方法可以建立發行者篩選器：使用事件類別的 MultiPublisherFilterCLSID 屬性，或使用 [**IEventControl：： SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)。</span><span class="sxs-lookup"><span data-stu-id="1a552-104">There are two methods to establish the publisher filter: using the MultiPublisherFilterCLSID property of the event class, or using [**IEventControl::SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).</span></span>

-   <span data-ttu-id="1a552-105">因為它可讓您使用 [Com + 佇列元件](com--queued-components.md) 服務來撰寫事件物件，所以慣用的方法是使用事件類別中的 MultiPublisherFilterCLSID 屬性來設定發行者篩選。</span><span class="sxs-lookup"><span data-stu-id="1a552-105">Because it allows you to compose the event object with the [COM+ queued components](com--queued-components.md) service, the preferred method is to use the MultiPublisherFilterCLSID property in the event class to set the publisher filter.</span></span> <span data-ttu-id="1a552-106">這會為事件物件的事件介面的所有方法建立一個篩選物件。</span><span class="sxs-lookup"><span data-stu-id="1a552-106">This establishes one filter object for all the methods of the event interfaces for an event object.</span></span> <span data-ttu-id="1a552-107">當事件類別物件是使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)具現化時，事件物件會啟動發行者篩選器。</span><span class="sxs-lookup"><span data-stu-id="1a552-107">The event object activates the publisher filter when the event class object is instantiated using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
-   <span data-ttu-id="1a552-108">您也可以使用 [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)。</span><span class="sxs-lookup"><span data-stu-id="1a552-108">You can also use [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter).</span></span> <span data-ttu-id="1a552-109">但是，如果您選擇此方法，則不會 queuable 介面，因此無法在發行者和事件類別物件之間使用事件物件與 COM + 佇列元件服務。</span><span class="sxs-lookup"><span data-stu-id="1a552-109">However, if you choose this method, the interface is not queuable and therefore cannot use the event object with the COM+ queued components service between the publisher and the event class object.</span></span> <span data-ttu-id="1a552-110">如需搭配使用佇列元件服務與 COM + 事件的詳細資訊，請參閱使用 com + [事件與 com + 佇列元件](using-com--events-with-com--queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="1a552-110">For additional information about using the queued components service with COM+ Events, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

<span data-ttu-id="1a552-111">一個事件可以有一個或多個篩選物件，也可以是 none。</span><span class="sxs-lookup"><span data-stu-id="1a552-111">An event can have one or more filter objects or none at all.</span></span> <span data-ttu-id="1a552-112">發行者篩選物件必須支援 [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 或 [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)，視您是否有單一引發介面或事件類別物件上的多個引發介面而定。</span><span class="sxs-lookup"><span data-stu-id="1a552-112">The publisher filter objects must support either [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) or [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter), depending on whether you have a single firing interface or multiple firing interfaces on the event class object.</span></span> <span data-ttu-id="1a552-113">**IPublisherFilter** 和 **IMultiInterfacePublisherFilter** 介面都會指定 **Initialize** 方法。</span><span class="sxs-lookup"><span data-stu-id="1a552-113">The **IPublisherFilter** and **IMultiInterfacePublisherFilter** interfaces both specify an **Initialize** method.</span></span> <span data-ttu-id="1a552-114">建立篩選物件之後，事件類別物件會立即呼叫 **Initialize** 方法。</span><span class="sxs-lookup"><span data-stu-id="1a552-114">The **Initialize** method is called by the event class object immediately after creating the filter object.</span></span>

<span data-ttu-id="1a552-115">COM + 事件會嘗試在篩選準則上叫用兩個方法。</span><span class="sxs-lookup"><span data-stu-id="1a552-115">COM+ Events tries to invoke two methods on the filter.</span></span> <span data-ttu-id="1a552-116">首先，它會呼叫 [**IPublisherFilter：:P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) ，並將 [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) 介面指標傳遞至篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1a552-116">First it calls [**IPublisherFilter::PrepareToFire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) and passes an [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) interface pointer to the filter.</span></span> <span data-ttu-id="1a552-117">然後，它會查詢事件介面的篩選物件。</span><span class="sxs-lookup"><span data-stu-id="1a552-117">Then it queries the filter object for the event interface.</span></span> <span data-ttu-id="1a552-118">如果篩選支援事件介面，則會在其上叫用方法。</span><span class="sxs-lookup"><span data-stu-id="1a552-118">If the filter supports the event interface, it invokes a method on it.</span></span> <span data-ttu-id="1a552-119">這可讓您存取事件的發行者參數。</span><span class="sxs-lookup"><span data-stu-id="1a552-119">This provides access to the publisher parameters for an event.</span></span> <span data-ttu-id="1a552-120">篩選可以使用這些參數來判斷要引發的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a552-120">The filter can use these parameters to determine which subscriptions to fire.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a552-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a552-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a552-122">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="1a552-122">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> </dl>

 

 
