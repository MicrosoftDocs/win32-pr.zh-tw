---
description: 本主題描述 Sequencer 來源如何處理播放期間的呈現時間。
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: 順序呈現時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17f5b0ff4bd6f0cfee2b1b461d6fbd11bdbf0fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512552"
---
# <a name="sequence-presentation-times"></a><span data-ttu-id="988a4-103">順序呈現時間</span><span class="sxs-lookup"><span data-stu-id="988a4-103">Sequence Presentation Times</span></span>

<span data-ttu-id="988a4-104">本主題描述 [Sequencer 來源](sequencer-source.md) 如何處理播放期間的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-104">This topic describes how the [Sequencer Source](sequencer-source.md) handles presentation times during playback.</span></span>

## <a name="overview"></a><span data-ttu-id="988a4-105">概觀</span><span class="sxs-lookup"><span data-stu-id="988a4-105">Overview</span></span>

<span data-ttu-id="988a4-106">Sequencer 來源支援兩種不同的模式：播放清單順序和編輯順序。</span><span class="sxs-lookup"><span data-stu-id="988a4-106">The sequencer source supports two different modes: playlist sequences and editing sequences.</span></span>

<span data-ttu-id="988a4-107">在編輯順序中，應用程式會在開始播放之前，事先指定每個區段的持續時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-107">In an editing sequence, the application specifies the duration of each segment in advance, before starting playback.</span></span> <span data-ttu-id="988a4-108">在播放清單順序中，應用程式不會事先指定持續時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-108">In a playlist sequence, the application does not specify the duration in advance.</span></span> <span data-ttu-id="988a4-109"> (事實上，可能不知道持續時間。 ) </span><span class="sxs-lookup"><span data-stu-id="988a4-109">(In fact, the duration might not be known.)</span></span>

<span data-ttu-id="988a4-110">在這兩種情況下，您都可以指定區段的媒體開始和媒體停止時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-110">In both cases, you can specify a segment's media start and media stop time.</span></span> <span data-ttu-id="988a4-111">這些時間會指定來源檔案中區段開始和結束的位置。</span><span class="sxs-lookup"><span data-stu-id="988a4-111">These times specify the position in the source file where the segment begins and ends.</span></span> <span data-ttu-id="988a4-112">例如，假設原始程式檔的長度是90秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-112">For example, suppose that the source file is 90 seconds long.</span></span> <span data-ttu-id="988a4-113">如果您想要修剪前10秒和最後10秒，您需要指定下列值：</span><span class="sxs-lookup"><span data-stu-id="988a4-113">If you wanted to trim the first 10 seconds and the last 10 seconds, you would specify the following values:</span></span>

-   <span data-ttu-id="988a4-114">媒體啟動：10秒</span><span class="sxs-lookup"><span data-stu-id="988a4-114">Media start: 10 seconds</span></span>
-   <span data-ttu-id="988a4-115">媒體停止：80秒</span><span class="sxs-lookup"><span data-stu-id="988a4-115">Media stop: 80 seconds</span></span>

