---
description: 媒體來源事件
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: 媒體來源事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106976405"
---
# <a name="media-source-events"></a><span data-ttu-id="abac2-103">媒體來源事件</span><span class="sxs-lookup"><span data-stu-id="abac2-103">Media Source Events</span></span>

<span data-ttu-id="abac2-104">本主題列出媒體來源和媒體資料流程所傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="abac2-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="abac2-105">媒體來源也可以傳送此處未列出的自訂事件。</span><span class="sxs-lookup"><span data-stu-id="abac2-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="abac2-106">媒體來源事件</span><span class="sxs-lookup"><span data-stu-id="abac2-106">Media Source Events</span></span>



| <span data-ttu-id="abac2-107">事件</span><span class="sxs-lookup"><span data-stu-id="abac2-107">Event</span></span>                                                                      | <span data-ttu-id="abac2-108">描述</span><span class="sxs-lookup"><span data-stu-id="abac2-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abac2-109">MEEndOfPresentation 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="abac2-110">簡報結束。</span><span class="sxs-lookup"><span data-stu-id="abac2-110">The presentation ended.</span></span> <span data-ttu-id="abac2-111">簡報中的所有資料流程都已達到資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="abac2-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="abac2-112">MENewStream 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="abac2-113">已建立新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="abac2-113">A new stream was created.</span></span> <span data-ttu-id="abac2-114">事件包含資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="abac2-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="abac2-115">MESourceCharacteristicsChanged 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="abac2-116">來源的特性已變更。</span><span class="sxs-lookup"><span data-stu-id="abac2-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="abac2-117">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="abac2-118">MESourceMetadataChanged 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="abac2-119">來源的中繼資料已變更。</span><span class="sxs-lookup"><span data-stu-id="abac2-119">The source's metadata has changed.</span></span> <span data-ttu-id="abac2-120">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="abac2-121">MESourcePaused 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="abac2-122">來源已暫停。</span><span class="sxs-lookup"><span data-stu-id="abac2-122">The source was paused.</span></span> <span data-ttu-id="abac2-123">並非所有來源都支援暫停。</span><span class="sxs-lookup"><span data-stu-id="abac2-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="abac2-124">MESourceRateChanged 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="abac2-125">來源的播放率已變更。</span><span class="sxs-lookup"><span data-stu-id="abac2-125">The source's playback rate has changed.</span></span> <span data-ttu-id="abac2-126"> (選用;適用于來源是否支援速率控制。 ) </span><span class="sxs-lookup"><span data-stu-id="abac2-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="abac2-127">MESourceRateChangeRequested 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="abac2-128">來源正在要求新的播放速率。</span><span class="sxs-lookup"><span data-stu-id="abac2-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="abac2-129">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="abac2-130">MESourceSeeked 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="abac2-131">來源已 seeked。</span><span class="sxs-lookup"><span data-stu-id="abac2-131">The source was seeked.</span></span> <span data-ttu-id="abac2-132">並非所有來源都支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="abac2-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="abac2-133">MESourceStarted 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="abac2-134">來源已啟動。</span><span class="sxs-lookup"><span data-stu-id="abac2-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="abac2-135">MESourceStopped 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="abac2-136">來源已停止。</span><span class="sxs-lookup"><span data-stu-id="abac2-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="abac2-137">MEUpdatedStream 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="abac2-138">現有的資料流程已 seeked 或重新開機。</span><span class="sxs-lookup"><span data-stu-id="abac2-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="abac2-139">事件包含資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="abac2-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="abac2-140">媒體串流事件</span><span class="sxs-lookup"><span data-stu-id="abac2-140">Media Stream Events</span></span>



| <span data-ttu-id="abac2-141">事件</span><span class="sxs-lookup"><span data-stu-id="abac2-141">Event</span></span>                                                    | <span data-ttu-id="abac2-142">描述</span><span class="sxs-lookup"><span data-stu-id="abac2-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="abac2-143">MEEndOfStream 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="abac2-144">資料流程已結束。</span><span class="sxs-lookup"><span data-stu-id="abac2-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="abac2-145">MEError 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="abac2-146">串流期間發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="abac2-146">An error has occurred during streaming.</span></span> <span data-ttu-id="abac2-147">如果錯誤與此處所列的任何其他事件無關，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="abac2-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="abac2-148">MEMediaSample 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="abac2-149">資料流程已產生新的範例。</span><span class="sxs-lookup"><span data-stu-id="abac2-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="abac2-150">MEStreamFormatChanged 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="abac2-151">媒體類型已變更。</span><span class="sxs-lookup"><span data-stu-id="abac2-151">The media type has changed.</span></span> <span data-ttu-id="abac2-152">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="abac2-153">MEStreamPaused 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="abac2-154">資料流程已暫停。</span><span class="sxs-lookup"><span data-stu-id="abac2-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="abac2-155">MEStreamSeeked 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="abac2-156">資料流程已 seeked。</span><span class="sxs-lookup"><span data-stu-id="abac2-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="abac2-157">MEStreamStarted 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="abac2-158">資料流程已啟動。</span><span class="sxs-lookup"><span data-stu-id="abac2-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="abac2-159">MEStreamStopped 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="abac2-160">資料流程已停止。</span><span class="sxs-lookup"><span data-stu-id="abac2-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="abac2-161">MEStreamThinMode 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="abac2-162">Thinning 模式已啟動或停止。</span><span class="sxs-lookup"><span data-stu-id="abac2-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="abac2-163">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="abac2-164">MEStreamTick 事件</span><span class="sxs-lookup"><span data-stu-id="abac2-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="abac2-165">資料流程中有一個間距。</span><span class="sxs-lookup"><span data-stu-id="abac2-165">There is a gap in the stream.</span></span> <span data-ttu-id="abac2-166">(選擇性。)</span><span class="sxs-lookup"><span data-stu-id="abac2-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="abac2-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="abac2-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abac2-168">媒體來源</span><span class="sxs-lookup"><span data-stu-id="abac2-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



