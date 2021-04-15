---
description: DirectShow 中的資料流程總覽
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: DirectShow 中的資料流程總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467826"
---
# <a name="overview-of-data-flow-in-directshow"></a><span data-ttu-id="02bed-103">DirectShow 中的資料流程總覽</span><span class="sxs-lookup"><span data-stu-id="02bed-103">Overview of Data Flow in DirectShow</span></span>

<span data-ttu-id="02bed-104">本節將全面探討資料流程在 DirectShow 中的運作方式。</span><span class="sxs-lookup"><span data-stu-id="02bed-104">This section gives a broad overview of how data flow works in DirectShow.</span></span> <span data-ttu-id="02bed-105">您可以在檔的其他章節中找到詳細資料。</span><span class="sxs-lookup"><span data-stu-id="02bed-105">Details can be found in other sections of the documentation.</span></span>

<span data-ttu-id="02bed-106">資料會保留在緩衝區中，這只是位元組的陣列。</span><span class="sxs-lookup"><span data-stu-id="02bed-106">Data is held in buffers, which are simply arrays of bytes.</span></span> <span data-ttu-id="02bed-107">每個緩衝區都是由稱為 *媒體範例* 的 COM 物件所包裝，它會執行 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面。</span><span class="sxs-lookup"><span data-stu-id="02bed-107">Each buffer is wrapped by a COM object called a *media sample*, which implements the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="02bed-108">範例是由另一種類型的物件所建立，稱為配置器，它會執行 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。</span><span class="sxs-lookup"><span data-stu-id="02bed-108">Samples are created by another type of object, called an allocator, which implements the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span> <span data-ttu-id="02bed-109">因為有兩個以上的 pin 連線可能共用相同的配置器，所以系統會為每個 pin 連接指派配置器。</span><span class="sxs-lookup"><span data-stu-id="02bed-109">An allocator is assigned for every pin connection, although two or more pin connections might share the same allocator.</span></span> <span data-ttu-id="02bed-110">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="02bed-110">The following image illustrates this process.</span></span>

![緩衝區、範例和配置器](images/dataflow.png)

