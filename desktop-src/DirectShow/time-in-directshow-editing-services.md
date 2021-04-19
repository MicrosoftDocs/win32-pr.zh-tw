---
description: DirectShow 編輯服務中的時間
ms.assetid: 4e8cc766-97f3-45d5-9c4a-5cd6e9ad9c09
title: DirectShow 編輯服務中的時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421831742a2805f58d61c2258dad89d339131f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992602"
---
# <a name="time-in-directshow-editing-services"></a><span data-ttu-id="23d77-103">DirectShow 編輯服務中的時間</span><span class="sxs-lookup"><span data-stu-id="23d77-103">Time in DirectShow Editing Services</span></span>

<span data-ttu-id="23d77-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="23d77-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="23d77-105">若要編輯影片，您必須使用一些重要的時間概念。</span><span class="sxs-lookup"><span data-stu-id="23d77-105">To edit video, you must work with some important timing concepts.</span></span> <span data-ttu-id="23d77-106">例如：</span><span class="sxs-lookup"><span data-stu-id="23d77-106">For example:</span></span>

-   <span data-ttu-id="23d77-107">每個剪輯都有持續時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-107">Each clip has a duration.</span></span>
-   <span data-ttu-id="23d77-108">剪輯、轉換和效果都會出現在專案的特定時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-108">Clips, transitions, and effects appear at certain times in a project.</span></span>
-   <span data-ttu-id="23d77-109">影片具有畫面播放速率，以每秒的畫面格 (fps) 來表示。</span><span class="sxs-lookup"><span data-stu-id="23d77-109">Video has a frame rate, expressed in frames per second (fps).</span></span>

<span data-ttu-id="23d77-110"> (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)提供各種可設定或抓取時間和畫面播放速率的方法。</span><span class="sxs-lookup"><span data-stu-id="23d77-110">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides various methods that set or retrieve times and frame rates.</span></span> <span data-ttu-id="23d77-111">這些值的意義取決於內容。</span><span class="sxs-lookup"><span data-stu-id="23d77-111">The meaning of these values depends on the context.</span></span>

<span data-ttu-id="23d77-112">**時間值**</span><span class="sxs-lookup"><span data-stu-id="23d77-112">**Time Values**</span></span>

<span data-ttu-id="23d77-113">當參數表示時間時，有三種不同意義：</span><span class="sxs-lookup"><span data-stu-id="23d77-113">When a parameter expresses a time, three distinct meanings are possible:</span></span>

-   <span data-ttu-id="23d77-114">時間 *軸時間*：相對於時間軸開始的時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-114">*Timeline time*: The time relative to the beginning of the timeline.</span></span> <span data-ttu-id="23d77-115">例如，剪輯可能會在時間軸中開始2秒，或在時間軸中有15秒的轉換。</span><span class="sxs-lookup"><span data-stu-id="23d77-115">For example, a clip might start 2 seconds into the timeline, or a transition might occur 15 seconds into the timeline.</span></span> <span data-ttu-id="23d77-116">時間軸會判斷最終呈現的專案，因此您也可以將時間軸時間視為「專案時間」。</span><span class="sxs-lookup"><span data-stu-id="23d77-116">The timeline determines the final rendered project, so you can also think of timeline time as "project time."</span></span>
-   <span data-ttu-id="23d77-117">*媒體時間*：相對於檔案開頭的原始程式檔中的點，如同正常播放期間所達到的位置。</span><span class="sxs-lookup"><span data-stu-id="23d77-117">*Media time*: A point in a source file relative to the start of the file, as reached during normal playback.</span></span> <span data-ttu-id="23d77-118">例如，如果您有10秒的影片檔案，則檔案中間的點會出現在5秒（以媒體時程表示）。</span><span class="sxs-lookup"><span data-stu-id="23d77-118">For example, if you have a 10-second video file, the point midway through the file occurs at 5 seconds, expressed as a media time.</span></span>
-   <span data-ttu-id="23d77-119">*Parent time*：相對於時間軸中物件的時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-119">*Parent time*: Time relative to an object in the timeline.</span></span> <span data-ttu-id="23d77-120">例如，如果物件在時間軸上的8秒開始，且包含另一個在時間軸上從10秒開始的物件，則子物件會從相對於父系的2秒開始。</span><span class="sxs-lookup"><span data-stu-id="23d77-120">For example, if an object starts at 8 seconds on the timeline and contains another object that starts at 10 seconds on the timeline, the child object starts at 2 seconds relative to the parent.</span></span> <span data-ttu-id="23d77-121">相對於時程表，虛擬追蹤的所有時間都是以零為起始。</span><span class="sxs-lookup"><span data-stu-id="23d77-121">Virtual tracks all start at time zero, relative to the timeline.</span></span> <span data-ttu-id="23d77-122">因此針對虛擬軌中的任何物件，父時間等於時間軸時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-122">So for any object in a virtual track, parent time equals timeline time.</span></span>

