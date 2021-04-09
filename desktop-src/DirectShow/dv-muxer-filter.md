---
description: DV Muxer 濾波器
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688376"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="cc322-103">DV Muxer 濾波器</span><span class="sxs-lookup"><span data-stu-id="cc322-103">DV Muxer Filter</span></span>

<span data-ttu-id="cc322-104">此篩選器結合數位視訊 (DV) 編碼的影片串流與一或兩個音訊串流，以產生交錯的 DV 串流。</span><span class="sxs-lookup"><span data-stu-id="cc322-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="cc322-105">若要將資料流程寫入 AVI 檔案，請將此篩選連接到 [Avi mux](avi-mux-filter.md) 篩選器，並將 *AVI mux* 連接至檔案 [寫入](file-writer-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="cc322-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="cc322-106">如需詳細資訊，請參閱 [DirectShow 中的數位視訊](digital-video-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="cc322-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc322-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="cc322-107">Filter Interfaces</span></span>                        | <span data-ttu-id="cc322-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="cc322-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="cc322-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cc322-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="cc322-110">**影片**：媒體媒體 \_ 、MEDIASUBTYPE \_ Dvsd、format \_ VideoInfo **Audio**：媒體媒體 \_ 、MEDIASUBTYPE \_ PCM、format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="cc322-110">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="cc322-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cc322-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cc322-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cc322-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="cc322-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cc322-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="cc322-114">媒體 \_ 中交錯、MEDIASUBTYPE \_ DVSD、格式 \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="cc322-114">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="cc322-115">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="cc322-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="cc322-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cc322-116">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="cc322-117">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="cc322-117">Filter CLSID</span></span>                             | <span data-ttu-id="cc322-118">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="cc322-118">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="cc322-119">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="cc322-119">Property Page CLSID</span></span>                      | <span data-ttu-id="cc322-120">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="cc322-120">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="cc322-121">可執行檔</span><span class="sxs-lookup"><span data-stu-id="cc322-121">Executable</span></span>                               | <span data-ttu-id="cc322-122">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="cc322-122">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="cc322-123">優點</span><span class="sxs-lookup"><span data-stu-id="cc322-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="cc322-124">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="cc322-124">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="cc322-125">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="cc322-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cc322-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cc322-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="cc322-127">備註</span><span class="sxs-lookup"><span data-stu-id="cc322-127">Remarks</span></span>

<span data-ttu-id="cc322-128">DV Muxer 可以建立兩個音訊輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="cc322-128">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="cc322-129">它支援下表所示的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="cc322-129">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="cc322-130">音訊 Pin 1</span><span class="sxs-lookup"><span data-stu-id="cc322-130">Audio Pin 1</span></span>

<span data-ttu-id="cc322-131">音訊 Pin 2</span><span class="sxs-lookup"><span data-stu-id="cc322-131">Audio Pin 2</span></span>

<span data-ttu-id="cc322-132">輸出格式</span><span class="sxs-lookup"><span data-stu-id="cc322-132">Output Format</span></span>

<span data-ttu-id="cc322-133">取樣率 (kHz) </span><span class="sxs-lookup"><span data-stu-id="cc322-133">Sample Rate (kHz)</span></span>

<span data-ttu-id="cc322-134">位/範例</span><span class="sxs-lookup"><span data-stu-id="cc322-134">Bits/Sample</span></span>

<span data-ttu-id="cc322-135">通道</span><span class="sxs-lookup"><span data-stu-id="cc322-135">Channels</span></span>

<span data-ttu-id="cc322-136">採樣速率</span><span class="sxs-lookup"><span data-stu-id="cc322-136">Sample Rate</span></span>

<span data-ttu-id="cc322-137">位/範例</span><span class="sxs-lookup"><span data-stu-id="cc322-137">Bits/Sample</span></span>

<span data-ttu-id="cc322-138">通道</span><span class="sxs-lookup"><span data-stu-id="cc322-138">Channels</span></span>

<span data-ttu-id="cc322-139">32</span><span class="sxs-lookup"><span data-stu-id="cc322-139">32</span></span>

<span data-ttu-id="cc322-140">16</span><span class="sxs-lookup"><span data-stu-id="cc322-140">16</span></span>

<span data-ttu-id="cc322-141">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-141">Mono</span></span>

<span data-ttu-id="cc322-142">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-142">Unconnected</span></span>

<span data-ttu-id="cc322-143">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-143">SD 2 Channel</span></span>

<span data-ttu-id="cc322-144">32</span><span class="sxs-lookup"><span data-stu-id="cc322-144">32</span></span>

<span data-ttu-id="cc322-145">16</span><span class="sxs-lookup"><span data-stu-id="cc322-145">16</span></span>

<span data-ttu-id="cc322-146">立體聲</span><span class="sxs-lookup"><span data-stu-id="cc322-146">Stereo</span></span>

<span data-ttu-id="cc322-147">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-147">Unconnected</span></span>

<span data-ttu-id="cc322-148">SD 4 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-148">SD 4 Channel</span></span>

<span data-ttu-id="cc322-149">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="cc322-149">44.1 or 48</span></span>

<span data-ttu-id="cc322-150">16</span><span class="sxs-lookup"><span data-stu-id="cc322-150">16</span></span>

<span data-ttu-id="cc322-151">身歷聲或 Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-151">Stereo or Mono</span></span>

<span data-ttu-id="cc322-152">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-152">Unconnected</span></span>

<span data-ttu-id="cc322-153">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-153">SD 2 Channel</span></span>

<span data-ttu-id="cc322-154">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-154">Unconnected</span></span>

<span data-ttu-id="cc322-155">32</span><span class="sxs-lookup"><span data-stu-id="cc322-155">32</span></span>

<span data-ttu-id="cc322-156">16</span><span class="sxs-lookup"><span data-stu-id="cc322-156">16</span></span>

<span data-ttu-id="cc322-157">身歷聲或 Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-157">Stereo or Mono</span></span>

<span data-ttu-id="cc322-158">不允許</span><span class="sxs-lookup"><span data-stu-id="cc322-158">Disallowed</span></span>

<span data-ttu-id="cc322-159">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-159">Unconnected</span></span>

<span data-ttu-id="cc322-160">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="cc322-160">44.1 or 48</span></span>

<span data-ttu-id="cc322-161">16</span><span class="sxs-lookup"><span data-stu-id="cc322-161">16</span></span>

<span data-ttu-id="cc322-162">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-162">Mono</span></span>

<span data-ttu-id="cc322-163">不允許</span><span class="sxs-lookup"><span data-stu-id="cc322-163">Disallowed</span></span>

<span data-ttu-id="cc322-164">無關</span><span class="sxs-lookup"><span data-stu-id="cc322-164">Unconnected</span></span>

<span data-ttu-id="cc322-165">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="cc322-165">44.1 or 48</span></span>

<span data-ttu-id="cc322-166">16</span><span class="sxs-lookup"><span data-stu-id="cc322-166">16</span></span>

<span data-ttu-id="cc322-167">立體聲</span><span class="sxs-lookup"><span data-stu-id="cc322-167">Stereo</span></span>

<span data-ttu-id="cc322-168">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-168">SD 2 Channel</span></span>

<span data-ttu-id="cc322-169">32</span><span class="sxs-lookup"><span data-stu-id="cc322-169">32</span></span>

<span data-ttu-id="cc322-170">16</span><span class="sxs-lookup"><span data-stu-id="cc322-170">16</span></span>

<span data-ttu-id="cc322-171">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-171">Mono</span></span>

<span data-ttu-id="cc322-172">32</span><span class="sxs-lookup"><span data-stu-id="cc322-172">32</span></span>

<span data-ttu-id="cc322-173">16</span><span class="sxs-lookup"><span data-stu-id="cc322-173">16</span></span>

<span data-ttu-id="cc322-174">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-174">Mono</span></span>

<span data-ttu-id="cc322-175">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-175">SD 2 Channel</span></span>

<span data-ttu-id="cc322-176">32</span><span class="sxs-lookup"><span data-stu-id="cc322-176">32</span></span>

<span data-ttu-id="cc322-177">16</span><span class="sxs-lookup"><span data-stu-id="cc322-177">16</span></span>

<span data-ttu-id="cc322-178">身歷聲或 Mono\*</span><span class="sxs-lookup"><span data-stu-id="cc322-178">Stereo or Mono\*</span></span>

<span data-ttu-id="cc322-179">32</span><span class="sxs-lookup"><span data-stu-id="cc322-179">32</span></span>

<span data-ttu-id="cc322-180">16</span><span class="sxs-lookup"><span data-stu-id="cc322-180">16</span></span>

<span data-ttu-id="cc322-181">身歷聲或 Mono\*</span><span class="sxs-lookup"><span data-stu-id="cc322-181">Stereo or Mono\*</span></span>

<span data-ttu-id="cc322-182">SD 4 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-182">SD 4 Channel</span></span>

<span data-ttu-id="cc322-183">44.1</span><span class="sxs-lookup"><span data-stu-id="cc322-183">44.1</span></span>

<span data-ttu-id="cc322-184">16</span><span class="sxs-lookup"><span data-stu-id="cc322-184">16</span></span>

<span data-ttu-id="cc322-185">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-185">Mono</span></span>

<span data-ttu-id="cc322-186">44.1</span><span class="sxs-lookup"><span data-stu-id="cc322-186">44.1</span></span>

<span data-ttu-id="cc322-187">16</span><span class="sxs-lookup"><span data-stu-id="cc322-187">16</span></span>

<span data-ttu-id="cc322-188">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-188">Mono</span></span>

<span data-ttu-id="cc322-189">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-189">SD 2 Channel</span></span>

<span data-ttu-id="cc322-190">48</span><span class="sxs-lookup"><span data-stu-id="cc322-190">48</span></span>

<span data-ttu-id="cc322-191">16</span><span class="sxs-lookup"><span data-stu-id="cc322-191">16</span></span>

<span data-ttu-id="cc322-192">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-192">Mono</span></span>

<span data-ttu-id="cc322-193">48</span><span class="sxs-lookup"><span data-stu-id="cc322-193">48</span></span>

<span data-ttu-id="cc322-194">16</span><span class="sxs-lookup"><span data-stu-id="cc322-194">16</span></span>

<span data-ttu-id="cc322-195">Mono</span><span class="sxs-lookup"><span data-stu-id="cc322-195">Mono</span></span>

<span data-ttu-id="cc322-196">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="cc322-196">SD 2 Channel</span></span>

<span data-ttu-id="cc322-197">\* 如果至少有一個輸入 pin 是身歷聲。</span><span class="sxs-lookup"><span data-stu-id="cc322-197">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="cc322-198">基於此表格的目的，音訊 pin 1 會定義為連接到音訊來源的第一個輸入連接，而音訊 pin 2 則定義為連接到音訊來源的第二個輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="cc322-198">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="cc322-199">連接音訊 pin 之後，除非兩個音訊針腳都已中斷連線，否則此編號配置仍會保持有效。</span><span class="sxs-lookup"><span data-stu-id="cc322-199">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="cc322-200">例如，如果您連接兩個音訊針腳，然後中斷音訊 pin 1 的連線，則剩餘的 pin 仍會被視為 pin 2。</span><span class="sxs-lookup"><span data-stu-id="cc322-200">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="cc322-201">提供給 pin 1 的音訊會記錄至 DV 框架的第一個音訊區塊 (CH1) ，而提供給針腳2的音訊會記錄到第二個音訊區塊 (CH2) 。</span><span class="sxs-lookup"><span data-stu-id="cc322-201">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="cc322-202">例外狀況：如果篩選器的 44.1 kHz 或 48 kHz 有單一的身歷聲輸入，則左側音訊頻道會記錄到第一個音訊區塊，而右邊的音訊頻道會記錄到第二個音訊區塊。</span><span class="sxs-lookup"><span data-stu-id="cc322-202">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="cc322-203">針對 SD 4-通道輸出：如果輸入為身歷聲，則會將左軌記錄到 CHa 或 CHc，並將正確的曲目記錄到 CHb 或 CHd。</span><span class="sxs-lookup"><span data-stu-id="cc322-203">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="cc322-204">如果輸入為 mono，則會將音訊記錄為 CHa 或 CHc，而 CHb 和 CHd 為無訊息。</span><span class="sxs-lookup"><span data-stu-id="cc322-204">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="cc322-205">藉由連接並中斷連接音訊 pin 1，就可以達到不允許的格式。</span><span class="sxs-lookup"><span data-stu-id="cc322-205">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="cc322-206">在此情況下，篩選的 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法會傳回 VFW \_ E \_ 未 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="cc322-206">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="cc322-207">這項限制可防止第一個音訊區塊沒有音訊，但第二個音訊區塊有音訊的情況。</span><span class="sxs-lookup"><span data-stu-id="cc322-207">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="cc322-208">第二個區塊只有在第一個區塊也有音訊時，才應該有音訊。</span><span class="sxs-lookup"><span data-stu-id="cc322-208">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="cc322-209">DV Muxer 不允許具有不同取樣率的音訊輸入。</span><span class="sxs-lookup"><span data-stu-id="cc322-209">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="cc322-210">不過，圖形建立方法（例如 [**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ）通常會新增「高階 [包裝](acm-wrapper-filter.md) 函式」篩選器，這會將第二個音訊串流轉換成符合第一個資料流程的取樣率。</span><span class="sxs-lookup"><span data-stu-id="cc322-210">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="cc322-211">如果音訊輸入是 48 kHz 或 32 kHz，音訊輸出會被鎖定。</span><span class="sxs-lookup"><span data-stu-id="cc322-211">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="cc322-212"> (不能鎖定 44.1-kHz 音訊。 ) </span><span class="sxs-lookup"><span data-stu-id="cc322-212">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="cc322-213">如果沒有連線音訊 pin，輸出會包含傳入 DV 框架的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="cc322-213">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="cc322-214">這可能是靜音或有效的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="cc322-214">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc322-215">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc322-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc322-216">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="cc322-216">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="cc322-217">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="cc322-217">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



