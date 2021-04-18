---
description: 動態圖表建立
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: 動態圖表建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971287"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="ba276-103">動態圖表建立</span><span class="sxs-lookup"><span data-stu-id="ba276-103">Dynamic Graph Building</span></span>

<span data-ttu-id="ba276-104">如果您需要修改現有的篩選圖形，您可以停止圖形、進行變更，然後重新開機圖形。</span><span class="sxs-lookup"><span data-stu-id="ba276-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="ba276-105">這通常是最好的方法。</span><span class="sxs-lookup"><span data-stu-id="ba276-105">This is usually the best approach.</span></span> <span data-ttu-id="ba276-106">不過，在某些情況下，您可能會想要在圖形仍在執行時加以變更。</span><span class="sxs-lookup"><span data-stu-id="ba276-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="ba276-107">例如：</span><span class="sxs-lookup"><span data-stu-id="ba276-107">For example:</span></span>

-   <span data-ttu-id="ba276-108">應用程式會在播放期間插入影片效果篩選。</span><span class="sxs-lookup"><span data-stu-id="ba276-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="ba276-109">來源篩選器會切換媒體類型中途，可能需要新的解壓縮篩選器。</span><span class="sxs-lookup"><span data-stu-id="ba276-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="ba276-110">應用程式會將新的影片串流新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="ba276-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="ba276-111">這些都是 *動態圖形建築物* 的範例，這是在圖形繼續執行時涵蓋對篩選圖形任何變更類型的詞彙。</span><span class="sxs-lookup"><span data-stu-id="ba276-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="ba276-112">動態圖形建築物可以由應用程式或圖形中的篩選器起始。</span><span class="sxs-lookup"><span data-stu-id="ba276-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="ba276-113">可能有三種不同的案例：</span><span class="sxs-lookup"><span data-stu-id="ba276-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="ba276-114">[動態格式變更](dynamic-format-changes.md)：篩選準則可以變更中途格式，而不需要移除或取代任何篩選準則。</span><span class="sxs-lookup"><span data-stu-id="ba276-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="ba276-115">[動態重新連接](dynamic-reconnection.md)：藉由加入或移除篩選來變更圖形。</span><span class="sxs-lookup"><span data-stu-id="ba276-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="ba276-116">[篩選鏈](filter-chains.md)：新增、移除及控制篩選的鏈。</span><span class="sxs-lookup"><span data-stu-id="ba276-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba276-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba276-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba276-118">關於 DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba276-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