<span data-ttu-id="23d77-123">媒體時間僅適用于來源物件。</span><span class="sxs-lookup"><span data-stu-id="23d77-123">Media time applies only to source objects.</span></span> <span data-ttu-id="23d77-124">每個來源物件都有媒體開始時間和媒體停止時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-124">Each source object has a media start time and a media stop time.</span></span> <span data-ttu-id="23d77-125">例如，假設您有10秒的影片剪輯，而且您只想要從剪輯中間使用5秒鐘，請從剪輯中修剪前2秒和最後3秒。</span><span class="sxs-lookup"><span data-stu-id="23d77-125">For example, suppose you have a 10-second video clip, and you want to use only 5 seconds from the middle of the clip, trimming the first 2 seconds and the last 3 seconds from the clip.</span></span> <span data-ttu-id="23d77-126">如果您想要讓剪輯在專案中顯示20秒 (並且假設正常播放速率) 您會指定下列開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-126">If you want the clip to appear 20 seconds into the project (and assuming a normal playback rate) you would specify the following start and stop times.</span></span>

-   <span data-ttu-id="23d77-127">媒體啟動：2秒</span><span class="sxs-lookup"><span data-stu-id="23d77-127">Media start: 2 seconds</span></span>
-   <span data-ttu-id="23d77-128">媒體停止：7秒</span><span class="sxs-lookup"><span data-stu-id="23d77-128">Media stop: 7 seconds</span></span>
-   <span data-ttu-id="23d77-129">時間軸開始：20秒</span><span class="sxs-lookup"><span data-stu-id="23d77-129">Timeline start: 20 seconds</span></span>
-   <span data-ttu-id="23d77-130">時間軸停止：25秒</span><span class="sxs-lookup"><span data-stu-id="23d77-130">Timeline stop: 25 seconds</span></span>

    ![在時間軸上插入來源剪輯](images/des-time1.png)

<span data-ttu-id="23d77-132">**畫面播放速率**</span><span class="sxs-lookup"><span data-stu-id="23d77-132">**Frame Rates**</span></span>

<span data-ttu-id="23d77-133">畫面播放速率是媒體資料流程的「速度」，以每秒的畫面格數來測量。</span><span class="sxs-lookup"><span data-stu-id="23d77-133">Frame rate is the "speed" of a media stream, measured in frames per second.</span></span> <span data-ttu-id="23d77-134">如同時間值，畫面播放速率的意義取決於內容：</span><span class="sxs-lookup"><span data-stu-id="23d77-134">As with time values, the meaning of a frame rate depends on the context:</span></span>

-   <span data-ttu-id="23d77-135">**輸出畫面播放速率：** 由群組定義之最終轉譯專案的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-135">**Output frame rate:** The frame rate of the final rendered project, defined by the group.</span></span> <span data-ttu-id="23d77-136">當您轉譯專案時，每個群組都會變成個別的媒體資料流程及其本身的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-136">When you render the project, each group becomes a separate media stream with its own frame rate.</span></span>
-   <span data-ttu-id="23d77-137">**來源畫面播放速率：** 原始程式檔最初撰寫的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-137">**Source frame rate:** The frame rate in which the source file was originally authored.</span></span> <span data-ttu-id="23d77-138">撰寫的畫面播放速率不需要與群組的輸出畫面播放速率相符。</span><span class="sxs-lookup"><span data-stu-id="23d77-138">The authored frame rate does not have to match the group's output frame rate.</span></span> <span data-ttu-id="23d77-139">DES 會視需要自動 upsample 或縮減檔案。</span><span class="sxs-lookup"><span data-stu-id="23d77-139">DES will automatically upsample or downsample the file as needed.</span></span> <span data-ttu-id="23d77-140">針對大部分的媒體格式，DES 可以檢查格式來判斷畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-140">For most media formats, DES can determine the frame rate by examining the format.</span></span> <span data-ttu-id="23d77-141">DIB 順序是例外狀況;您必須指定 DIB 順序的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-141">A DIB sequence is an exception; you must specify the frame rate of a DIB sequence.</span></span> <span data-ttu-id="23d77-142"> (需詳細資訊，請參閱 [使用來源](working-with-sources.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="23d77-142">(For more information, see [Working with Sources](working-with-sources.md).)</span></span>

<span data-ttu-id="23d77-143">**播放速率：** 來源剪輯出現在專案中的明顯速度。</span><span class="sxs-lookup"><span data-stu-id="23d77-143">**Playback rate:** The apparent speed of a source clip when it appears in the project.</span></span> <span data-ttu-id="23d77-144">例如，10秒的影片可容納在時間軸上的5秒。</span><span class="sxs-lookup"><span data-stu-id="23d77-144">For example, 10 seconds' of video can be fit into 5 seconds on the timeline.</span></span> <span data-ttu-id="23d77-145">如此一來，剪輯的速度會以2的因數增加，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="23d77-145">As a result, the speed of the clip increases by a factor of 2, as the following diagram illustrates.</span></span>

