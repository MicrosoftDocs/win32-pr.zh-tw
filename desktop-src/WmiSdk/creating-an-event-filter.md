---
description: 事件篩選器是一種 WMI 類別，描述 WMI 傳遞給實體取用者的事件。
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: 建立事件篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980081"
---
# <a name="creating-an-event-filter"></a><span data-ttu-id="b6f28-103">建立事件篩選器</span><span class="sxs-lookup"><span data-stu-id="b6f28-103">Creating an Event Filter</span></span>

<span data-ttu-id="b6f28-104">事件篩選器是一種 WMI 類別，描述 WMI 傳遞給實體取用者的事件。</span><span class="sxs-lookup"><span data-stu-id="b6f28-104">An event filter is a WMI class that describes which events WMI delivers to a physical consumer.</span></span> <span data-ttu-id="b6f28-105">例如，事件篩選器可以指示 WMI 傳遞給取用者所有的電源管理事件，或所有系統重新開機事件。</span><span class="sxs-lookup"><span data-stu-id="b6f28-105">For example, an event filter can instruct WMI to deliver to a consumer all power management events, or all system reboot events.</span></span> <span data-ttu-id="b6f28-106">事件篩選器也會說明 WMI 傳遞事件的條件。</span><span class="sxs-lookup"><span data-stu-id="b6f28-106">An event filter also describes the conditions under which WMI delivers the events.</span></span> <span data-ttu-id="b6f28-107">事件篩選器可以指定內建或外來事件;而且篩選可以參考源自命名空間的事件，也就是篩選的命名空間以外的事件。</span><span class="sxs-lookup"><span data-stu-id="b6f28-107">An event filter can specify an intrinsic or extrinsic event; and the filter can refer to events that originate in the namespace—that is, other than the namespace of the filter.</span></span> <span data-ttu-id="b6f28-108">永久取用者在取用者、篩選和系結實例中必須具有相同的 [**CreatorSID**](--eventconsumer.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6f28-108">The permanent consumer must have the same [**CreatorSID**](--eventconsumer.md) in the consumer, filter, and binding instances.</span></span> <span data-ttu-id="b6f28-109">如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="b6f28-109">For more information, see [Receiving Events Securely](receiving-events-securely.md).</span></span>

<span data-ttu-id="b6f28-110">下列程式說明如何建立事件篩選準則。</span><span class="sxs-lookup"><span data-stu-id="b6f28-110">The following procedure describes how to create an event filter.</span></span>

<span data-ttu-id="b6f28-111">**若要建立事件篩選器**</span><span class="sxs-lookup"><span data-stu-id="b6f28-111">**To create an event filter**</span></span>

1.  <span data-ttu-id="b6f28-112">建立 WMI [**\_ \_ >eventfilter**](--eventfilter.md)系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b6f28-112">Create an instance of the WMI [**\_\_EventFilter**](--eventfilter.md) system class.</span></span>
2.  <span data-ttu-id="b6f28-113">以下列兩種方式之一，使用 [ **名稱** ] 屬性建立篩選器的唯一識別碼：</span><span class="sxs-lookup"><span data-stu-id="b6f28-113">Create a unique identifier for your filter with the **Name** property, in one of two ways:</span></span>

    -   <span data-ttu-id="b6f28-114">使用私用配置。</span><span class="sxs-lookup"><span data-stu-id="b6f28-114">Use a private scheme.</span></span>

        <span data-ttu-id="b6f28-115">只要您不與其他篩選命名配置發生衝突，就可以任意命名事件篩選器的運作方式。</span><span class="sxs-lookup"><span data-stu-id="b6f28-115">Arbitrarily naming your event filters works as long as you do not conflict with other filter naming schemes.</span></span> <span data-ttu-id="b6f28-116">您必須避免命名衝突，因為加入具有重複 **名稱** 值的實例會覆寫舊的實例。</span><span class="sxs-lookup"><span data-stu-id="b6f28-116">You must avoid naming conflicts because adding an instance with a duplicate **Name** value overwrites the old instance.</span></span>

    -   <span data-ttu-id="b6f28-117">使用全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="b6f28-117">Use a globally unique identifier (GUID).</span></span>

        <span data-ttu-id="b6f28-118">如果您將 [ **名稱** ] 保留空白，WMI 就會填滿 GUID 的 **名稱** 。</span><span class="sxs-lookup"><span data-stu-id="b6f28-118">If you leave **Name** empty, WMI fills **Name** with a GUID.</span></span>

3.  <span data-ttu-id="b6f28-119">描述您想要使用 **查詢** 屬性篩選的事件種類。</span><span class="sxs-lookup"><span data-stu-id="b6f28-119">Describe the type of event you want filtered with the **Query** property.</span></span>

    <span data-ttu-id="b6f28-120">**查詢** 屬性包含 WMI 查詢語言 (WQL) 查詢，可描述您想要篩選的事件種類。</span><span class="sxs-lookup"><span data-stu-id="b6f28-120">The **Query** property contains the WMI Query Language (WQL) query that describes the type of event you want filtered.</span></span> <span data-ttu-id="b6f28-121">您可以使用各種不同的運算子和 WQL 延伸來進行精確的篩選。</span><span class="sxs-lookup"><span data-stu-id="b6f28-121">You can achieve precise filtering using a variety of operators and extensions to WQL.</span></span>

    <span data-ttu-id="b6f28-122">當來自永久性事件取用者的查詢失敗時，就會產生 NT 記錄事件。</span><span class="sxs-lookup"><span data-stu-id="b6f28-122">An NT Log event is generated when a query from a permanent event consumer fails.</span></span> <span data-ttu-id="b6f28-123">事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。</span><span class="sxs-lookup"><span data-stu-id="b6f28-123">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

    <span data-ttu-id="b6f28-124">WMI 比廣泛查詢更有效率地處理限制的特定查詢。</span><span class="sxs-lookup"><span data-stu-id="b6f28-124">WMI is more efficient at processing restrictive, specific queries than broad queries.</span></span> <span data-ttu-id="b6f28-125">藉由建立特定查詢，您可以避免不必要的處理序間通訊和網路流量。</span><span class="sxs-lookup"><span data-stu-id="b6f28-125">By creating a specific query, you can avoid unnecessary inter-process communication and network traffic.</span></span> <span data-ttu-id="b6f28-126">在提供者所產生的事件案例中，WMI 會對提供者執行篩選，這可確保只有符合篩選準則的事件會產生進程間的通訊成本。</span><span class="sxs-lookup"><span data-stu-id="b6f28-126">In cases of events generated by a provider, WMI performs the filtering in process to the provider; this ensures that only events matching the filter incur the interprocess communication cost.</span></span> <span data-ttu-id="b6f28-127">如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="b6f28-127">For more information, see [Querying WMI](querying-wmi.md).</span></span>

4.  <span data-ttu-id="b6f28-128">將 **QueryLanguage** 屬性設定為您在 **查詢** 屬性中使用的查詢語言類型。</span><span class="sxs-lookup"><span data-stu-id="b6f28-128">Set the **QueryLanguage** property to the type of query language you use in the **Query** property.</span></span>

    <span data-ttu-id="b6f28-129">您幾乎一律會將 **QueryLanguage** 設定為「WQL」。</span><span class="sxs-lookup"><span data-stu-id="b6f28-129">You will almost always set **QueryLanguage** to "WQL".</span></span>

<span data-ttu-id="b6f28-130">下列程式碼範例描述事件篩選器，每次 WMI 在根 cimv2 命名空間中建立 [**\_ \_ TimerEvent**](--timerevent.md)類別的實例時，就會對事件發出信號 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b6f28-130">The following code example describes an event filter that signals an event each time WMI creates an instance of the [**\_\_TimerEvent**](--timerevent.md) class in the root\\cimv2 namespace.</span></span>

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

<span data-ttu-id="b6f28-131">**EventNamespace** 屬性會指定事件來源的命名空間。</span><span class="sxs-lookup"><span data-stu-id="b6f28-131">The **EventNamespace** property specifies the namespace from which the events originate.</span></span> <span data-ttu-id="b6f28-132">您不需要在事件來源的命名空間中建立篩選準則的實例。</span><span class="sxs-lookup"><span data-stu-id="b6f28-132">You do not have to create an instance of the filters in the namespace where the events originate.</span></span> <span data-ttu-id="b6f28-133">如果您沒有指定命名空間，則 WMI 會在預設命名空間中建立篩選。</span><span class="sxs-lookup"><span data-stu-id="b6f28-133">If you do not specify the namespace, then WMI creates the filter in the default namespace.</span></span> <span data-ttu-id="b6f28-134">內建事件類別（例如 [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) ）可在每個命名空間中使用。</span><span class="sxs-lookup"><span data-stu-id="b6f28-134">The intrinsic events classes, such as [**\_\_InstanceOperationEvent**](--instanceoperationevent.md) are available in every namespace.</span></span>

<span data-ttu-id="b6f28-135">若要為您的邏輯取用者註冊事件通知，您必須將事件篩選器系結至邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="b6f28-135">To register your logical consumer for event notifications, you must bind the event filters to a logical consumer.</span></span> <span data-ttu-id="b6f28-136">如需詳細資訊，請參閱系結 [事件篩選與邏輯取用者](binding-an-event-filter-with-a-logical-consumer.md)。</span><span class="sxs-lookup"><span data-stu-id="b6f28-136">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md).</span></span>

 

 



