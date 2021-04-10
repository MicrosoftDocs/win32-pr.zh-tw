---
description: 控制篩選圖形的介面
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: 控制篩選圖形的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688231"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="1d3f8-103">控制篩選圖形的介面</span><span class="sxs-lookup"><span data-stu-id="1d3f8-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="1d3f8-104">這些介面提供控制篩選圖形的方法。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="1d3f8-105">介面</span><span class="sxs-lookup"><span data-stu-id="1d3f8-105">Interface</span></span>                                  | <span data-ttu-id="1d3f8-106">描述</span><span class="sxs-lookup"><span data-stu-id="1d3f8-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d3f8-107">**IAMClockAdjust**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="1d3f8-108">調整圖形時鐘。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="1d3f8-109">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="1d3f8-110">同步處理篩選圖形中的即時資料流。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="1d3f8-111">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="1d3f8-112">控制篩選準則的鏈。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="1d3f8-113">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="1d3f8-114">執行、暫停和停止篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="1d3f8-115"> (也提供自動化相容的方法來建立圖形。 ) </span><span class="sxs-lookup"><span data-stu-id="1d3f8-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="1d3f8-116">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="1d3f8-117">回應圖形中的事件。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="1d3f8-118">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="1d3f8-119">在檔案中搜尋。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="1d3f8-120">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="1d3f8-121">稍後要執行的佇列命令。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="1d3f8-122">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="1d3f8-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="1d3f8-123">畫面-逐步執行影片串流。</span><span class="sxs-lookup"><span data-stu-id="1d3f8-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



