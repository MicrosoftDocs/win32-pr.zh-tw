---
description: 執行緒和重要區段
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: 執行緒和重要區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321111"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="413a0-103">執行緒和重要區段</span><span class="sxs-lookup"><span data-stu-id="413a0-103">Threads and Critical Sections</span></span>

<span data-ttu-id="413a0-104">本節說明 DirectShow 篩選器中的執行緒，以及您應採取的步驟，以避免在自訂篩選器中發生損毀或鎖死。</span><span class="sxs-lookup"><span data-stu-id="413a0-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="413a0-105">本節中的範例會使用虛擬程式碼來說明您需要撰寫的程式碼。</span><span class="sxs-lookup"><span data-stu-id="413a0-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="413a0-106">它們假設自訂篩選器使用衍生自 DirectShow 基類的類別，如下所示：</span><span class="sxs-lookup"><span data-stu-id="413a0-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="413a0-107">CMyInputPin：衍生自 [**CBaseInputPin**](cbaseinputpin.md)。</span><span class="sxs-lookup"><span data-stu-id="413a0-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="413a0-108">CMyOutputPin：衍生自 [**CBaseOutputPin**](cbaseoutputpin.md)。</span><span class="sxs-lookup"><span data-stu-id="413a0-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="413a0-109">CMyFilter：衍生自 [**CBaseFilter**](cbasefilter.md)。</span><span class="sxs-lookup"><span data-stu-id="413a0-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="413a0-110">CMyInputAllocator：輸入釘選器，衍生自 [**CMemAllocator**](cmemallocator.md)。</span><span class="sxs-lookup"><span data-stu-id="413a0-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="413a0-111">並非每個篩選都需要自訂配置器。</span><span class="sxs-lookup"><span data-stu-id="413a0-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="413a0-112">針對許多篩選準則， **CMemAllocator** 類別已足夠。</span><span class="sxs-lookup"><span data-stu-id="413a0-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="413a0-113">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="413a0-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="413a0-114">串流和應用程式執行緒</span><span class="sxs-lookup"><span data-stu-id="413a0-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="413a0-115">暫停中</span><span class="sxs-lookup"><span data-stu-id="413a0-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="413a0-116">接收和傳遞範例</span><span class="sxs-lookup"><span data-stu-id="413a0-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="413a0-117">傳遞資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="413a0-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="413a0-118">清除資料</span><span class="sxs-lookup"><span data-stu-id="413a0-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="413a0-119">停止中</span><span class="sxs-lookup"><span data-stu-id="413a0-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="413a0-120">取得緩衝區</span><span class="sxs-lookup"><span data-stu-id="413a0-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="413a0-121">串流執行緒和篩選圖形管理員</span><span class="sxs-lookup"><span data-stu-id="413a0-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="413a0-122">篩選準則執行緒的摘要</span><span class="sxs-lookup"><span data-stu-id="413a0-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="413a0-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="413a0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="413a0-124">篩選開發人員的資料流程</span><span class="sxs-lookup"><span data-stu-id="413a0-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="413a0-125">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="413a0-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



