---
description: DV Muxer 濾波器
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: DV Muxer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908596"
---
# <a name="dv-muxer-filter"></a><span data-ttu-id="de3d4-103">DV Muxer 濾波器</span><span class="sxs-lookup"><span data-stu-id="de3d4-103">DV Muxer Filter</span></span>

<span data-ttu-id="de3d4-104">此篩選器結合數位視訊 (DV) 編碼的影片串流與一或兩個音訊串流，以產生交錯的 DV 串流。</span><span class="sxs-lookup"><span data-stu-id="de3d4-104">This filter combines a digital video (DV)—encoded video stream with one or two audio streams to produce an interleaved DV stream.</span></span> <span data-ttu-id="de3d4-105">若要將資料流程寫入 AVI 檔案，請將此篩選連接到 [Avi mux](avi-mux-filter.md) 篩選器，並將 *AVI mux* 連接至檔案 [寫入](file-writer-filter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="de3d4-105">To write the stream to an AVI file, connect this filter to the [AVI Mux](avi-mux-filter.md) filter and connect the *AVI Mux* to the [File Writer](file-writer-filter.md) filter.</span></span> <span data-ttu-id="de3d4-106">如需詳細資訊，請參閱 [DirectShow 中的數位視訊](digital-video-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="de3d4-106">For more information, see [Digital Video in DirectShow](digital-video-in-directshow.md).</span></span>



| <span data-ttu-id="de3d4-107">標籤</span><span class="sxs-lookup"><span data-stu-id="de3d4-107">Label</span></span> | <span data-ttu-id="de3d4-108">值</span><span class="sxs-lookup"><span data-stu-id="de3d4-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3d4-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="de3d4-109">Filter Interfaces</span></span>                        | <span data-ttu-id="de3d4-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="de3d4-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span>                                                             |
| <span data-ttu-id="de3d4-111">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="de3d4-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="de3d4-112">**影片**：媒體媒體 \_ 、MEDIASUBTYPE \_ Dvsd、format \_ VideoInfo **Audio**：媒體媒體 \_ 、MEDIASUBTYPE \_ PCM、format \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="de3d4-112">**Video**: MEDIATYPE\_Video, MEDIASUBTYPE\_dvsd, FORMAT\_VideoInfo **Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span> |
| <span data-ttu-id="de3d4-113">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="de3d4-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="de3d4-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="de3d4-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                 |
| <span data-ttu-id="de3d4-115">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="de3d4-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="de3d4-116">媒體 \_ 中交錯、MEDIASUBTYPE \_ DVSD、格式 \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="de3d4-116">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                             |
| <span data-ttu-id="de3d4-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="de3d4-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="de3d4-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="de3d4-118">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                       |
| <span data-ttu-id="de3d4-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="de3d4-119">Filter CLSID</span></span>                             | <span data-ttu-id="de3d4-120">CLSID \_ DVMux</span><span class="sxs-lookup"><span data-stu-id="de3d4-120">CLSID\_DVMux</span></span>                                                                                                                           |
| <span data-ttu-id="de3d4-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="de3d4-121">Property Page CLSID</span></span>                      | <span data-ttu-id="de3d4-122">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="de3d4-122">No property page</span></span>                                                                                                                       |
| <span data-ttu-id="de3d4-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="de3d4-123">Executable</span></span>                               | <span data-ttu-id="de3d4-124">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="de3d4-124">qdv.dll</span></span>                                                                                                                                |
| [<span data-ttu-id="de3d4-125">優點</span><span class="sxs-lookup"><span data-stu-id="de3d4-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="de3d4-126">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="de3d4-126">MERIT\_UNLIKELY</span></span>                                                                                                                        |
| [<span data-ttu-id="de3d4-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="de3d4-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="de3d4-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="de3d4-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="de3d4-129">備註</span><span class="sxs-lookup"><span data-stu-id="de3d4-129">Remarks</span></span>

<span data-ttu-id="de3d4-130">DV Muxer 可以建立兩個音訊輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="de3d4-130">The DV Muxer can create two audio input pins.</span></span> <span data-ttu-id="de3d4-131">它支援下表所示的音訊格式。</span><span class="sxs-lookup"><span data-stu-id="de3d4-131">It supports the audio formats shown in the following table.</span></span>



<span data-ttu-id="de3d4-132">音訊 Pin 1</span><span class="sxs-lookup"><span data-stu-id="de3d4-132">Audio Pin 1</span></span>

<span data-ttu-id="de3d4-133">音訊 Pin 2</span><span class="sxs-lookup"><span data-stu-id="de3d4-133">Audio Pin 2</span></span>

<span data-ttu-id="de3d4-134">輸出格式</span><span class="sxs-lookup"><span data-stu-id="de3d4-134">Output Format</span></span>

<span data-ttu-id="de3d4-135">取樣率 (kHz) </span><span class="sxs-lookup"><span data-stu-id="de3d4-135">Sample Rate (kHz)</span></span>

<span data-ttu-id="de3d4-136">位/範例</span><span class="sxs-lookup"><span data-stu-id="de3d4-136">Bits/Sample</span></span>

<span data-ttu-id="de3d4-137">通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-137">Channels</span></span>

<span data-ttu-id="de3d4-138">採樣速率</span><span class="sxs-lookup"><span data-stu-id="de3d4-138">Sample Rate</span></span>

<span data-ttu-id="de3d4-139">位/範例</span><span class="sxs-lookup"><span data-stu-id="de3d4-139">Bits/Sample</span></span>

<span data-ttu-id="de3d4-140">通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-140">Channels</span></span>

<span data-ttu-id="de3d4-141">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-141">32</span></span>

<span data-ttu-id="de3d4-142">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-142">16</span></span>

<span data-ttu-id="de3d4-143">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-143">Mono</span></span>

<span data-ttu-id="de3d4-144">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-144">Unconnected</span></span>

<span data-ttu-id="de3d4-145">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-145">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-146">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-146">32</span></span>

<span data-ttu-id="de3d4-147">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-147">16</span></span>

<span data-ttu-id="de3d4-148">立體聲</span><span class="sxs-lookup"><span data-stu-id="de3d4-148">Stereo</span></span>

<span data-ttu-id="de3d4-149">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-149">Unconnected</span></span>

<span data-ttu-id="de3d4-150">SD 4 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-150">SD 4 Channel</span></span>

<span data-ttu-id="de3d4-151">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="de3d4-151">44.1 or 48</span></span>

<span data-ttu-id="de3d4-152">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-152">16</span></span>

<span data-ttu-id="de3d4-153">身歷聲或 Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-153">Stereo or Mono</span></span>

<span data-ttu-id="de3d4-154">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-154">Unconnected</span></span>

<span data-ttu-id="de3d4-155">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-155">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-156">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-156">Unconnected</span></span>

<span data-ttu-id="de3d4-157">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-157">32</span></span>

<span data-ttu-id="de3d4-158">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-158">16</span></span>

<span data-ttu-id="de3d4-159">身歷聲或 Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-159">Stereo or Mono</span></span>

<span data-ttu-id="de3d4-160">不允許</span><span class="sxs-lookup"><span data-stu-id="de3d4-160">Disallowed</span></span>

<span data-ttu-id="de3d4-161">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-161">Unconnected</span></span>

<span data-ttu-id="de3d4-162">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="de3d4-162">44.1 or 48</span></span>

<span data-ttu-id="de3d4-163">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-163">16</span></span>

<span data-ttu-id="de3d4-164">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-164">Mono</span></span>

<span data-ttu-id="de3d4-165">不允許</span><span class="sxs-lookup"><span data-stu-id="de3d4-165">Disallowed</span></span>

<span data-ttu-id="de3d4-166">無關</span><span class="sxs-lookup"><span data-stu-id="de3d4-166">Unconnected</span></span>

<span data-ttu-id="de3d4-167">44.1 或48</span><span class="sxs-lookup"><span data-stu-id="de3d4-167">44.1 or 48</span></span>

<span data-ttu-id="de3d4-168">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-168">16</span></span>

<span data-ttu-id="de3d4-169">立體聲</span><span class="sxs-lookup"><span data-stu-id="de3d4-169">Stereo</span></span>

<span data-ttu-id="de3d4-170">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-170">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-171">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-171">32</span></span>

<span data-ttu-id="de3d4-172">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-172">16</span></span>

<span data-ttu-id="de3d4-173">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-173">Mono</span></span>

<span data-ttu-id="de3d4-174">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-174">32</span></span>

<span data-ttu-id="de3d4-175">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-175">16</span></span>

<span data-ttu-id="de3d4-176">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-176">Mono</span></span>

<span data-ttu-id="de3d4-177">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-177">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-178">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-178">32</span></span>

<span data-ttu-id="de3d4-179">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-179">16</span></span>

<span data-ttu-id="de3d4-180">身歷聲或 Mono\*</span><span class="sxs-lookup"><span data-stu-id="de3d4-180">Stereo or Mono\*</span></span>

<span data-ttu-id="de3d4-181">32</span><span class="sxs-lookup"><span data-stu-id="de3d4-181">32</span></span>

<span data-ttu-id="de3d4-182">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-182">16</span></span>

<span data-ttu-id="de3d4-183">身歷聲或 Mono\*</span><span class="sxs-lookup"><span data-stu-id="de3d4-183">Stereo or Mono\*</span></span>

<span data-ttu-id="de3d4-184">SD 4 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-184">SD 4 Channel</span></span>

<span data-ttu-id="de3d4-185">44.1</span><span class="sxs-lookup"><span data-stu-id="de3d4-185">44.1</span></span>

<span data-ttu-id="de3d4-186">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-186">16</span></span>

<span data-ttu-id="de3d4-187">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-187">Mono</span></span>

<span data-ttu-id="de3d4-188">44.1</span><span class="sxs-lookup"><span data-stu-id="de3d4-188">44.1</span></span>

<span data-ttu-id="de3d4-189">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-189">16</span></span>

<span data-ttu-id="de3d4-190">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-190">Mono</span></span>

<span data-ttu-id="de3d4-191">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-191">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-192">48</span><span class="sxs-lookup"><span data-stu-id="de3d4-192">48</span></span>

<span data-ttu-id="de3d4-193">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-193">16</span></span>

<span data-ttu-id="de3d4-194">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-194">Mono</span></span>

<span data-ttu-id="de3d4-195">48</span><span class="sxs-lookup"><span data-stu-id="de3d4-195">48</span></span>

<span data-ttu-id="de3d4-196">16</span><span class="sxs-lookup"><span data-stu-id="de3d4-196">16</span></span>

<span data-ttu-id="de3d4-197">Mono</span><span class="sxs-lookup"><span data-stu-id="de3d4-197">Mono</span></span>

<span data-ttu-id="de3d4-198">SD 2 通道</span><span class="sxs-lookup"><span data-stu-id="de3d4-198">SD 2 Channel</span></span>

<span data-ttu-id="de3d4-199">\* 如果至少有一個輸入 pin 是身歷聲。</span><span class="sxs-lookup"><span data-stu-id="de3d4-199">\* If at least one input pin is stereo.</span></span>



 

<span data-ttu-id="de3d4-200">基於此表格的目的，音訊 pin 1 會定義為連接到音訊來源的第一個輸入連接，而音訊 pin 2 則定義為連接到音訊來源的第二個輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="de3d4-200">For the purpose of this table, audio pin 1 is defined as the first input pin connected to an audio source, and audio pin 2 is defined as the second input pin connected to an audio source.</span></span> <span data-ttu-id="de3d4-201">連接音訊 pin 之後，除非兩個音訊針腳都已中斷連線，否則此編號配置仍會保持有效。</span><span class="sxs-lookup"><span data-stu-id="de3d4-201">Once an audio pin is connected, this numbering scheme remains in effect unless both audio pins are disconnected.</span></span> <span data-ttu-id="de3d4-202">例如，如果您連接兩個音訊針腳，然後中斷音訊 pin 1 的連線，則剩餘的 pin 仍會被視為 pin 2。</span><span class="sxs-lookup"><span data-stu-id="de3d4-202">For example, if you connect both audio pins and then disconnect audio pin 1, the remaining pin is still considered pin 2.</span></span>

<span data-ttu-id="de3d4-203">提供給 pin 1 的音訊會記錄至 DV 框架的第一個音訊區塊 (CH1) ，而提供給針腳2的音訊會記錄到第二個音訊區塊 (CH2) 。</span><span class="sxs-lookup"><span data-stu-id="de3d4-203">Audio supplied to pin 1 is recorded to the first audio block of the DV frames (CH1), and audio supplied to pin 2 is recorded to the second audio block (CH2).</span></span> <span data-ttu-id="de3d4-204">例外狀況：如果篩選器的 44.1 kHz 或 48 kHz 有單一的身歷聲輸入，則左側音訊頻道會記錄到第一個音訊區塊，而右邊的音訊頻道會記錄到第二個音訊區塊。</span><span class="sxs-lookup"><span data-stu-id="de3d4-204">Exception: if the filter has a single stereo input at 44.1 kHz or 48 kHz, the left audio channel is recorded to the first audio block, and the right audio channel is recorded to the second audio block.</span></span>

<span data-ttu-id="de3d4-205">針對 SD 4-通道輸出：如果輸入為身歷聲，則會將左軌記錄到 CHa 或 CHc，並將正確的曲目記錄到 CHb 或 CHd。</span><span class="sxs-lookup"><span data-stu-id="de3d4-205">For SD 4-channel output: If the input is stereo, the left track is recorded to CHa or CHc, and the right track is recorded to CHb or CHd.</span></span> <span data-ttu-id="de3d4-206">如果輸入為 mono，則會將音訊記錄為 CHa 或 CHc，而 CHb 和 CHd 為無訊息。</span><span class="sxs-lookup"><span data-stu-id="de3d4-206">If the input is mono, the audio is recorded to CHa or CHc, and CHb and CHd are silent.</span></span>

<span data-ttu-id="de3d4-207">藉由連接並中斷連接音訊 pin 1，就可以達到不允許的格式。</span><span class="sxs-lookup"><span data-stu-id="de3d4-207">By connecting and disconnecting audio pin 1, it is possible to reach a disallowed format.</span></span> <span data-ttu-id="de3d4-208">在此情況下，篩選的 [**IMediaFilter：:P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) 方法會傳回 VFW \_ E \_ 未 \_ 連接。</span><span class="sxs-lookup"><span data-stu-id="de3d4-208">In that case, the filter's [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method returns VFW\_E\_NOT\_CONNECTED.</span></span> <span data-ttu-id="de3d4-209">這項限制可防止第一個音訊區塊沒有音訊，但第二個音訊區塊有音訊的情況。</span><span class="sxs-lookup"><span data-stu-id="de3d4-209">This limitation prevents a situation in which the first audio block has no audio, but the second audio block does have audio.</span></span> <span data-ttu-id="de3d4-210">第二個區塊只有在第一個區塊也有音訊時，才應該有音訊。</span><span class="sxs-lookup"><span data-stu-id="de3d4-210">The second block should have audio only if the first block also has audio.</span></span>

<span data-ttu-id="de3d4-211">DV Muxer 不允許具有不同取樣率的音訊輸入。</span><span class="sxs-lookup"><span data-stu-id="de3d4-211">The DV Muxer does not permit audio inputs with different sampling rates.</span></span> <span data-ttu-id="de3d4-212">不過，圖形建立方法（例如 [**IGraphBuilder：： Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ）通常會新增「高階 [包裝](acm-wrapper-filter.md) 函式」篩選器，這會將第二個音訊串流轉換成符合第一個資料流程的取樣率。</span><span class="sxs-lookup"><span data-stu-id="de3d4-212">However, graph-building methods such as [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) will typically add the [ACM Wrapper](acm-wrapper-filter.md) filter, which will convert the second audio stream to match the first stream's sampling rate.</span></span>

<span data-ttu-id="de3d4-213">如果音訊輸入是 48 kHz 或 32 kHz，音訊輸出會被鎖定。</span><span class="sxs-lookup"><span data-stu-id="de3d4-213">If the audio input is 48 kHz or 32 kHz, the audio output is locked.</span></span> <span data-ttu-id="de3d4-214"> (不能鎖定 44.1-kHz 音訊。 ) </span><span class="sxs-lookup"><span data-stu-id="de3d4-214">(It is not possible to lock 44.1-kHz audio.)</span></span>

<span data-ttu-id="de3d4-215">如果沒有連線音訊 pin，輸出會包含傳入 DV 框架的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="de3d4-215">If no audio pins are connected, the output contains the audio data from the incoming DV frames.</span></span> <span data-ttu-id="de3d4-216">這可能是靜音或有效的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="de3d4-216">This might be silence, or valid audio data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de3d4-217">相關主題</span><span class="sxs-lookup"><span data-stu-id="de3d4-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de3d4-218">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="de3d4-218">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="de3d4-219">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="de3d4-219">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