<span data-ttu-id="988a4-116">若要指定媒體開始時間，請在來源節點上設定 [ [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="988a4-116">To specify the media start time, set the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute on the source node.</span></span> <span data-ttu-id="988a4-117">若要指定媒體停止時間，請在來源節點上設定 [ [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="988a4-117">To specify the media stop time, set the [MF\_TOPONODE\_MEDIASTOP](mf-toponode-mediastop-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="988a4-118">若要建立編輯順序，請在建立媒體會話時設定 [ [MF \_ 會話 \_ 全域 \_ 時間](mf-session-global-time-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="988a4-118">To create an editing sequence, set the [MF\_SESSION\_GLOBAL\_TIME](mf-session-global-time-attribute.md) attribute when you create the Media Session.</span></span> <span data-ttu-id="988a4-119">否則，媒體會話會預期播放清單順序。</span><span class="sxs-lookup"><span data-stu-id="988a4-119">Otherwise, the Media Session expects playlist sequences.</span></span> <span data-ttu-id="988a4-120">在編輯順序中，每個區段拓撲都必須有 [mf \_ 拓撲 \_ PROJECTSTART](mf-topology-projectstart-attribute.md) 屬性和 [mf \_ 拓撲 \_ PROJECTSTOP](mf-topology-projectstop-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="988a4-120">In an editing sequence, every segment topology must have the [MF\_TOPOLOGY\_PROJECTSTART](mf-topology-projectstart-attribute.md) attribute and the [MF\_TOPOLOGY\_PROJECTSTOP](mf-topology-projectstop-attribute.md) attribute.</span></span>

## <a name="playlist-sequences"></a><span data-ttu-id="988a4-121">播放清單順序</span><span class="sxs-lookup"><span data-stu-id="988a4-121">Playlist Sequences</span></span>

<span data-ttu-id="988a4-122">在播放清單順序中，標記法會從零開始，並在區段界限之間繼續。</span><span class="sxs-lookup"><span data-stu-id="988a4-122">In a playlist sequence, the presentation clock starts at zero and continues across segment boundaries.</span></span> <span data-ttu-id="988a4-123">原生來源會提供時間戳記等於媒體時間的範例。</span><span class="sxs-lookup"><span data-stu-id="988a4-123">The native sources deliver samples with time stamps equal to the media time.</span></span> <span data-ttu-id="988a4-124">管線會將時間戳記轉換為正確的呈現時間，如下所示：</span><span class="sxs-lookup"><span data-stu-id="988a4-124">The pipeline converts the time stamps to the correct presentation time as follows:</span></span>

-   <span data-ttu-id="988a4-125">新的時間戳記 = 媒體時間 + 位移−媒體開始</span><span class="sxs-lookup"><span data-stu-id="988a4-125">New time stamp = media time + offset − media start</span></span>

<span data-ttu-id="988a4-126">*Offset* 的值是前一個區段結束的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-126">The value of *offset* is the presentation time at which the previous segment ended.</span></span> <span data-ttu-id="988a4-127">若為第一個區段，則位移為零。</span><span class="sxs-lookup"><span data-stu-id="988a4-127">For the first segment, the offset is zero.</span></span> <span data-ttu-id="988a4-128">以下是計算這些時間戳記轉換的兩個範例：</span><span class="sxs-lookup"><span data-stu-id="988a4-128">Here are two examples of how these time-stamp conversions are calculated:</span></span>

-   <span data-ttu-id="988a4-129">範例1：假設第一個區段 (S1) 的長度為10秒，而第二個區段 (S2) 具有媒體開始時間為零。</span><span class="sxs-lookup"><span data-stu-id="988a4-129">Example 1: Suppose the first segment (S1) is 10 seconds long, and the second segment (S2) has a media start time of zero.</span></span> <span data-ttu-id="988a4-130">原生來源使用媒體時間作為時間戳記，因此 S2 的第一個範例的時間戳記為零。</span><span class="sxs-lookup"><span data-stu-id="988a4-130">The native source uses the media time for its time stamps, so the first sample from S2 has a time stamp of zero.</span></span> <span data-ttu-id="988a4-131">位移是 (S1) 的持續時間為10秒，因此調整的時間戳記為： 0 + 10 − 0 = 10 秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-131">The offset is 10 seconds (the duration of S1), so the adjusted time stamp is:0 + 10 − 0 = 10 seconds.</span></span>
-   <span data-ttu-id="988a4-132">範例2：假設區段 S1 的長度為10秒，而 S2 的媒體開始時間為5秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-132">Example 2: Suppose segment S1 is 10 seconds long, and S2 has a media start time of 5 seconds.</span></span> <span data-ttu-id="988a4-133">S2 的第一個範例有5秒的時間戳記 (媒體時間) 。</span><span class="sxs-lookup"><span data-stu-id="988a4-133">The first sample from S2 has a time stamp of 5 seconds (media time).</span></span> <span data-ttu-id="988a4-134">位移為10秒，因此調整的時間戳記為： 5 + 10 − 5 = 10 秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-134">The offset is 10 seconds, so the adjusted time stamp is:5 + 10 − 5 = 10 seconds.</span></span>

<span data-ttu-id="988a4-135">來源節點下游的所有管線元件都會收到範例，其中包含已調整的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="988a4-135">All pipeline components downstream from the source nodes receive samples with the adjusted time stamps.</span></span> <span data-ttu-id="988a4-136">拓撲中的來源節點可能會有不同的媒體開始時間，因此會針對拓撲的每個分支分別計算其調整。</span><span class="sxs-lookup"><span data-stu-id="988a4-136">The source nodes in a topology can have different media start times, so the adjustments are calculated separately for each branch of the topology.</span></span>

<span data-ttu-id="988a4-137">當簡報切換至下一個區段時，標記法的時鐘不會停止或重設，而且呈現時間會以單純方式遞增。</span><span class="sxs-lookup"><span data-stu-id="988a4-137">When the presentation switches to the next segment, the presentation clock does not stop or reset, and the presentation time increases monotonically.</span></span> <span data-ttu-id="988a4-138">在新的區段開始之前，媒體會話會將 [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) 事件傳送給應用程式。</span><span class="sxs-lookup"><span data-stu-id="988a4-138">Before a new segment starts, the Media Session sends the application an [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) event.</span></span> <span data-ttu-id="988a4-139">事件會指定區段的開始時間（相對於呈現時鐘）和位移的值。</span><span class="sxs-lookup"><span data-stu-id="988a4-139">The event specifies the starting time of the segment, relative to the presentation clock, and the value of the offset.</span></span> <span data-ttu-id="988a4-140">當新的區段開始時，管線會[](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫以 VT 空白值的 Sequencer 來源開始 \_ 。</span><span class="sxs-lookup"><span data-stu-id="988a4-140">When a new segment starts, the pipeline calls [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) on the sequencer source with the value VT\_EMPTY.</span></span> <span data-ttu-id="988a4-141">Sequencer 來源傳送的 [MESourceStarted](mesourcestarted.md) 事件沒有開始時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-141">The sequencer source sends an [MESourceStarted](mesourcestarted.md) event with no start time.</span></span>

<span data-ttu-id="988a4-142">若要搜尋，應用程式會指定區段識別碼加上區段內的時間位移。</span><span class="sxs-lookup"><span data-stu-id="988a4-142">To seek, the application specifies a segment identifier plus a time offset within the segment.</span></span> <span data-ttu-id="988a4-143">搜尋之後，簡報時鐘就會從 *區段* 位移開始。</span><span class="sxs-lookup"><span data-stu-id="988a4-143">After the seek, the presentation clock starts at the *segment* offset.</span></span> <span data-ttu-id="988a4-144">以下是該程式如何運作的範例：</span><span class="sxs-lookup"><span data-stu-id="988a4-144">Here is an example of how that process works:</span></span>

-   <span data-ttu-id="988a4-145">範例3：應用程式會搜尋分割 S3，其區段位移為10秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-145">Example 3: The application seeks to segment S3, with a segment offset of 10 seconds.</span></span> <span data-ttu-id="988a4-146">簡報時鐘的開始時間為10秒， (區段位移) 。</span><span class="sxs-lookup"><span data-stu-id="988a4-146">The presentation clock starts at 10 seconds (the segment offset).</span></span> <span data-ttu-id="988a4-147">位移不包含區段 S1 和 S2 的持續時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-147">The offset does not include the duration of segments S1 and S2.</span></span> <span data-ttu-id="988a4-148">Sequencer 來源傳送的 [MESourceStarted](mesourcestarted.md) 事件，其開始時間等於區段位移10秒。</span><span class="sxs-lookup"><span data-stu-id="988a4-148">The sequencer source sends an [MESourceStarted](mesourcestarted.md) event with a start time equal to the segment offset, 10 seconds.</span></span>

<span data-ttu-id="988a4-149">搜尋之後，如果播放繼續前往下一個區段，則轉換的運作方式就如同先前的範例，差別在於位移不包含略過的區段。</span><span class="sxs-lookup"><span data-stu-id="988a4-149">After a seek, if playback continues to the next segment, the transition works just like the previous examples, except that the offset does not include the skipped segments.</span></span>

<span data-ttu-id="988a4-150">以下是一些進一步的詳細資料，會影響取樣的時間戳記：</span><span class="sxs-lookup"><span data-stu-id="988a4-150">Here are some further details that affect how samples are time stamped:</span></span>

-   <span data-ttu-id="988a4-151">您可能需要在媒體停止時間以外的時間進行的資料。</span><span class="sxs-lookup"><span data-stu-id="988a4-151">Decoders may need data beyond the media stop time.</span></span> <span data-ttu-id="988a4-152">管線會從來源提取所需的資料量，然後修剪該解碼器的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="988a4-152">The pipeline pulls as much data from the source as the decoder requires, and then trims the decoder's output samples.</span></span>
-   <span data-ttu-id="988a4-153">轉換可能會緩衝資料。</span><span class="sxs-lookup"><span data-stu-id="988a4-153">Transforms might buffer data.</span></span> <span data-ttu-id="988a4-154">例如，音訊效果可能需要這樣做。</span><span class="sxs-lookup"><span data-stu-id="988a4-154">For example, an audio effect might need to do this.</span></span> <span data-ttu-id="988a4-155">當區段結束時，轉換的最後一個樣本上的時間戳記會早于區段的結尾，因為轉換會保留一些資料。</span><span class="sxs-lookup"><span data-stu-id="988a4-155">When a segment ends, the time stamp on the last sample from the transform is earlier than the end of the segment, because the transform is holding back some data.</span></span> <span data-ttu-id="988a4-156">當下一個區段開始時，第一個樣本上的時間戳記會稍微早于區段的起點。</span><span class="sxs-lookup"><span data-stu-id="988a4-156">When the next segment starts, the time stamp on the first sample is slightly earlier than the start of the segment.</span></span> <span data-ttu-id="988a4-157">時間戳記中沒有間距，所以到達媒體接收器的資料是連續的。</span><span class="sxs-lookup"><span data-stu-id="988a4-157">There is no gap in the time stamps, so the data that reaches the media sink is continuous.</span></span> <span data-ttu-id="988a4-158">當最後一個區段結束時，管線會清空轉換，因此不會遺失任何資料。</span><span class="sxs-lookup"><span data-stu-id="988a4-158">When the final segment ends, the pipeline drains the transform, so no data is lost.</span></span>
-   <span data-ttu-id="988a4-159">來源可能必須稍微早于媒體開始時間，才能挑選先前的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="988a4-159">The source may need to start slightly earlier than the media start time, to pick up the previous key frame.</span></span> <span data-ttu-id="988a4-160">因此，在調整之後，第一個範例可能會有負面的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="988a4-160">Therefore, after the adjustment, the first sample might have a negative presentation time.</span></span>

## <a name="editing-sequences"></a><span data-ttu-id="988a4-161">編輯順序</span><span class="sxs-lookup"><span data-stu-id="988a4-161">Editing Sequences</span></span>

<span data-ttu-id="988a4-162">在編輯順序中，應用程式會藉由設定 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 和 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性，預先指定區段界限。</span><span class="sxs-lookup"><span data-stu-id="988a4-162">In an editing sequence, the application specifies the segment boundaries in advance, by setting the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="988a4-163">管線會計算時間戳記的調整，與播放清單順序的方式幾乎相同：</span><span class="sxs-lookup"><span data-stu-id="988a4-163">The pipeline calculates adjustments for the time stamps in almost the same way as for a playlist sequence:</span></span>

-   <span data-ttu-id="988a4-164">針對位移，它會使用 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)的值，而不是使用區段觀察到的結尾。</span><span class="sxs-lookup"><span data-stu-id="988a4-164">For the offset, it uses the value of [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md), instead of using the observed end of the segment.</span></span>

-   <span data-ttu-id="988a4-165">針對搜尋，位移會使用等於區段的 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 值加上區段位移的值。</span><span class="sxs-lookup"><span data-stu-id="988a4-165">For seeking, the offset uses a value equal to the segment's [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) value plus the segment offset.</span></span>

<span data-ttu-id="988a4-166">因此，即使應用程式搜尋至另一個區段，編輯順序中的呈現時間一律會相對於簡報的開頭。</span><span class="sxs-lookup"><span data-stu-id="988a4-166">Therefore, the presentation time in an editing sequence is always relative to the start of the presentation, even if the application seeks to another segment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="988a4-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="988a4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="988a4-168">媒體會話</span><span class="sxs-lookup"><span data-stu-id="988a4-168">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="988a4-169">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="988a4-169">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