<span data-ttu-id="02bed-112">每個配置器都會建立媒體範例的集區，並為每個範例配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="02bed-112">Each allocator creates a pool of media samples and allocates the buffers for each sample.</span></span> <span data-ttu-id="02bed-113">每當篩選需要填滿資料的緩衝區時，就會呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)向配置器要求範例。</span><span class="sxs-lookup"><span data-stu-id="02bed-113">Whenever a filter needs to fill a buffer with data, it requests a sample from the allocator by calling [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="02bed-114">如果配置器具有目前未由其他篩選使用的任何範例， **GetBuffer** 方法會立即傳回範例的指標。</span><span class="sxs-lookup"><span data-stu-id="02bed-114">If the allocator has any samples that are not currently in use by another filter, the **GetBuffer** method returns immediately with a pointer to the sample.</span></span> <span data-ttu-id="02bed-115">如果配置器的所有範例都在使用中，方法會封鎖，直到範例變成可用為止。</span><span class="sxs-lookup"><span data-stu-id="02bed-115">If all of the allocator's samples are in use, the method blocks until a sample becomes available.</span></span> <span data-ttu-id="02bed-116">當方法傳回範例時，篩選會將資料放入緩衝區、在範例上設定適當的旗標 (通常包括時間戳記) ，並傳遞範例下游。</span><span class="sxs-lookup"><span data-stu-id="02bed-116">When the method does return a sample, the filter puts data into the buffer, sets the appropriate flags on the sample (typically including a time stamp), and delivers the sample downstream.</span></span>

<span data-ttu-id="02bed-117">當轉譯器篩選器收到範例時，它會檢查時間戳記並保存到範例上，直到篩選圖形的參考時鐘指出應該呈現資料為止。</span><span class="sxs-lookup"><span data-stu-id="02bed-117">When a renderer filter receives a sample, it checks the time stamp and holds onto the sample until the filter graph's reference clock indicates that the data should be rendered.</span></span> <span data-ttu-id="02bed-118">在篩選轉譯資料之後，它會釋放範例。</span><span class="sxs-lookup"><span data-stu-id="02bed-118">After the filter renders the data, it releases the sample.</span></span> <span data-ttu-id="02bed-119">此範例不會回到配置器的範例集區，直到樣本的參考計數為零，這表示每個篩選都已釋放範例。</span><span class="sxs-lookup"><span data-stu-id="02bed-119">The sample does not go back into the allocator's pool of samples until the sample's reference count is zero, meaning that every filter has released the sample.</span></span> <span data-ttu-id="02bed-120">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="02bed-120">The following image illustrates this process.</span></span>

![以解碼等候可用媒體範例](images/dataflow2.png)

<span data-ttu-id="02bed-122">上游篩選器可能會在轉譯器之前執行，也就是，它可能會比轉譯器取用緩衝區更快地填滿緩衝區。</span><span class="sxs-lookup"><span data-stu-id="02bed-122">The upstream filter might run ahead of the renderer — that is, it might fill buffers faster than the renderer consumes them.</span></span> <span data-ttu-id="02bed-123">即使是這樣，範例也不會提早轉譯，因為轉譯器會保存每個範例，直到其呈現時間為止。</span><span class="sxs-lookup"><span data-stu-id="02bed-123">Even so, samples do not get rendered early, because the renderer holds each until its presentation time.</span></span> <span data-ttu-id="02bed-124">此外，上游篩選不會不慎覆寫緩衝區，因為 **GetSample** 只會傳回未使用的範例。</span><span class="sxs-lookup"><span data-stu-id="02bed-124">Moreover, the upstream filter will not overwrite buffers accidentally, because **GetSample** only returns samples that are not otherwise in use.</span></span> <span data-ttu-id="02bed-125">上游篩選器可以預先執行的數量取決於配置器集區中的樣本數。</span><span class="sxs-lookup"><span data-stu-id="02bed-125">The amount by which the upstream filter can run ahead is determined by the number of samples in the allocator's pool.</span></span>

<span data-ttu-id="02bed-126">上圖只會顯示一個配置器，但每個串流通常會有數個配置器。</span><span class="sxs-lookup"><span data-stu-id="02bed-126">The previous diagram only shows one allocator, but typically there are several allocators per stream.</span></span> <span data-ttu-id="02bed-127">因此，當轉譯器釋放範例時，它可能會有串聯效果。</span><span class="sxs-lookup"><span data-stu-id="02bed-127">Thus, when the renderer releases a sample, it can have a cascading effect.</span></span> <span data-ttu-id="02bed-128">下圖顯示在等候轉譯器釋放範例時，某個解碼器持有壓縮影片框架的情況。</span><span class="sxs-lookup"><span data-stu-id="02bed-128">The following diagram shows a situation where a decoder holds a compressed video frame while it waits for the renderer to release a sample.</span></span> <span data-ttu-id="02bed-129">剖析器篩選器也會等候解碼器釋放範例。</span><span class="sxs-lookup"><span data-stu-id="02bed-129">A parser filter is also waiting for the decoder to release a sample.</span></span>

![等候範例的兩個篩選](images/dataflow3.png)

<span data-ttu-id="02bed-131">當轉譯器釋放其範例時，會傳回 **GetBuffer** 的解碼器暫止呼叫。</span><span class="sxs-lookup"><span data-stu-id="02bed-131">When the renderer releases its sample, the decoder's pending call to **GetBuffer** returns.</span></span> <span data-ttu-id="02bed-132">然後，您可以將壓縮的影片框架解碼並釋出它所保留的範例，藉此解除封鎖剖析器的暫止 **GetBuffer** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="02bed-132">The decoder can then decode the compressed video frame and release the sample it was holding, thereby unblocking the parser's pending **GetBuffer** call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02bed-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="02bed-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02bed-134">篩選圖形中的資料流程</span><span class="sxs-lookup"><span data-stu-id="02bed-134">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



