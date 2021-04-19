---
title: 使用 Windows 事件收集器
description: 本節列出的主題說明可以使用 Windows 事件收集器 SDK 完成的工作。 所有工作的程式碼範例和說明都包含在下列每個主題中。
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969848"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="346a9-104">使用 Windows 事件收集器</span><span class="sxs-lookup"><span data-stu-id="346a9-104">Using Windows Event Collector</span></span>

<span data-ttu-id="346a9-105">本節列出的主題說明可以使用 Windows 事件收集器 SDK 完成的工作。</span><span class="sxs-lookup"><span data-stu-id="346a9-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="346a9-106">所有工作的程式碼範例和說明都包含在下列每個主題中。</span><span class="sxs-lookup"><span data-stu-id="346a9-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="346a9-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="346a9-107">In This Section</span></span>

-   [<span data-ttu-id="346a9-108">建立收集器起始的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="346a9-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-109">提供用來建立收集器起始訂用帳戶的資訊和 c + + 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="346a9-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="346a9-110">收集器起始的訂用帳戶可讓您在本機電腦上接收事件， (從遠端電腦轉送的事件收集器)  (事件來源) 。</span><span class="sxs-lookup"><span data-stu-id="346a9-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="346a9-111">設定來源起始的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="346a9-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="346a9-112">提供用來建立來源起始訂用帳戶的資訊和 c + + 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="346a9-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="346a9-113">來源起始的訂用帳戶可讓您在本機電腦上接收事件 (事件收集器) 從遠端電腦轉送 (事件來源) 而不指定訂用帳戶中的事件來源。</span><span class="sxs-lookup"><span data-stu-id="346a9-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="346a9-114">將事件來源新增至收集器起始的訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="346a9-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-115">提供資訊和 c + + 程式碼範例，以將事件來源 (本機電腦或遠端電腦) 新增至收集器起始的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="346a9-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="346a9-116">收集器起始的訂用帳戶無法開始收集事件，直到將事件來源新增至訂用帳戶為止。</span><span class="sxs-lookup"><span data-stu-id="346a9-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="346a9-117">建立硬體事件訂閱</span><span class="sxs-lookup"><span data-stu-id="346a9-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="346a9-118">提供有關如何建立事件訂閱，以便從已安裝基礎板管理控制器 (BMC) 的電腦接收硬體事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="346a9-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="346a9-119">刪除事件收集器訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="346a9-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-120">提供從本機電腦刪除事件收集器訂用帳戶的資訊和 c + + 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="346a9-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="346a9-121">顯示事件收集器訂用帳戶的屬性</span><span class="sxs-lookup"><span data-stu-id="346a9-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-122">提供資訊和 c + + 程式碼範例，以顯示事件收集器訂用帳戶的屬性值。</span><span class="sxs-lookup"><span data-stu-id="346a9-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="346a9-123">屬性值可提供有用的資訊，例如事件來源的位址、訂用帳戶和事件來源的狀態，以及事件傳遞方式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="346a9-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="346a9-124">顯示事件收集器訂用帳戶的狀態</span><span class="sxs-lookup"><span data-stu-id="346a9-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-125">提供資訊和 c + + 程式碼範例，以顯示與事件收集器訂用帳戶相關聯之事件來源的執行時間狀態。</span><span class="sxs-lookup"><span data-stu-id="346a9-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="346a9-126">這可讓您查看有助於解決問題的錯誤訊息，以防止事件來源轉送事件。</span><span class="sxs-lookup"><span data-stu-id="346a9-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="346a9-127">列出事件收集器訂閱</span><span class="sxs-lookup"><span data-stu-id="346a9-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="346a9-128">提供資訊和 c + + 程式碼範例，以列出存在於本機電腦上的訂閱。</span><span class="sxs-lookup"><span data-stu-id="346a9-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="346a9-129">您可以使用以此範例取得的訂用帳戶名稱來刪除訂用帳戶、將事件來源新增至訂用帳戶、取出訂用帳戶的屬性，或查看訂用帳戶的狀態。</span><span class="sxs-lookup"><span data-stu-id="346a9-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="346a9-130">從收集器起始的訂用帳戶中移除事件來源</span><span class="sxs-lookup"><span data-stu-id="346a9-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-131">提供資訊和 c + + 程式碼範例，以從收集器起始的訂用帳戶中移除事件來源。</span><span class="sxs-lookup"><span data-stu-id="346a9-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="346a9-132">您可以從收集器起始的訂用帳戶中移除事件來源，而不需要停用訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="346a9-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="346a9-133">重試事件收集器訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="346a9-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="346a9-134">提供資訊和 c + + 程式碼範例，以在一或多個事件來源失敗時重試事件收集器訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="346a9-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="346a9-135">您可以重試單一事件來源，也可以重試整個訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="346a9-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




