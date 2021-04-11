---
description: 篩選開發人員的資料流程
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: 篩選開發人員的資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025786"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="97ae1-103">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="97ae1-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="97ae1-104">本節將詳細說明如何透過篩選圖形來移動資料。</span><span class="sxs-lookup"><span data-stu-id="97ae1-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="97ae1-105">它著重于使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 或 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面的本機記憶體傳輸。</span><span class="sxs-lookup"><span data-stu-id="97ae1-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="97ae1-106">它適用于撰寫自己的自訂篩選器的開發人員。</span><span class="sxs-lookup"><span data-stu-id="97ae1-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="97ae1-107">如需 Microsoft DirectShow 如何處理資料流程的一般簡介，請參閱 [篩選圖形中的](data-flow-in-the-filter-graph.md)資料流程。</span><span class="sxs-lookup"><span data-stu-id="97ae1-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="97ae1-108">許多資料會透過篩選圖形來移動。</span><span class="sxs-lookup"><span data-stu-id="97ae1-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="97ae1-109">它大致分為兩類：媒體資料和控制資料。</span><span class="sxs-lookup"><span data-stu-id="97ae1-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="97ae1-110">一般情況下，媒體資料會傳輸下游，而控制資料會傳輸到上游。</span><span class="sxs-lookup"><span data-stu-id="97ae1-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="97ae1-111">媒體資料包括構成資料流程的影片畫面、音訊範例、MPEG 封包等等，但也包含排清命令、串流結束通知，以及其他與資料流程一起傳送的資料。</span><span class="sxs-lookup"><span data-stu-id="97ae1-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="97ae1-112">控制資料不是媒體資料流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="97ae1-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="97ae1-113">控制資料的範例包括品質控制要求和搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="97ae1-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="97ae1-114">本節包含下列文章。</span><span class="sxs-lookup"><span data-stu-id="97ae1-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="97ae1-115">傳遞範例</span><span class="sxs-lookup"><span data-stu-id="97ae1-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="97ae1-116">處理資料</span><span class="sxs-lookup"><span data-stu-id="97ae1-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="97ae1-117">資料流程結束通知</span><span class="sxs-lookup"><span data-stu-id="97ae1-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="97ae1-118">新區段</span><span class="sxs-lookup"><span data-stu-id="97ae1-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="97ae1-119">沖洗</span><span class="sxs-lookup"><span data-stu-id="97ae1-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="97ae1-120">尋求</span><span class="sxs-lookup"><span data-stu-id="97ae1-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="97ae1-121">動態格式變更</span><span class="sxs-lookup"><span data-stu-id="97ae1-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="97ae1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="97ae1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ae1-123">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="97ae1-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="97ae1-124">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="97ae1-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="97ae1-125">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="97ae1-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



