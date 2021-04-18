---
description: 關於篩選圖形管理員
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: 關於篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510221"
---
# <a name="about-the-filter-graph-manager"></a><span data-ttu-id="e4292-103">關於篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="e4292-103">About the Filter Graph Manager</span></span>

<span data-ttu-id="e4292-104">[篩選圖形管理員](filter-graph-manager.md)是一個 COM 物件，可控制篩選圖形中的篩選。</span><span class="sxs-lookup"><span data-stu-id="e4292-104">The [Filter Graph Manager](filter-graph-manager.md) is a COM object that controls the filters in a filter graph.</span></span> <span data-ttu-id="e4292-105">它會執行許多功能，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="e4292-105">It performs many functions, including the following:</span></span>

-   <span data-ttu-id="e4292-106">協調篩選之間的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="e4292-106">Coordinating state changes among the filters.</span></span>
-   <span data-ttu-id="e4292-107">建立參考時鐘。</span><span class="sxs-lookup"><span data-stu-id="e4292-107">Establishing a reference clock.</span></span>
-   <span data-ttu-id="e4292-108">將事件傳達回應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4292-108">Communicating events back to the application.</span></span>
-   <span data-ttu-id="e4292-109">提供應用程式用來建立篩選圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="e4292-109">Providing methods for applications to build the filter graph.</span></span>

<span data-ttu-id="e4292-110">其中每個函式都會在這裡簡短描述。</span><span class="sxs-lookup"><span data-stu-id="e4292-110">Each of these functions is described briefly here.</span></span> <span data-ttu-id="e4292-111">您可以在檔的其他位置找到詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e4292-111">Details can be found elsewhere in the documentation.</span></span>

<span data-ttu-id="e4292-112">**狀態變更**。</span><span class="sxs-lookup"><span data-stu-id="e4292-112">**State changes**.</span></span> <span data-ttu-id="e4292-113">篩選準則內的狀態變更必須以特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="e4292-113">State changes within filters must occur in a particular order.</span></span> <span data-ttu-id="e4292-114">因此，應用程式不會直接對篩選發出狀態變更命令。</span><span class="sxs-lookup"><span data-stu-id="e4292-114">Therefore, the application does not issue state-change commands directly to the filters.</span></span> <span data-ttu-id="e4292-115">相反地，它會為篩選圖形管理員提供單一命令，此命令會將命令散發給每個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e4292-115">Instead, it gives a single command to the Filter Graph Manager, which distributes the command to each of the filters.</span></span> <span data-ttu-id="e4292-116">搜尋的運作方式類似：應用程式會向篩選圖形管理員提供搜尋命令，該命令會將其散發至篩選。</span><span class="sxs-lookup"><span data-stu-id="e4292-116">Seeking works in a similar fashion: The application gives a seek command to the Filter Graph Manager, which distributes it to the filters.</span></span>

<span data-ttu-id="e4292-117">**參考時鐘**。</span><span class="sxs-lookup"><span data-stu-id="e4292-117">**Reference clock**.</span></span> <span data-ttu-id="e4292-118">圖形中的所有篩選都使用相同的時鐘，稱為 *參考時鐘*。</span><span class="sxs-lookup"><span data-stu-id="e4292-118">All of the filters in the graph use the same clock, called a *reference clock*.</span></span> <span data-ttu-id="e4292-119">參考時鐘可確保同步處理所有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e4292-119">The reference clock ensures that all the streams are synchronized.</span></span> <span data-ttu-id="e4292-120">應轉譯影片畫面或音訊樣本的時間，稱為呈現 *時間*。</span><span class="sxs-lookup"><span data-stu-id="e4292-120">The time at which a video frame or audio sample should be rendered is called the *presentation time*.</span></span> <span data-ttu-id="e4292-121">呈現時間是相對於參考時鐘來測量。</span><span class="sxs-lookup"><span data-stu-id="e4292-121">The presentation time is measured relative to the reference clock.</span></span> <span data-ttu-id="e4292-122">篩選圖形管理員選擇參考時鐘，通常是音效卡上的時鐘或系統時鐘。</span><span class="sxs-lookup"><span data-stu-id="e4292-122">The Filter Graph Manager chooses a reference clock, usually either the clock on the sound card, or the system clock.</span></span>

<span data-ttu-id="e4292-123">**圖形事件**。</span><span class="sxs-lookup"><span data-stu-id="e4292-123">**Graph events**.</span></span> <span data-ttu-id="e4292-124">篩選圖形管理員會使用事件佇列來通知應用程式發生在篩選圖形中的事件。</span><span class="sxs-lookup"><span data-stu-id="e4292-124">The Filter Graph Manager uses an event queue to inform the application of events that occur in the filter graph.</span></span> <span data-ttu-id="e4292-125">這項機制類似于 Windows 訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="e4292-125">This mechanism is similar to a Windows message loop.</span></span>

<span data-ttu-id="e4292-126">**圖形建立方法**。</span><span class="sxs-lookup"><span data-stu-id="e4292-126">**Graph-building methods**.</span></span> <span data-ttu-id="e4292-127">篩選圖形管理員會提供方法，讓應用程式將篩選準則新增至圖形、將篩選連接至其他篩選，以及中斷篩選。</span><span class="sxs-lookup"><span data-stu-id="e4292-127">The Filter Graph Manager provides methods for the application to add filters to the graph, connect filters to other filters, and disconnect filters.</span></span>

<span data-ttu-id="e4292-128">篩選圖形管理員未處理的一個函式，是將資料從一個篩選準則移至下一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="e4292-128">One function the Filter Graph Manager does not handle is moving data from one filter to the next.</span></span> <span data-ttu-id="e4292-129">這是由篩選準則本身透過其 pin 連接來完成。</span><span class="sxs-lookup"><span data-stu-id="e4292-129">This is done by the filters themselves, through their pin connections.</span></span> <span data-ttu-id="e4292-130">處理一律會在個別的執行緒上發生。</span><span class="sxs-lookup"><span data-stu-id="e4292-130">Processing always happens on a separate thread.</span></span>

> [!Note]  
> <span data-ttu-id="e4292-131">篩選準則一律是無限制執行緒、位於與篩選圖形管理員相同的進程中，並從同進程伺服器載入。</span><span class="sxs-lookup"><span data-stu-id="e4292-131">Filters are always free-threaded, reside in the same process as the Filter Graph Manager, and are loaded from in-process servers.</span></span> <span data-ttu-id="e4292-132">因此，方法呼叫不會在篩選之間，或在篩選器和篩選圖形管理員之間進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="e4292-132">Therefore, method calls are not marshaled between filters, or between filters and the Filter Graph Manager.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e4292-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4292-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4292-134">篩選圖形中的資料流程</span><span class="sxs-lookup"><span data-stu-id="e4292-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="e4292-135">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="e4292-135">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="e4292-136">設定圖形時鐘</span><span class="sxs-lookup"><span data-stu-id="e4292-136">Setting the Graph Clock</span></span>](setting-the-graph-clock.md)
</dt> <dt>

[<span data-ttu-id="e4292-137">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="e4292-137">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