![讓來源播放更快](images/des-time2.png)

<span data-ttu-id="23d77-147"> (使用音訊來源時，音調也會移動。 ) 下列公式會決定來源剪輯的播放速率：</span><span class="sxs-lookup"><span data-stu-id="23d77-147">(With an audio source, the pitch would shift as well.) The following formula determines a source clip's playback rate:</span></span>

-   <span data-ttu-id="23d77-148">播放速率 = (媒體停止-媒體啟動) / (時間軸停止–時程表開始) </span><span class="sxs-lookup"><span data-stu-id="23d77-148">Playback rate = (Media Stop – Media Start) / (Timeline Stop – Timeline Start)</span></span>

<span data-ttu-id="23d77-149">請注意，這三個費率與其他費率無關：</span><span class="sxs-lookup"><span data-stu-id="23d77-149">Note that each of these three rates is independent of the others:</span></span>

-   <span data-ttu-id="23d77-150">您可以藉由調整媒體時間來加速或減緩剪輯的速度;這不會影響最終輸出的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-150">You can speed up or slow down a clip by adjusting the media times; this does not affect the frame rate of the final output.</span></span>
-   <span data-ttu-id="23d77-151">您可以增加或減少輸出畫面播放速率，而不會影響檔案播放的速度。</span><span class="sxs-lookup"><span data-stu-id="23d77-151">You can increase or decrease the output frame rate without affecting how fast a file plays.</span></span>
-   <span data-ttu-id="23d77-152">您可以在同一個群組中混用具有不同編寫畫面播放速率的原始程式檔，而 DES 將會 upsample 或縮減每個剪輯，以符合群組的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="23d77-152">You can mix, within the same group, source files that have different authored frame rates, and DES will upsample or downsample each clip to match the group's frame rate.</span></span>

<span data-ttu-id="23d77-153">當您轉譯專案時，會將所有時間四捨五入到最接近的框架界限（由群組畫面播放速率判斷）。</span><span class="sxs-lookup"><span data-stu-id="23d77-153">When you render a project, all times are rounded to the nearest frame boundary, as determined by the group frame rate.</span></span> <span data-ttu-id="23d77-154">例如，假設某個影片群組的畫面播放速率為 30 fps。</span><span class="sxs-lookup"><span data-stu-id="23d77-154">For example, suppose a video group has a frame rate of 30 fps.</span></span> <span data-ttu-id="23d77-155">每個框架大約是33毫秒 (ms) 。</span><span class="sxs-lookup"><span data-stu-id="23d77-155">Each frame is roughly 33 milliseconds (ms).</span></span> <span data-ttu-id="23d77-156">假設您將1.68 秒的來源剪輯新增至時間軸，從零開始。</span><span class="sxs-lookup"><span data-stu-id="23d77-156">Suppose you add a 1.68-second source clip to the timeline, starting at time zero.</span></span> <span data-ttu-id="23d77-157">來源不會完全以框架界限結束，因此 DES 會將停止時間四捨五入至1.6666 秒 (50 畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="23d77-157">The source does not end exactly on a frame boundary, so DES rounds the stop time to 1.6666 seconds (50 frames).</span></span> <span data-ttu-id="23d77-158">如果您在轉譯的專案中搜尋至1.68 秒，您實際上會在第51個畫面格的結尾處尋找超過來源的結尾。</span><span class="sxs-lookup"><span data-stu-id="23d77-158">If you seek to 1.68 seconds in the rendered project, you will actually seek past the end of the source, to the 51st frame.</span></span>

<span data-ttu-id="23d77-159">不過，DES 不會覆寫來源的停止時間。</span><span class="sxs-lookup"><span data-stu-id="23d77-159">However, DES does not overwrite the source's stop time.</span></span> <span data-ttu-id="23d77-160">您稍後可能會變更群組框架速率，或將來源移至時間軸中以不同方式四捨五入的新位置。</span><span class="sxs-lookup"><span data-stu-id="23d77-160">You might later change the group frame rate, or move the source to a new spot in the timeline where it rounds differently.</span></span> <span data-ttu-id="23d77-161">因此，DES 會保留原始的停止時間，而且只會在必要時進行四捨五入。</span><span class="sxs-lookup"><span data-stu-id="23d77-161">Therefore, DES preserves the original stop time and rounds only when necessary.</span></span> <span data-ttu-id="23d77-162">如需詳細資訊，請參閱 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md)。</span><span class="sxs-lookup"><span data-stu-id="23d77-162">For more information, see [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23d77-163">相關主題</span><span class="sxs-lookup"><span data-stu-id="23d77-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23d77-164">使用 DirectShow 編輯服務開始使用</span><span class="sxs-lookup"><span data-stu-id="23d77-164">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



