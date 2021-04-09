---
description: 若要發佈事件，只要將事件類別物件具現化，並叫用所需的方法;如需如何在程式碼中進行這項作業的詳細指示，請參閱發佈事件。
ms.assetid: 835c3753-fdcc-4afe-94c3-c954aaf1c832
title: 在 COM + 中發行和傳遞事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47a444b64501156191590c115d6000f4c0bda153
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689104"
---
# <a name="publishing-and-delivering-events-in-com"></a><span data-ttu-id="05de5-103">在 COM + 中發行和傳遞事件</span><span class="sxs-lookup"><span data-stu-id="05de5-103">Publishing and Delivering Events in COM+</span></span>

<span data-ttu-id="05de5-104">若要發佈事件，只要將 [事件類別](the-com--event-class-object.md) 物件具現化，並叫用所需的方法;如需如何在程式碼中進行這項作業的詳細指示，請參閱 [發佈事件](publishing-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="05de5-104">To publish an event, simply instantiate an [event class](the-com--event-class-object.md) object and invoke the desired method; for detailed instructions on how to do this in code, see [Publishing an Event](publishing-an-event.md).</span></span>

<span data-ttu-id="05de5-105">當發行者引發事件時，COM + 事件服務會搜尋訂閱資料庫，以尋找已向具現化事件類別註冊訂用帳戶的所有訂閱者。</span><span class="sxs-lookup"><span data-stu-id="05de5-105">When a publisher fires an event, the COM+ Events service searches the subscription database to find all the subscribers who have registered subscriptions to the instantiated event class.</span></span> <span data-ttu-id="05de5-106">它會連接到這些訂閱者 (由直接建立、標記或佇列元件) ，然後呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="05de5-106">It connects to those subscribers (by direct creation, monikers, or queued components) and calls the method.</span></span> <span data-ttu-id="05de5-107">若要支援一個事件的多個訂閱者通知，方法只可包含在參數中，而且必須只傳回成功或失敗的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="05de5-107">To support more than one subscriber notification for an event, methods can contain only in parameters and must return only success or failure **HRESULT** values.</span></span>

> [!Note]  
> <span data-ttu-id="05de5-108">此版本的 COM + 事件不支援分散式事件存放區。</span><span class="sxs-lookup"><span data-stu-id="05de5-108">This version of COM+ events does not support a distributed event store.</span></span> <span data-ttu-id="05de5-109">訂閱者必須在每一部要接收通知的電腦上訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="05de5-109">A subscriber must subscribe to an event on each computer from which it wants to receive notification.</span></span> <span data-ttu-id="05de5-110">或者，您可以在中央電腦上註冊事件類別物件和訂用帳戶，並從您發佈事件的遠端電腦，將此事件類別物件具現化。</span><span class="sxs-lookup"><span data-stu-id="05de5-110">As an alternative, you can register the event class object and subscriptions on a central computer and instantiate this event class object from the remote computers on which you publish events.</span></span> <span data-ttu-id="05de5-111">事件的傳遞是由 DCOM 或由 COM + 佇列元件服務提供。</span><span class="sxs-lookup"><span data-stu-id="05de5-111">Delivery of events is provided either by DCOM or by the COM+ queued components service.</span></span> <span data-ttu-id="05de5-112">如需使用 COM + 佇列元件服務的詳細資訊，請參閱使用 com + [事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)。</span><span class="sxs-lookup"><span data-stu-id="05de5-112">For more information about using the COM+ queued components service, see [Using COM+ Events with COM+ Queued Components](using-com--events-with-com--queued-components.md).</span></span>

 

<span data-ttu-id="05de5-113">根據預設，COM + 事件服務會以未決定或可重複的順序，一次引發一個事件。</span><span class="sxs-lookup"><span data-stu-id="05de5-113">By default, the COM+ events service fires events one at a time, in no determined or repeatable order.</span></span> <span data-ttu-id="05de5-114">需要控制訂閱者接收事件之順序的發行者，可以執行發行者篩選。</span><span class="sxs-lookup"><span data-stu-id="05de5-114">Publishers that need to control the order in which subscribers receive an event can implement a publisher filter.</span></span> <span data-ttu-id="05de5-115"> (需詳細資訊，請參閱 [在 COM + 中篩選事件](filtering-events-in-com-.md)) </span><span class="sxs-lookup"><span data-stu-id="05de5-115">(For more information, see [Filtering Events in COM+](filtering-events-in-com-.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="05de5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="05de5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05de5-117">在 COM + 中篩選事件</span><span class="sxs-lookup"><span data-stu-id="05de5-117">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="05de5-118">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="05de5-118">Subscriptions</span></span>](subscriptions.md)
</dt> <dt>

[<span data-ttu-id="05de5-119">COM + 事件類別物件</span><span class="sxs-lookup"><span data-stu-id="05de5-119">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> <dt>

[<span data-ttu-id="05de5-120">使用 com + 事件與 COM + 佇列元件</span><span class="sxs-lookup"><span data-stu-id="05de5-120">Using COM+ Events with COM+ Queued Components</span></span>](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



