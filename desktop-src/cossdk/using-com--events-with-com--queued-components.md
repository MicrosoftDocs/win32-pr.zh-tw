---
description: COM + 事件服務是用來管理將發行者的事件傳遞給訂閱者。
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: 使用 com + 事件與 COM + 佇列元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973788"
---
# <a name="using-com-events-with-com-queued-components"></a><span data-ttu-id="c1585-103">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="c1585-103">Using COM+ Events with COM+ Queued Components</span></span>

<span data-ttu-id="c1585-104">COM + 事件服務是用來管理將發行者的事件傳遞給訂閱者。</span><span class="sxs-lookup"><span data-stu-id="c1585-104">The COM+ events service is used to manage the delivery of events from publishers to subscribers.</span></span> <span data-ttu-id="c1585-105">COM + 佇列的元件服務可以用來將發行者和訂閱者的訊息排入佇列，讓發行者和訂閱者的處理時間獨立，並在稍後將它重新顯示給訂閱者。</span><span class="sxs-lookup"><span data-stu-id="c1585-105">The COM+ queued components service can be used to make the publisher and subscriber processing time independent by queuing the publisher's message and later replaying it to the subscriber.</span></span> <span data-ttu-id="c1585-106">您是否需要使用已排入佇列的元件服務，取決於您應用程式的基礎商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="c1585-106">Whether or not you need to use the queued components service depends on the underlying business logic of your application.</span></span> <span data-ttu-id="c1585-107">如果您需要與時間無關的事件，您可以使用 COM + 事件服務與 COM + 佇列元件服務來建立它們。</span><span class="sxs-lookup"><span data-stu-id="c1585-107">If you need to have events that are time independent, you can create them by using the COM+ events service with COM+ queued components service.</span></span>

> [!Note]  
> <span data-ttu-id="c1585-108">如需使用 COM + 佇列元件服務的詳細資訊，請參閱 [Com + 佇列元件](com--queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="c1585-108">For additional information about using the COM+ queued components service, see [COM+ Queued Components](com--queued-components.md).</span></span>

 

<span data-ttu-id="c1585-109">排入佇列的元件服務會維護單一訊息內的方法調用順序。</span><span class="sxs-lookup"><span data-stu-id="c1585-109">The queued components service maintains order-of-method invocation within a single message.</span></span> <span data-ttu-id="c1585-110">錄製器會將所有方法調用都批次處理到訊息中，然後播放程式在處理訊息時依序叫用這些方法。</span><span class="sxs-lookup"><span data-stu-id="c1585-110">The recorder batches all method invocations into a message, and then the player invokes those methods in order when the message is processed.</span></span>

<span data-ttu-id="c1585-111">排入佇列的元件錄製器和播放機可放置在下列兩個位置的其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="c1585-111">A queued components recorder and player can be positioned in either of the following two places:</span></span>

-   <span data-ttu-id="c1585-112">在發行者和事件物件之間</span><span class="sxs-lookup"><span data-stu-id="c1585-112">Between the publisher and event object</span></span>
-   <span data-ttu-id="c1585-113">在事件物件和訂閱者之間</span><span class="sxs-lookup"><span data-stu-id="c1585-113">Between the event object and subscriber</span></span>

<span data-ttu-id="c1585-114">如果您在「發行者」和「事件」物件之間放置錄製器和播放機，則會讓 [事件類別](the-com--event-class-object.md) 元件 queuable。</span><span class="sxs-lookup"><span data-stu-id="c1585-114">If you position the recorder and player between the publisher and event object, you are making the [event class](the-com--event-class-object.md) component queuable.</span></span> <span data-ttu-id="c1585-115">事件類別元件必須標示為排入佇列，並且由播放程式在與發行者不同的進程中啟動。</span><span class="sxs-lookup"><span data-stu-id="c1585-115">The event class component must be marked for queuing and be activated by the player in a process that is separate from the publisher.</span></span>

<span data-ttu-id="c1585-116">若要以非同步方式傳遞事件，請在事件物件和訂閱者之間撰寫錄製器和播放機，並設定訂閱物件的佇列屬性。</span><span class="sxs-lookup"><span data-stu-id="c1585-116">To deliver events asynchronously, compose the recorder and player between the event object and subscriber and set the Queued attribute of the subscription object.</span></span> <span data-ttu-id="c1585-117">這會設定 SubscriberMoniker，如下所示： "queue：/new：/ {12345678-1234-1234-1234-123456789012} "。</span><span class="sxs-lookup"><span data-stu-id="c1585-117">This sets SubscriberMoniker as follows: "queue:/new:/{12345678-1234-1234-1234-123456789012}".</span></span>

<span data-ttu-id="c1585-118">在事件情況下使用佇列元件時，會有隱含的行程順序。</span><span class="sxs-lookup"><span data-stu-id="c1585-118">There is an order of delivery implication to consider when using queued components in an event situation.</span></span> <span data-ttu-id="c1585-119">由於已排入佇列的元件服務會在單一物件的存留期內記錄並播放所有呼叫，因此所有呼叫都會依發出的順序重新執行。</span><span class="sxs-lookup"><span data-stu-id="c1585-119">Because the queued components service records and plays back all calls within the lifetime of a single object in one message, all calls are replayed in the order in which they were made.</span></span> <span data-ttu-id="c1585-120">但是，如果有多個會話有一個以上的物件，則無法保證順序。</span><span class="sxs-lookup"><span data-stu-id="c1585-120">However, if there is more than one session with more than one object, order cannot be guaranteed.</span></span> <span data-ttu-id="c1585-121">如果順序很重要，請確定需要依序播放的呼叫位於相同的物件實例上。</span><span class="sxs-lookup"><span data-stu-id="c1585-121">If order is important, make sure that calls that need to be played back in order reside on the same object instance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1585-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1585-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1585-123">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="c1585-123">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="c1585-124">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="c1585-124">Publishing and Delivering Events in COM+</span></span>](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="c1585-125">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="c1585-125">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="c1585-126">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="c1585-126">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



