---
description: CVideoTransformFilter 類別主要是用來做為 AVI 解壓縮程式篩選準則的基類。
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846815"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="21926-103">CVideoTransformFilter 類別</span><span class="sxs-lookup"><span data-stu-id="21926-103">CVideoTransformFilter class</span></span>

![cvideotransformfilter 類別階層](images/vtsip01.png)

<span data-ttu-id="21926-105">`CVideoTransformFilter`類別主要是用來做為 AVI 解壓縮程式篩選準則的基類。</span><span class="sxs-lookup"><span data-stu-id="21926-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="21926-106">此類別會將品質控制的支援新增至 [**CTransformFilter**](ctransformfilter.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="21926-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="21926-107">篩選器的 **Receive** 方法可以決定要根據轉譯器中的品質訊息和篩選器在串流處理時所收集的效能測量，來卸載畫面格。</span><span class="sxs-lookup"><span data-stu-id="21926-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="21926-108">如果篩選器卸載框架，則會繼續卸載框架，直到到達下一個主要畫面格為止。</span><span class="sxs-lookup"><span data-stu-id="21926-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="21926-109">針對 MPEG 資料流程，篩選不會區分 B 框架和 P 框架。</span><span class="sxs-lookup"><span data-stu-id="21926-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="21926-110">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="21926-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="21926-111">Description</span><span class="sxs-lookup"><span data-stu-id="21926-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21926-112">**m \_ bQualityChanged**</span><span class="sxs-lookup"><span data-stu-id="21926-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="21926-113">指出篩選是否已卸載框架。</span><span class="sxs-lookup"><span data-stu-id="21926-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="21926-114">**m \_ bSkipping**</span><span class="sxs-lookup"><span data-stu-id="21926-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="21926-115">指出篩選目前是否正在卸載框架。</span><span class="sxs-lookup"><span data-stu-id="21926-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="21926-116">**m \_ itrAvgDecode**</span><span class="sxs-lookup"><span data-stu-id="21926-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="21926-117">用來解碼框架的平均時間長度。</span><span class="sxs-lookup"><span data-stu-id="21926-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="21926-118">**m \_ itrLate**</span><span class="sxs-lookup"><span data-stu-id="21926-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="21926-119">表示樣本到達轉譯器的延遲。</span><span class="sxs-lookup"><span data-stu-id="21926-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="21926-120">**m \_ nFramesSinceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="21926-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="21926-121">自最後一個主要畫面格之後，篩選所收到的框架數目。</span><span class="sxs-lookup"><span data-stu-id="21926-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="21926-122">**m \_ nKeyFramePeriod**</span><span class="sxs-lookup"><span data-stu-id="21926-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="21926-123">主要畫面格之間的最大觀察間隔。</span><span class="sxs-lookup"><span data-stu-id="21926-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="21926-124">**m \_ nWaitForKey**</span><span class="sxs-lookup"><span data-stu-id="21926-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="21926-125">要卸載之 delta 框架的目前最大數目。</span><span class="sxs-lookup"><span data-stu-id="21926-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="21926-126">**m \_ tDecodeStart**</span><span class="sxs-lookup"><span data-stu-id="21926-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="21926-127">解碼最新範例所花費的時間長度。</span><span class="sxs-lookup"><span data-stu-id="21926-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="21926-128">保護方法</span><span class="sxs-lookup"><span data-stu-id="21926-128">Protected Methods</span></span>                                                               | <span data-ttu-id="21926-129">Description</span><span class="sxs-lookup"><span data-stu-id="21926-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="21926-130">**AbortPlayback**</span><span class="sxs-lookup"><span data-stu-id="21926-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="21926-131">用來發出串流錯誤的信號。</span><span class="sxs-lookup"><span data-stu-id="21926-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="21926-132">**AlterQuality**</span><span class="sxs-lookup"><span data-stu-id="21926-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="21926-133">通知篩選準則要求品質變更。</span><span class="sxs-lookup"><span data-stu-id="21926-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="21926-134">**收到**</span><span class="sxs-lookup"><span data-stu-id="21926-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="21926-135">接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。</span><span class="sxs-lookup"><span data-stu-id="21926-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="21926-136">**ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="21926-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="21926-137">判斷篩選是否應卸載指定的範例。</span><span class="sxs-lookup"><span data-stu-id="21926-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="21926-138">**StartStreaming**</span><span class="sxs-lookup"><span data-stu-id="21926-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="21926-139">當篩選參數切換為暫停狀態時呼叫。</span><span class="sxs-lookup"><span data-stu-id="21926-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="21926-140">公用方法</span><span class="sxs-lookup"><span data-stu-id="21926-140">Public Methods</span></span>                                                                  | <span data-ttu-id="21926-141">Description</span><span class="sxs-lookup"><span data-stu-id="21926-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="21926-142">**CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="21926-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="21926-143">函式方法。</span><span class="sxs-lookup"><span data-stu-id="21926-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="21926-144">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="21926-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="21926-145">結束清除操作。</span><span class="sxs-lookup"><span data-stu-id="21926-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



