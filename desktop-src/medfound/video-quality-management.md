---
description: 影片品質管制
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: 影片品質管制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943721"
---
# <a name="video-quality-management"></a><span data-ttu-id="1bbe2-103">影片品質管制</span><span class="sxs-lookup"><span data-stu-id="1bbe2-103">Video Quality Management</span></span>

<span data-ttu-id="1bbe2-104">本主題說明 Windows 7 中影片管線的一些改良功能，包括 Microsoft 媒體基礎和 Microsoft DirectShow。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-104">This topic describes some improvements to the video pipeline in Windows 7, both for Microsoft Media Foundation and Microsoft DirectShow.</span></span>

<span data-ttu-id="1bbe2-105">在完美的世界中，不論影片解析度或 CPU/GPU 負載為何，影片都不會有任何問題。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-105">In a perfect world, video would never glitch, regardless of the video resolution or the CPU/GPU load.</span></span> <span data-ttu-id="1bbe2-106">當然，在實際的情況下，影片管線必須能夠處理有限的硬體資源，而且必須以量身打造的方式自訂播放到系統內容。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-106">In reality, of course, the video pipeline must be able to cope with finite hardware resources, and it must adaptively tailor playback to the system environment.</span></span> <span data-ttu-id="1bbe2-107">影片品質管制的目標是：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-107">The goals for video quality management are to:</span></span>

-   <span data-ttu-id="1bbe2-108">減少瑕疵 (捨棄或延遲的畫面) 。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-108">Reduce glitching (dropped or late frames).</span></span>
-   <span data-ttu-id="1bbe2-109">減少記憶體使用量，尤其是在 GPU 中。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-109">Reduce memory usage, especially in the GPU.</span></span>
-   <span data-ttu-id="1bbe2-110">減少耗電量，尤其是在以電池電源執行的膝上型電腦上。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-110">Reduce power consumption, especially in laptops running on battery power.</span></span>
-   <span data-ttu-id="1bbe2-111">在給定的資源條件約束下，獲得最佳的影像品質。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-111">Get the best image quality possible, given resource constraints.</span></span>
-   <span data-ttu-id="1bbe2-112">讓影片與音訊保持同步。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-112">Keep video synchronized with audio.</span></span>

<span data-ttu-id="1bbe2-113">其中某些目標相反，特別是在低終端系統上。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-113">Some of these goals are contrary, particularly on low-end systems.</span></span> <span data-ttu-id="1bbe2-114">一般來說，速度和品質之間會有取捨。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-114">Generally there is a trade-off between speed and quality.</span></span> <span data-ttu-id="1bbe2-115">瑕疵比中等減少視覺品質更令人討厭。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-115">Glitching is more objectionable than moderate reductions in visual quality.</span></span> <span data-ttu-id="1bbe2-116">電源耗用量的相對重要性隨環境而異;在以電池電力執行的膝上型電腦中，這點非常重要。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-116">The relative importance of power consumption varies with the environment; in a laptop running on battery power, it is very important.</span></span>

<span data-ttu-id="1bbe2-117">在 Windows 7 中，增強型影片轉譯器 (EVR) 具有更佳的影片品質管制支援。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-117">In Windows 7, the enhanced video renderer (EVR) has better support for video quality management.</span></span> <span data-ttu-id="1bbe2-118">媒體基礎管線和 DirectShow 管線都已更新，可利用這些功能。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-118">Both the Media Foundation pipeline and the DirectShow pipeline have been updated to take advantage of these capabilities.</span></span> <span data-ttu-id="1bbe2-119">使用的方法有兩種：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-119">A two-pronged approach is used:</span></span>

-   <span data-ttu-id="1bbe2-120">開始播放之前，管線可以根據使用者的電源管理設定和硬體的相關資訊，執行靜態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-120">Before playback starts, the pipeline can perform static optimizations, based on the user's power management settings and information about the hardware.</span></span>
-   <span data-ttu-id="1bbe2-121">播放開始之後，管線可以根據執行時間效能套用動態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-121">After playback starts, the pipeline can apply dynamic optimizations, based on run-time performance.</span></span>

## <a name="quality-management-in-media-foundation"></a><span data-ttu-id="1bbe2-122">媒體基礎中的品質管制</span><span class="sxs-lookup"><span data-stu-id="1bbe2-122">Quality Management in Media Foundation</span></span>

