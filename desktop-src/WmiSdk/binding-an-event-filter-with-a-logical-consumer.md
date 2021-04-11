---
description: 建立邏輯事件取用者和事件篩選器之後，您必須連結它們，以註冊邏輯取用者接收篩選所指定之事件的通知。
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: 使用邏輯取用者來系結事件篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851672"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a><span data-ttu-id="14837-103">使用邏輯取用者來系結事件篩選器</span><span class="sxs-lookup"><span data-stu-id="14837-103">Binding an Event Filter with a Logical Consumer</span></span>

<span data-ttu-id="14837-104">建立邏輯事件取用者和事件篩選器之後，您必須連結它們，以註冊邏輯取用者接收篩選所指定之事件的通知。</span><span class="sxs-lookup"><span data-stu-id="14837-104">After you create the logical event consumer and the event filter you must link them, which registers the logical consumer to receive notification about the events specified by the filter.</span></span>

<span data-ttu-id="14837-105">下列程式說明如何將事件篩選器與邏輯取用者系結。</span><span class="sxs-lookup"><span data-stu-id="14837-105">The following procedure describes how to bind an event filter with a logical consumer.</span></span>

<span data-ttu-id="14837-106">**系結事件篩選器與邏輯取用者**</span><span class="sxs-lookup"><span data-stu-id="14837-106">**To bind an event filter with a logical consumer**</span></span>

1.  <span data-ttu-id="14837-107">在 WMI 存放庫中建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="14837-107">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) system class in the WMI repository.</span></span>

    <span data-ttu-id="14837-108">[**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別是一個關聯類別，可透過 **篩選** 和取用 **者** 參考屬性，將事件篩選準則實例和邏輯取用者實例連結在一起。</span><span class="sxs-lookup"><span data-stu-id="14837-108">The [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class is an association class that links the event filter instance and the logical consumer instance together through the **Filter** and **Consumer** reference properties.</span></span> <span data-ttu-id="14837-109">如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。</span><span class="sxs-lookup"><span data-stu-id="14837-109">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

2.  <span data-ttu-id="14837-110">將 [ **篩選** ] 屬性設定為篩選準則的實例。</span><span class="sxs-lookup"><span data-stu-id="14837-110">Set the **Filter** property to the instance of your filter.</span></span>
3.  <span data-ttu-id="14837-111">將取用 **者** 屬性設定為邏輯取用者的實例。</span><span class="sxs-lookup"><span data-stu-id="14837-111">Set the **Consumer** property to the instance of your logical consumer.</span></span>
4.  <span data-ttu-id="14837-112">設定 **DeliverSynchronously** 屬性，以判斷您想要的傳遞類型。</span><span class="sxs-lookup"><span data-stu-id="14837-112">Set the **DeliverSynchronously** property to determine the type of delivery you want.</span></span>

    <span data-ttu-id="14837-113">**DeliverSynchronously** 屬性可決定 WMI 何時以同步或非同步方式傳遞事件通知。</span><span class="sxs-lookup"><span data-stu-id="14837-113">The **DeliverSynchronously** property determines when WMI delivers event notifications synchronously or asynchronously.</span></span> <span data-ttu-id="14837-114">將這個屬性設定為 **TRUE** 會要求同步傳遞。</span><span class="sxs-lookup"><span data-stu-id="14837-114">Setting this property to **TRUE** requests a synchronous delivery.</span></span> <span data-ttu-id="14837-115">只有在永久取用者可以在大約100毫秒內處理事件時，才使用同步傳遞。</span><span class="sxs-lookup"><span data-stu-id="14837-115">Use synchronous delivery only when the permanent consumer can process events within approximately 100 microseconds.</span></span>

    > [!Note]  
    > <span data-ttu-id="14837-116">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="14837-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="14837-117">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="14837-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

     

5.  <span data-ttu-id="14837-118">當您取消註冊邏輯事件取用者時，請務必刪除 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例。</span><span class="sxs-lookup"><span data-stu-id="14837-118">When unregistering your logical event consumer, ensure you delete the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance.</span></span>

    <span data-ttu-id="14837-119">每個 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例都代表特定事件通知的註冊。</span><span class="sxs-lookup"><span data-stu-id="14837-119">Each [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance represents a registration for a specific event notification.</span></span> <span data-ttu-id="14837-120">當您刪除系結時，WMI 會停用註冊。</span><span class="sxs-lookup"><span data-stu-id="14837-120">When you delete a binding, WMI deactivates the registration.</span></span> <span data-ttu-id="14837-121">您可能必須刪除邏輯取用者和事件篩選準則實例，才能根據執行來停用註冊。</span><span class="sxs-lookup"><span data-stu-id="14837-121">You might have to delete the logical consumer and event filter instances to deactivate registration, depending on the implementation.</span></span>

<span data-ttu-id="14837-122">下列程式碼範例會顯示 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)實例，此實例會將 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別的實例與特定事件篩選器產生關聯 (在建立 [邏輯取用者](creating-a-logical-consumer.md)主題中建立事件取用者的實例，並在 [[建立事件篩選器](creating-an-event-filter.md)] 主題中建立事件篩選器) 。</span><span class="sxs-lookup"><span data-stu-id="14837-122">The following code example shows you a [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instance that associates an instance of an [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class with a specific event filter (the instance of the event consumer was created in the [Creating a Logical Consumer](creating-a-logical-consumer.md) topic, and the event filter was created in the [Creating an Event Filter](creating-an-event-filter.md) topic).</span></span>

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="14837-123">除非取用者是本機系統管理員群組的成員，否則兩個取用者（ [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 和 [**CommandLineEventConsumer**](commandlineeventconsumer.md)）將無法運作。</span><span class="sxs-lookup"><span data-stu-id="14837-123">Two consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md), will not work unless their creator is a member of the local Administrators group.</span></span>

<span data-ttu-id="14837-124">**:** 當系統管理員建立訂用帳戶時，它的 SID 不會用在 **CreatorSID** 屬性中，而是改用本機 Administrators 群組的 sid。</span><span class="sxs-lookup"><span data-stu-id="14837-124">**:** When an administrator creates a subscription, his SID is not used for the **CreatorSID** property, but the SID of the local Administrators group is used instead.</span></span> <span data-ttu-id="14837-125">因此，實例可以由不同的系統管理員建立，且訂用帳戶仍可運作。</span><span class="sxs-lookup"><span data-stu-id="14837-125">Therefore, instances can be created by different administrators and the subscription will still work.</span></span> <span data-ttu-id="14837-126">如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="14837-126">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="14837-127">當篩選準則系結至邏輯取用者時，Windows (ETW) 的 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 會記錄事件。</span><span class="sxs-lookup"><span data-stu-id="14837-127">When a filter is bound to a logical consumer the event is recorded by [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW).</span></span> <span data-ttu-id="14837-128">如需詳細資訊，請參閱 [追蹤 WMI 活動](tracing-wmi-activity.md)。</span><span class="sxs-lookup"><span data-stu-id="14837-128">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14837-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="14837-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14837-130">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="14837-130">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

 