<span data-ttu-id="1bbe2-123">若要啟用靜態優化，請在解析拓撲之前，先在部分拓撲上設定 [MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化](mf-topology-static-playback-optimizations.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-123">To enable static optimizations, set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute on the partial topology before resolving the topology.</span></span> <span data-ttu-id="1bbe2-124">拓撲載入器會在其 [**IMFTopoLoader：： Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) 方法中查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-124">The topology loader queries this attribute in its [**IMFTopoLoader::Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) method.</span></span>

<span data-ttu-id="1bbe2-125">如果您啟用靜態優化，則應該在拓撲上設定兩個其他屬性：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-125">If you enable static optimizations, you should set two other attributes on the topology:</span></span>



| <span data-ttu-id="1bbe2-126">屬性</span><span class="sxs-lookup"><span data-stu-id="1bbe2-126">Attribute</span></span>                                                                                                                                      | <span data-ttu-id="1bbe2-127">描述</span><span class="sxs-lookup"><span data-stu-id="1bbe2-127">Description</span></span>                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1bbe2-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度</span><span class="sxs-lookup"><span data-stu-id="1bbe2-128"><span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span><br/>   | <span data-ttu-id="1bbe2-129">指定影片播放視窗的大小上限。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-129">Specifies the maximum size of the video playback window.</span></span><br/> |
| <span data-ttu-id="1bbe2-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF \_ 拓撲 \_ 播放 \_ 畫面播放速率</span><span class="sxs-lookup"><span data-stu-id="1bbe2-130"><span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span><br/> | <span data-ttu-id="1bbe2-131">指定監視器的重新整理頻率。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-131">Specifies the monitor refresh rate.</span></span><br/>                      |



 

<span data-ttu-id="1bbe2-132">這兩個屬性可協助管線計算品質管制最有效的設定。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-132">These two attributes help the pipeline calculate the most effective setting for quality management.</span></span>

<span data-ttu-id="1bbe2-133">「品質管制員」會執行動態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-133">Dynamic optimizations are performed by the quality manager.</span></span> <span data-ttu-id="1bbe2-134">您不需要採取任何動作來啟用品質管制員;它會自動啟用。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-134">You do not need to do anything to enable the quality manager; it is automatically enabled.</span></span> <span data-ttu-id="1bbe2-135">品質管制員存在於 Windows Vista 中;在 Windows 7 中，EVR 可以更妥善地回應品質管制員的訊息。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-135">The quality manager existed in Windows Vista; in Windows 7, the EVR can respond better to messages from the quality manager.</span></span>

## <a name="quality-management-in-directshow"></a><span data-ttu-id="1bbe2-136">DirectShow 中的品質管制</span><span class="sxs-lookup"><span data-stu-id="1bbe2-136">Quality Management in DirectShow</span></span>

<span data-ttu-id="1bbe2-137">DirectShow 支援 DVD 播放的靜態和動態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-137">DirectShow supports static and dynamic optimizations for DVD playback.</span></span> <span data-ttu-id="1bbe2-138">若要在 DVD 播放應用程式中啟用這些優化，請在 **IDvdGraphBuilder：： RenderDvdVideoVolume** 方法的 *dwFlags* 參數中設定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-138">To enable these optimizations in a DVD playback application, set the following flags in the *dwFlags* parameter of the **IDvdGraphBuilder::RenderDvdVideoVolume** method:</span></span>



| <span data-ttu-id="1bbe2-139">旗標</span><span class="sxs-lookup"><span data-stu-id="1bbe2-139">Flag</span></span>                  | <span data-ttu-id="1bbe2-140">描述</span><span class="sxs-lookup"><span data-stu-id="1bbe2-140">Description</span></span>                    |
|-----------------------|--------------------------------|
| <span data-ttu-id="1bbe2-141">上午 \_ DVD \_ 調整 \_ 圖形</span><span class="sxs-lookup"><span data-stu-id="1bbe2-141">AM\_DVD\_ADAPT\_GRAPH</span></span> | <span data-ttu-id="1bbe2-142">啟用靜態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-142">Enables static optimizations.</span></span>  |
| <span data-ttu-id="1bbe2-143">AM \_ DVD \_ EVR \_ QOS</span><span class="sxs-lookup"><span data-stu-id="1bbe2-143">AM\_DVD\_EVR\_QOS</span></span>     | <span data-ttu-id="1bbe2-144">啟用動態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-144">Enables dynamic optimizations.</span></span> |



 

<span data-ttu-id="1bbe2-145">其他的 DirectShow 應用程式可以直接在 EVR 篩選上呼叫 [**IEVRFilterConfigEx：： SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) 方法來啟用動態優化。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-145">Other DirectShow applications can enable dynamic optimizations by calling the [**IEVRFilterConfigEx::SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) method directly on the EVR filter.</span></span> <span data-ttu-id="1bbe2-146">指定 **EVRFilterConfigPrefs \_ EnableQoS** 旗標。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-146">Specify the **EVRFilterConfigPrefs\_EnableQoS** flag.</span></span>

> [!Note]  
> <span data-ttu-id="1bbe2-147">DirectShow 中的靜態優化僅限於 DVD 播放。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-147">Static optimizations in DirectShow are limited to DVD playback.</span></span>

 

## <a name="quality-management-in-the-evr"></a><span data-ttu-id="1bbe2-148">EVR 中的品質管制</span><span class="sxs-lookup"><span data-stu-id="1bbe2-148">Quality Management in the EVR</span></span>

<span data-ttu-id="1bbe2-149">EVR 支援一些新的設定旗標來進行品質管制。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-149">The EVR supports some new configuration flags for quality management.</span></span> <span data-ttu-id="1bbe2-150">如果您啟用先前所述的品質管制優化，則不需要直接設定這些旗標。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-150">If you enable the quality management optimizations described previously, you do not have to set these flags directly.</span></span> <span data-ttu-id="1bbe2-151">不過，它們會針對想要更細微地控制 EVR 的應用程式記載。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-151">However, they are documented for applications that want more granular control over the EVR.</span></span>

<span data-ttu-id="1bbe2-152">藉由呼叫 [**IMFVideoMixerControl2：： SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) 方法，在 EVR 混音器上設定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-152">Set the following flags on the EVR mixer by calling the [**IMFVideoMixerControl2::SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bbe2-153">Flags</span><span class="sxs-lookup"><span data-stu-id="1bbe2-153">Flags</span></span></th>
<th><span data-ttu-id="1bbe2-154">Description</span><span class="sxs-lookup"><span data-stu-id="1bbe2-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1bbe2-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-155"><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></span></span></li>
<li><span data-ttu-id="1bbe2-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-156"><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="1bbe2-157">略過每個交錯框架的第二個欄位。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-157">Skip the second field of every interlaced frame.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="1bbe2-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-158"><strong>MFVideoMixPrefs_AllowDropToBob</strong></span></span></li>
<li><span data-ttu-id="1bbe2-159"><strong>MFVideoMixPrefs_ForceBob</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-159"><strong>MFVideoMixPrefs_ForceBob</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="1bbe2-160">使用 bob 去交錯，即使驅動程式支援較高品質的交錯模式也是如此。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-160">Use bob deinterlacing, even if the driver supports a higher-quality deinterlace mode.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1bbe2-161">藉由呼叫 [**IMFVideoDisplayControl：： SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) 方法，在 EVR 展示者上設定下列旗標：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-161">Set the following flags on the EVR presenter by calling the [**IMFVideoDisplayControl::SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) method:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bbe2-162">Flags</span><span class="sxs-lookup"><span data-stu-id="1bbe2-162">Flags</span></span></th>
<th><span data-ttu-id="1bbe2-163">Description</span><span class="sxs-lookup"><span data-stu-id="1bbe2-163">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1bbe2-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-164"><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></span></span></li>
<li><span data-ttu-id="1bbe2-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-165"><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="1bbe2-166">節流輸出以符合 GPU 頻寬。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-166">Throttle output to match GPU bandwidth.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="1bbe2-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-167"><strong>MFVideoRenderPrefs_ForceBatching</strong></span></span></li>
<li><span data-ttu-id="1bbe2-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span><span class="sxs-lookup"><span data-stu-id="1bbe2-168"><strong>MFVideoRenderPrefs_AllowBatching</strong></span></span></li>
</ul></td>
<td><span data-ttu-id="1bbe2-169">Batch Direct3D 目前的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-169">Batch Direct3D Present calls.</span></span> <span data-ttu-id="1bbe2-170">這種優化可讓系統更頻繁進入閒置狀態，進而降低耗電量。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-170">This optimization enables the system to enter into idle states more frequently, which can reduce power consumption.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="1bbe2-171">MFVideoRenderPrefs_ForceScaling</span><span class="sxs-lookup"><span data-stu-id="1bbe2-171">MFVideoRenderPrefs_ForceScaling</span></span></li>
<li><span data-ttu-id="1bbe2-172">MFVideoRenderPrefs_AllowScaling</span><span class="sxs-lookup"><span data-stu-id="1bbe2-172">MFVideoRenderPrefs_AllowScaling</span></span></li>
</ul></td>
<td><span data-ttu-id="1bbe2-173">使用小於輸出矩形的矩形來執行混合的影片。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-173">Perform video mixing using a rectangle smaller than the output rectangle.</span></span> <span data-ttu-id="1bbe2-174">將結果調整為正確的輸出大小。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-174">Scale the result to the correct output size.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1bbe2-175">此外，EVR 媒體接收器還支援對應至每個旗標的設定屬性：</span><span class="sxs-lookup"><span data-stu-id="1bbe2-175">In addition, the EVR media sink supports configuration attributes that correspond to each of these flags:</span></span>

-   [<span data-ttu-id="1bbe2-176">EVRConfig \_ AllowBatching</span><span class="sxs-lookup"><span data-stu-id="1bbe2-176">EVRConfig\_AllowBatching</span></span>](evrconfig-allowbatching.md)
-   [<span data-ttu-id="1bbe2-177">EVRConfig \_ AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="1bbe2-177">EVRConfig\_AllowDropToBob</span></span>](evrconfig-allowdroptobob.md)
-   [<span data-ttu-id="1bbe2-178">EVRConfig \_ AllowDropToHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="1bbe2-178">EVRConfig\_AllowDropToHalfInterlace</span></span>](evrconfig-allowdroptohalfinterlace.md)
-   [<span data-ttu-id="1bbe2-179">EVRConfig \_ AllowScaling</span><span class="sxs-lookup"><span data-stu-id="1bbe2-179">EVRConfig\_AllowScaling</span></span>](evrconfig-allowscaling.md)
-   [<span data-ttu-id="1bbe2-180">EVRConfig \_ AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="1bbe2-180">EVRConfig\_AllowDropToThrottle</span></span>](evrconfig-allowdroptothrottle.md)
-   [<span data-ttu-id="1bbe2-181">EVRConfig \_ ForceBatching</span><span class="sxs-lookup"><span data-stu-id="1bbe2-181">EVRConfig\_ForceBatching</span></span>](evrconfig-forcebatching.md)
-   [<span data-ttu-id="1bbe2-182">EVRConfig \_ ForceBob</span><span class="sxs-lookup"><span data-stu-id="1bbe2-182">EVRConfig\_ForceBob</span></span>](evrconfig-forcebob.md)
-   [<span data-ttu-id="1bbe2-183">EVRConfig \_ ForceHalfInterlace</span><span class="sxs-lookup"><span data-stu-id="1bbe2-183">EVRConfig\_ForceHalfInterlace</span></span>](evrconfig-forcehalfinterlace.md)
-   [<span data-ttu-id="1bbe2-184">EVRConfig \_ ForceScaling</span><span class="sxs-lookup"><span data-stu-id="1bbe2-184">EVRConfig\_ForceScaling</span></span>](evrconfig-forcescaling.md)
-   [<span data-ttu-id="1bbe2-185">EVRConfig \_ ForceThrottle</span><span class="sxs-lookup"><span data-stu-id="1bbe2-185">EVRConfig\_ForceThrottle</span></span>](evrconfig-forcethrottle.md)

<span data-ttu-id="1bbe2-186">開始播放之前，您可以直接在 EVR 媒體接收上設定這些屬性，做為呼叫 [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) 和 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) 方法的替代方法。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-186">Before playback starts, you can set these attributes directly on the EVR media sink, as an alternative to calling the [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) and [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) methods.</span></span> <span data-ttu-id="1bbe2-187">若要設定這些屬性，請查詢 EVR 媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)。</span><span class="sxs-lookup"><span data-stu-id="1bbe2-187">To set these attributes, query the EVR media sink for [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bbe2-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bbe2-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bbe2-189">媒體會話</span><span class="sxs-lookup"><span data-stu-id="1bbe2-189">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 




