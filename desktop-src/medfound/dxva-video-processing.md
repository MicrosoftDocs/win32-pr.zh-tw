---
description: DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。 影片處理服務包含去交錯和影片混合。
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: DXVA 影片處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510797"
---
# <a name="dxva-video-processing"></a><span data-ttu-id="f596e-104">DXVA 影片處理</span><span class="sxs-lookup"><span data-stu-id="f596e-104">DXVA Video Processing</span></span>

<span data-ttu-id="f596e-105">DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。</span><span class="sxs-lookup"><span data-stu-id="f596e-105">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="f596e-106">影片處理服務包含去交錯和影片混合。</span><span class="sxs-lookup"><span data-stu-id="f596e-106">Video processing services include deinterlacing and video mixing.</span></span>

<span data-ttu-id="f596e-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="f596e-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f596e-108">概觀</span><span class="sxs-lookup"><span data-stu-id="f596e-108">Overview</span></span>](#overview)
-   [<span data-ttu-id="f596e-109">建立視頻處理裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-109">Creating a Video Processing Device</span></span>](#creating-a-video-processing-device)
    -   [<span data-ttu-id="f596e-110">取得 IDirectXVideoProcessorService 指標</span><span class="sxs-lookup"><span data-stu-id="f596e-110">Get the IDirectXVideoProcessorService Pointer</span></span>](#get-the-idirectxvideoprocessorservice-pointer)
    -   [<span data-ttu-id="f596e-111">列舉影片處理裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-111">Enumerate the Video Processing Devices</span></span>](#enumerate-the-video-processing-devices)
    -   [<span data-ttu-id="f596e-112">列舉 Render-Target 格式</span><span class="sxs-lookup"><span data-stu-id="f596e-112">Enumerate Render-Target Formats</span></span>](#enumerate-render-target-formats)
    -   [<span data-ttu-id="f596e-113">查詢裝置功能</span><span class="sxs-lookup"><span data-stu-id="f596e-113">Query the Device Capabilities</span></span>](#query-the-device-capabilities)
    -   [<span data-ttu-id="f596e-114">建立裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-114">Create the Device</span></span>](#create-the-device)
-   [<span data-ttu-id="f596e-115">影片流程 Array.blit</span><span class="sxs-lookup"><span data-stu-id="f596e-115">Video Process Blit</span></span>](#video-process-blit)
    -   [<span data-ttu-id="f596e-116">Array.blit 參數</span><span class="sxs-lookup"><span data-stu-id="f596e-116">Blit Parameters</span></span>](#blit-parameters)
    -   [<span data-ttu-id="f596e-117">輸入範例</span><span class="sxs-lookup"><span data-stu-id="f596e-117">Input Samples</span></span>](#input-samples)
-   [<span data-ttu-id="f596e-118">影像組合</span><span class="sxs-lookup"><span data-stu-id="f596e-118">Image Composition</span></span>](#image-composition)
    -   [<span data-ttu-id="f596e-119">範例1：上下黑邊縮</span><span class="sxs-lookup"><span data-stu-id="f596e-119">Example 1: Letterboxing</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="f596e-120">範例2：延展子串流映射</span><span class="sxs-lookup"><span data-stu-id="f596e-120">Example 2: Stretching Substream Images</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="f596e-121">範例3：不相符的資料流程高度</span><span class="sxs-lookup"><span data-stu-id="f596e-121">Example 3: Mismatched Stream Heights</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="f596e-122">範例4：目標矩形小於目的介面</span><span class="sxs-lookup"><span data-stu-id="f596e-122">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [<span data-ttu-id="f596e-123">範例5：來源矩形</span><span class="sxs-lookup"><span data-stu-id="f596e-123">Example 5: Source Rectangles</span></span>](#example-5-source-rectangles)
    -   [<span data-ttu-id="f596e-124">範例6：交集的目的地矩形</span><span class="sxs-lookup"><span data-stu-id="f596e-124">Example 6: Intersecting Destination Rectangles</span></span>](#example-6-intersecting-destination-rectangles)
    -   [<span data-ttu-id="f596e-125">範例7：延展和裁剪影片</span><span class="sxs-lookup"><span data-stu-id="f596e-125">Example 7: Stretching and Cropping Video</span></span>](#example-7-stretching-and-cropping-video)
-   [<span data-ttu-id="f596e-126">輸入範例順序</span><span class="sxs-lookup"><span data-stu-id="f596e-126">Input Sample Order</span></span>](#input-sample-order)
    -   [<span data-ttu-id="f596e-127">範例 1</span><span class="sxs-lookup"><span data-stu-id="f596e-127">Example 1</span></span>](#example-1-letterboxing)
    -   [<span data-ttu-id="f596e-128">範例 2</span><span class="sxs-lookup"><span data-stu-id="f596e-128">Example 2</span></span>](#example-2-stretching-substream-images)
    -   [<span data-ttu-id="f596e-129">範例 3</span><span class="sxs-lookup"><span data-stu-id="f596e-129">Example 3</span></span>](#example-3-mismatched-stream-heights)
    -   [<span data-ttu-id="f596e-130">範例 4</span><span class="sxs-lookup"><span data-stu-id="f596e-130">Example 4</span></span>](#example-4-target-rectangle-smaller-than-destination-surface)
-   [<span data-ttu-id="f596e-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="f596e-131">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="f596e-132">概觀</span><span class="sxs-lookup"><span data-stu-id="f596e-132">Overview</span></span>

<span data-ttu-id="f596e-133">圖形硬體可以使用圖形處理器 (GPU) 來處理未壓縮的影片影像。</span><span class="sxs-lookup"><span data-stu-id="f596e-133">Graphics hardware can use the graphics processing unit (GPU) to process uncompressed video images.</span></span> <span data-ttu-id="f596e-134">*影片處理* 裝置是封裝這些功能的軟體元件。</span><span class="sxs-lookup"><span data-stu-id="f596e-134">A *video processing* device is a software component that encapsulates these functions.</span></span> <span data-ttu-id="f596e-135">應用程式可以使用影片處理裝置來執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="f596e-135">Applications can use a video processing device to perform functions such as:</span></span>

-   <span data-ttu-id="f596e-136">去交錯和反向電視</span><span class="sxs-lookup"><span data-stu-id="f596e-136">Deinterlacing and inverse telecine</span></span>
-   <span data-ttu-id="f596e-137">將影片子串流混合到主要影片影像</span><span class="sxs-lookup"><span data-stu-id="f596e-137">Mixing video substreams onto the main video image</span></span>
-   <span data-ttu-id="f596e-138">色彩調整 (ProcAmp) 和影像篩選</span><span class="sxs-lookup"><span data-stu-id="f596e-138">Color adjustment (ProcAmp) and image filtering</span></span>
-   <span data-ttu-id="f596e-139">影像縮放比例</span><span class="sxs-lookup"><span data-stu-id="f596e-139">Image scaling</span></span>
-   <span data-ttu-id="f596e-140">色彩空間轉換</span><span class="sxs-lookup"><span data-stu-id="f596e-140">Color-space conversion</span></span>
-   <span data-ttu-id="f596e-141">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="f596e-141">Alpha blending</span></span>

<span data-ttu-id="f596e-142">下圖顯示影片處理管線中的階段。</span><span class="sxs-lookup"><span data-stu-id="f596e-142">The following diagram shows the stages in the video processing pipeline.</span></span> <span data-ttu-id="f596e-143">此圖表並非用來顯示實際的實作為。</span><span class="sxs-lookup"><span data-stu-id="f596e-143">The diagram is not meant to show an actual implementation.</span></span> <span data-ttu-id="f596e-144">例如，圖形驅動程式可能會將數個階段合併成單一作業。</span><span class="sxs-lookup"><span data-stu-id="f596e-144">For example, the graphics driver might combine several stages into a single operation.</span></span> <span data-ttu-id="f596e-145">所有這些作業都可以在視頻處理裝置的單一呼叫中執行。</span><span class="sxs-lookup"><span data-stu-id="f596e-145">All of these operations can be performed in a single call to the video processing device.</span></span> <span data-ttu-id="f596e-146">驅動程式可能不支援此處顯示的一些階段，例如雜訊和詳細資料篩選。</span><span class="sxs-lookup"><span data-stu-id="f596e-146">Some stages shown here, such as noise and detail filtering, might not be supported by the driver.</span></span>

![此圖顯示 dxva 影片處理的階段。](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

<span data-ttu-id="f596e-148">影片處理管線的輸入一律包含 *主要* 影片串流，其中包含主要影像資料。</span><span class="sxs-lookup"><span data-stu-id="f596e-148">The input to the video processing pipeline always includes a *primary* video stream, which contains the main image data.</span></span> <span data-ttu-id="f596e-149">主要影片串流決定輸出影片的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="f596e-149">The primary video stream determines the frame rate for the output video.</span></span> <span data-ttu-id="f596e-150">輸出影片的每個畫面格都會相對於主要影片串流的輸入資料進行計算。</span><span class="sxs-lookup"><span data-stu-id="f596e-150">Each frame of the output video is calculated relative to the input data from the primary video stream.</span></span> <span data-ttu-id="f596e-151">主要資料流程中的圖元一律是不透明的，不含每圖元的 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="f596e-151">Pixels in the primary stream are always opaque, with no per-pixel alpha data.</span></span> <span data-ttu-id="f596e-152">主要影片串流可以是漸進式或交錯式。</span><span class="sxs-lookup"><span data-stu-id="f596e-152">The primary video stream can be progressive or interlaced.</span></span>

<span data-ttu-id="f596e-153">（選擇性）影片處理管線最多可接收15個影片子串流。</span><span class="sxs-lookup"><span data-stu-id="f596e-153">Optionally, the video processing pipeline can receive up to 15 video substreams.</span></span> <span data-ttu-id="f596e-154">子資料流程包含輔助的影像資料，例如隱藏式輔助字幕或 DVD subpictures。</span><span class="sxs-lookup"><span data-stu-id="f596e-154">A substream contains auxiliary image data, such as closed captions or DVD subpictures.</span></span> <span data-ttu-id="f596e-155">這些影像會顯示在主要影片串流上，通常不會自行顯示。</span><span class="sxs-lookup"><span data-stu-id="f596e-155">These images are displayed over the primary video stream, and are generally not meant to be shown by themselves.</span></span> <span data-ttu-id="f596e-156">子資料流程圖片可以包含每圖元的 Alpha 資料，而且一律是漸進式的框架。</span><span class="sxs-lookup"><span data-stu-id="f596e-156">Substream pictures can contain per-pixel alpha data, and are always progressive frames.</span></span> <span data-ttu-id="f596e-157">影片處理裝置 Alpha-使用主要影片串流中的目前 deinterlaced 框架來混合子資料流程影像。</span><span class="sxs-lookup"><span data-stu-id="f596e-157">The video processing device alpha-blends the substream images with the current deinterlaced frame from the primary video stream.</span></span>

<span data-ttu-id="f596e-158">在本主題的其餘部分，將會使用「詞彙 *圖片* 」將輸入資料用於視頻處理裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-158">In the remainder of this topic, the term *picture* is used for the input data to a video processing device.</span></span> <span data-ttu-id="f596e-159">圖片可能由漸進式框架、單一欄位或兩個交錯欄位所組成。</span><span class="sxs-lookup"><span data-stu-id="f596e-159">A picture might consist of a progressive frame, a single field, or two interleaved fields.</span></span> <span data-ttu-id="f596e-160">輸出一律為 deinterlaced 的框架。</span><span class="sxs-lookup"><span data-stu-id="f596e-160">The output is always a deinterlaced frame.</span></span>

<span data-ttu-id="f596e-161">視頻驅動程式可以執行一個以上的影片處理裝置，以提供不同的影片處理功能組合。</span><span class="sxs-lookup"><span data-stu-id="f596e-161">A video driver can implement more than one video processing device, to provide different sets of video processing capabilities.</span></span> <span data-ttu-id="f596e-162">裝置是由 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="f596e-162">Devices are identified by GUID.</span></span> <span data-ttu-id="f596e-163">下列是預先定義的 Guid：</span><span class="sxs-lookup"><span data-stu-id="f596e-163">The following GUIDs are predefined:</span></span>

-   <span data-ttu-id="f596e-164">**DXVA2 \_VideoProcBobDevice**。</span><span class="sxs-lookup"><span data-stu-id="f596e-164">**DXVA2\_VideoProcBobDevice**.</span></span> <span data-ttu-id="f596e-165">此裝置會執行 bob 去交錯。</span><span class="sxs-lookup"><span data-stu-id="f596e-165">This device performs bob deinterlacing.</span></span>
-   <span data-ttu-id="f596e-166">**DXVA2 \_VideoProcProgressiveDevice**。</span><span class="sxs-lookup"><span data-stu-id="f596e-166">**DXVA2\_VideoProcProgressiveDevice**.</span></span> <span data-ttu-id="f596e-167">如果影片只包含漸進式框架，而沒有交錯框架，則會使用此裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-167">This device is used if the video contains only progressive frames, with no interlaced frames.</span></span> <span data-ttu-id="f596e-168"> (部分影片內容包含漸進和交錯框架的混合。</span><span class="sxs-lookup"><span data-stu-id="f596e-168">(Some video content contains a mix of progressive and interlaced frames.</span></span> <span data-ttu-id="f596e-169">漸進式裝置無法用於這種「混合」的影片內容，因為交錯框架需要去交錯步驟。 ) </span><span class="sxs-lookup"><span data-stu-id="f596e-169">The progressive device cannot be used for this kind of "mixed" video content, because a deinterlacing step is required for the interlaced frames.)</span></span>

<span data-ttu-id="f596e-170">每個支援 DXVA 視頻處理的圖形驅動程式都必須至少執行這兩個裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-170">Every graphics driver that supports DXVA video processing must implement at least these two devices.</span></span> <span data-ttu-id="f596e-171">圖形驅動程式也可以提供其他裝置，這些裝置是由驅動程式特定的 Guid 所識別。</span><span class="sxs-lookup"><span data-stu-id="f596e-171">The graphics driver may also provide other devices, which are identified by driver-specific GUIDs.</span></span> <span data-ttu-id="f596e-172">例如，驅動程式可能會執行專屬的去交錯演算法，產生比 bob 去交錯更優質的輸出。</span><span class="sxs-lookup"><span data-stu-id="f596e-172">For example, a driver might implement a proprietary deinterlacing algorithm that produces better quality output than bob deinterlacing.</span></span> <span data-ttu-id="f596e-173">某些去交錯演算法可能需要來自主要資料流程的向前或向後參考圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-173">Some deinterlacing algorithms may require forward or backward reference pictures from the primary stream.</span></span> <span data-ttu-id="f596e-174">如果是，呼叫端必須以正確的順序將這些圖片提供給驅動程式，如本節稍後所述。</span><span class="sxs-lookup"><span data-stu-id="f596e-174">If so, the caller must provide these pictures to the driver in the correct sequence, as described later in this section.</span></span>

<span data-ttu-id="f596e-175">也提供參考軟體裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-175">A reference software device is also provided.</span></span> <span data-ttu-id="f596e-176">軟體裝置已針對品質而非速度優化，而且可能不適合即時影片處理。</span><span class="sxs-lookup"><span data-stu-id="f596e-176">The software device is optimized for quality rather than speed, and may not be adequate for real-time video processing.</span></span> <span data-ttu-id="f596e-177">參考軟體裝置使用 GUID 值 DXVA2 \_ VideoProcSoftwareDevice。</span><span class="sxs-lookup"><span data-stu-id="f596e-177">The reference software device uses the GUID value DXVA2\_VideoProcSoftwareDevice.</span></span>

## <a name="creating-a-video-processing-device"></a><span data-ttu-id="f596e-178">建立視頻處理裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-178">Creating a Video Processing Device</span></span>

<span data-ttu-id="f596e-179">使用 DXVA 影片處理之前，應用程式必須建立影片處理裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-179">Before using DXVA video processing, the application must create a video processing device.</span></span> <span data-ttu-id="f596e-180">以下是步驟的簡短概述，本節的其餘部分將更詳細地說明這些步驟：</span><span class="sxs-lookup"><span data-stu-id="f596e-180">Here is a brief outline of the steps, which are explained in greater detail in the remainder of this section:</span></span>

1.  <span data-ttu-id="f596e-181">取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f596e-181">Get a pointer to the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface.</span></span>
2.  <span data-ttu-id="f596e-182">建立主要影片串流的影片格式描述。</span><span class="sxs-lookup"><span data-stu-id="f596e-182">Create a description of the video format for the primary video stream.</span></span> <span data-ttu-id="f596e-183">您可以使用此描述來取得支援影片格式的影片處理裝置清單。</span><span class="sxs-lookup"><span data-stu-id="f596e-183">Use this description to get a list of the video processing devices that support the video format.</span></span> <span data-ttu-id="f596e-184">裝置是由 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="f596e-184">Devices are identified by GUID.</span></span>
3.  <span data-ttu-id="f596e-185">針對特定裝置，取得裝置所支援的轉譯目標格式清單。</span><span class="sxs-lookup"><span data-stu-id="f596e-185">For a particular device, get a list of render-target formats supported by the device.</span></span> <span data-ttu-id="f596e-186">格式會以 **D3DFORMAT** 值清單的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="f596e-186">The formats are returned as a list of **D3DFORMAT** values.</span></span> <span data-ttu-id="f596e-187">如果您打算混合子串流，也可以取得一份支援的子串流格式清單。</span><span class="sxs-lookup"><span data-stu-id="f596e-187">If you plan to mix substreams, get a list of the supported substream formats as well.</span></span>
4.  <span data-ttu-id="f596e-188">查詢每個裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="f596e-188">Query the capabilities of each device.</span></span>
5.  <span data-ttu-id="f596e-189">建立影片處理裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-189">Create the video processing device.</span></span>

<span data-ttu-id="f596e-190">有時您可以省略這些步驟的其中一部分。</span><span class="sxs-lookup"><span data-stu-id="f596e-190">Sometimes you can omit some of these steps.</span></span> <span data-ttu-id="f596e-191">例如，您可以嘗試使用慣用的格式來建立影片處理裝置，並查看是否成功，而不是取得轉譯目標格式的清單。</span><span class="sxs-lookup"><span data-stu-id="f596e-191">For example, instead of getting the list of render-target formats, you could simply try creating the video processing device with your preferred format, and see if it succeeds.</span></span> <span data-ttu-id="f596e-192">常見的格式，例如 D3DFMT \_ X8R8G8B8 可能會成功。</span><span class="sxs-lookup"><span data-stu-id="f596e-192">A common format such as D3DFMT\_X8R8G8B8 is likely to succeed.</span></span>

<span data-ttu-id="f596e-193">本節的其餘部分將詳細說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="f596e-193">The remainder of this section describes these steps in detail.</span></span>

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a><span data-ttu-id="f596e-194">取得 IDirectXVideoProcessorService 指標</span><span class="sxs-lookup"><span data-stu-id="f596e-194">Get the IDirectXVideoProcessorService Pointer</span></span>

<span data-ttu-id="f596e-195">[**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)介面是從 Direct3D 裝置取得的。</span><span class="sxs-lookup"><span data-stu-id="f596e-195">The [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) interface is obtained from the Direct3D device.</span></span> <span data-ttu-id="f596e-196">有兩種方式可以取得這個介面的指標：</span><span class="sxs-lookup"><span data-stu-id="f596e-196">There are two ways to get a pointer to this interface:</span></span>

-   <span data-ttu-id="f596e-197">從 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-197">From a Direct3D device.</span></span>
-   <span data-ttu-id="f596e-198">從 [Direct3D 裝置管理員](direct3d-device-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="f596e-198">From the [Direct3D Device Manager](direct3d-device-manager.md).</span></span>

<span data-ttu-id="f596e-199">如果您有 Direct3D 裝置的指標，您可以藉由呼叫 [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice)函數來取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)指標。</span><span class="sxs-lookup"><span data-stu-id="f596e-199">If you have a pointer to a Direct3D device, you can get an [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer by calling the [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) function.</span></span> <span data-ttu-id="f596e-200">傳入裝置 **IDirect3DDevice9** 介面的指標，並針對 *Riid* 參數指定 **IID \_ IDirectXVideoProcessorService** ，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="f596e-200">Pass in a pointer to the device's **IDirect3DDevice9** interface, and specify **IID\_IDirectXVideoProcessorService** for the *riid* parameter, as shown in the following code:</span></span>


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



<span data-ttu-id="f596e-201">在某些情況下，一個物件會建立 Direct3D 裝置，然後透過 [Direct3D 裝置管理員](direct3d-device-manager.md)與其他物件共用它。</span><span class="sxs-lookup"><span data-stu-id="f596e-201">n some cases, one object creates the Direct3D device and then shares it with other objects through the [Direct3D Device Manager](direct3d-device-manager.md).</span></span> <span data-ttu-id="f596e-202">在此情況下，您可以在裝置管理員上呼叫 [**IDirect3DDeviceManager9：： GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) 來取得 [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) 指標，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="f596e-202">In this situation, you can call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) on the device manager to get the [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) pointer, as shown in the following code:</span></span>


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a><span data-ttu-id="f596e-203">列舉影片處理裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-203">Enumerate the Video Processing Devices</span></span>

<span data-ttu-id="f596e-204">若要取得影片處理裝置的清單，請使用主要影片串流的格式填入 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構，並將此結構傳遞至 [**IDirectXVideoProcessorService：： GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 方法。</span><span class="sxs-lookup"><span data-stu-id="f596e-204">To get a list of video processing devices, fill in a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure with the format of the primary video stream, and pass this structure to the [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method.</span></span> <span data-ttu-id="f596e-205">方法會傳回 Guid 的陣列，每個可搭配此影片格式使用的影片處理裝置都有一個。</span><span class="sxs-lookup"><span data-stu-id="f596e-205">The method returns an array of GUIDs, one for each video processing device that can be used with this video format.</span></span>

<span data-ttu-id="f596e-206">請考慮使用 YUY2 格式轉譯影片資料流程的應用程式，並使用709定義的 YUV 色彩，畫面播放速率為每秒29.97 個畫面格。</span><span class="sxs-lookup"><span data-stu-id="f596e-206">Consider an application that renders a video stream in YUY2 format, using the BT.709 definition of YUV color, with a frame rate of 29.97 frames per second.</span></span> <span data-ttu-id="f596e-207">假設影片內容完全由漸進式框架組成。</span><span class="sxs-lookup"><span data-stu-id="f596e-207">Assume that the video content consists entirely of progressive frames.</span></span> <span data-ttu-id="f596e-208">下列程式碼片段顯示如何填入格式描述，並取得裝置 Guid：</span><span class="sxs-lookup"><span data-stu-id="f596e-208">The following code fragment shows how to fill in the format description and get the device GUIDs:</span></span>


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



<span data-ttu-id="f596e-209">此範例的程式碼取自 [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-209">The code for this example is taken from the [DXVA2\_VideoProc](dxva2-videoproc-sample.md) SDK sample.</span></span>

<span data-ttu-id="f596e-210">此範例中的 *pGuids* 陣列是由 [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 方法配置，因此應用程式必須藉由呼叫 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放陣列。</span><span class="sxs-lookup"><span data-stu-id="f596e-210">The *pGuids* array in this example is allocated by the [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) method, so the application must free the array by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="f596e-211">您可以使用這個方法所傳回的任何裝置 Guid 來執行其餘步驟。</span><span class="sxs-lookup"><span data-stu-id="f596e-211">The remaining steps can be performed using any of the device GUIDs returned by this method.</span></span>

### <a name="enumerate-render-target-formats"></a><span data-ttu-id="f596e-212">列舉 Render-Target 格式</span><span class="sxs-lookup"><span data-stu-id="f596e-212">Enumerate Render-Target Formats</span></span>

<span data-ttu-id="f596e-213">若要取得裝置支援的轉譯目標格式清單，請將裝置 GUID 和 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構傳遞至 [**IDirectXVideoProcessorService：： GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) 方法，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="f596e-213">To get the list of render-target formats supported by the device, pass the device GUID and the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure to the [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) method, as shown in the following code:</span></span>


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="f596e-214">方法會傳回 **D3DFORMAT** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="f596e-214">The method returns an array of **D3DFORMAT** values.</span></span> <span data-ttu-id="f596e-215">在此範例中，輸入類型是 YUY2，一般格式清單可能是 D3DFMT \_ X8R8G8B8 (32 位 RGB) 和 D3DMFT \_ YUY2 (輸入格式) 。</span><span class="sxs-lookup"><span data-stu-id="f596e-215">In this example, where the input type is YUY2, a typical list of formats might be D3DFMT\_X8R8G8B8 (32-bit RGB) and D3DMFT\_YUY2 (the input format).</span></span> <span data-ttu-id="f596e-216">不過，確切的清單將取決於驅動程式。</span><span class="sxs-lookup"><span data-stu-id="f596e-216">However, the exact list will depend on the driver.</span></span>

<span data-ttu-id="f596e-217">子串流的可用格式清單會根據轉譯目標格式和輸入格式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f596e-217">The list of available formats for the substreams can vary depending on the render-target format and the input format.</span></span> <span data-ttu-id="f596e-218">若要取得子串流格式的清單，請將裝置 GUID、格式結構和轉譯目標格式傳遞給 [**IDirectXVideoProcessorService：： GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) 方法，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="f596e-218">To get the list of substream formats, pass the device GUID, the format structure, and the render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) method, as shown in the following code:</span></span>


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



<span data-ttu-id="f596e-219">這個方法會傳回另一個 **D3DFORMAT** 值陣列。</span><span class="sxs-lookup"><span data-stu-id="f596e-219">This method returns another array of **D3DFORMAT** values.</span></span> <span data-ttu-id="f596e-220">一般的子串流格式為 AYUV 和 AI44。</span><span class="sxs-lookup"><span data-stu-id="f596e-220">Typical substream formats are AYUV and AI44.</span></span>

### <a name="query-the-device-capabilities"></a><span data-ttu-id="f596e-221">查詢裝置功能</span><span class="sxs-lookup"><span data-stu-id="f596e-221">Query the Device Capabilities</span></span>

<span data-ttu-id="f596e-222">若要取得特定裝置的功能，請將裝置 GUID、格式結構和轉譯目標格式傳遞給 [**IDirectXVideoProcessorService：： GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) 方法。</span><span class="sxs-lookup"><span data-stu-id="f596e-222">To get the capabilities of a particular device, pass the device GUID, the format structure, and a render-target format to the [**IDirectXVideoProcessorService::GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) method.</span></span> <span data-ttu-id="f596e-223">方法會以裝置功能填入 [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) 結構結構。</span><span class="sxs-lookup"><span data-stu-id="f596e-223">The method fills in a [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure structure with the device capabilities.</span></span>


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a><span data-ttu-id="f596e-224">建立裝置</span><span class="sxs-lookup"><span data-stu-id="f596e-224">Create the Device</span></span>

<span data-ttu-id="f596e-225">若要建立影片處理裝置，請呼叫 [**IDirectXVideoProcessorService：： CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor)。</span><span class="sxs-lookup"><span data-stu-id="f596e-225">To create the video processing device, call [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor).</span></span> <span data-ttu-id="f596e-226">此方法的輸入是裝置 GUID、格式描述、轉譯目標格式，以及您打算混合的子串流數目上限。</span><span class="sxs-lookup"><span data-stu-id="f596e-226">The input to this method is the device GUID, the format description, the render-target format, and the maximum number of substreams that you plan to mix.</span></span> <span data-ttu-id="f596e-227">方法會傳回 [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) 介面的指標，該介面表示影片處理裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-227">The method returns a pointer to the [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) interface, which represents the video processing device.</span></span>


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a><span data-ttu-id="f596e-228">影片流程 Array.blit</span><span class="sxs-lookup"><span data-stu-id="f596e-228">Video Process Blit</span></span>

<span data-ttu-id="f596e-229">主要的影片處理作業是 *影片處理 array.blit*。</span><span class="sxs-lookup"><span data-stu-id="f596e-229">The main video processing operation is the *video processing blit*.</span></span> <span data-ttu-id="f596e-230"> (*array.blit* 是將兩個或多個點陣圖組合成單一點陣圖的任何作業。</span><span class="sxs-lookup"><span data-stu-id="f596e-230">(A *blit* is any operation that combines two or more bitmaps into a single bitmap.</span></span> <span data-ttu-id="f596e-231">影片處理 array.blit 會結合輸入圖片以建立輸出框架。 ) 若要執行影片處理 array.blit，請呼叫 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)。</span><span class="sxs-lookup"><span data-stu-id="f596e-231">A video processing blit combines input pictures to create an output frame.) To perform a video processing blit, call [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="f596e-232">這個方法會將一組影片範例傳遞給影片處理裝置。</span><span class="sxs-lookup"><span data-stu-id="f596e-232">This method passes a set of video samples to the video processing device.</span></span> <span data-ttu-id="f596e-233">在回應中，影片處理裝置會處理輸入圖片並產生一個輸出畫面格。</span><span class="sxs-lookup"><span data-stu-id="f596e-233">In response, the video processing device processes the input pictures and generates one output frame.</span></span> <span data-ttu-id="f596e-234">處理可能包括去交錯、色彩空間轉換和子流混合。</span><span class="sxs-lookup"><span data-stu-id="f596e-234">Processing can include deinterlacing, color-space conversion, and substream mixing.</span></span> <span data-ttu-id="f596e-235">輸出會寫入至呼叫端所提供的目的介面。</span><span class="sxs-lookup"><span data-stu-id="f596e-235">The output is written to a destination surface provided by the caller.</span></span>

<span data-ttu-id="f596e-236">[**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="f596e-236">The [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method takes the following parameters:</span></span>

-   <span data-ttu-id="f596e-237">*pRT* 會指向 **IDirect3DSurface9** 轉譯目標介面，以接收已處理的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f596e-237">*pRT* points to an **IDirect3DSurface9** render target surface that will receive the processed video frame.</span></span>
-   <span data-ttu-id="f596e-238">*pBltParams* 會指向指定 array.blit 參數的 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構。</span><span class="sxs-lookup"><span data-stu-id="f596e-238">*pBltParams* points to a [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure that specifies the parameters for the blit.</span></span>
-   <span data-ttu-id="f596e-239">*pSamples* 是 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) 結構陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="f596e-239">*pSamples* is the address of an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="f596e-240">這些結構包含 array.blit 的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-240">These structures contain the input samples for the blit.</span></span>
-   <span data-ttu-id="f596e-241">*NumSamples* 會提供 *pSamples* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="f596e-241">*NumSamples* gives the size of the *pSamples* array.</span></span>
-   <span data-ttu-id="f596e-242">*保留* 的參數是保留的，而且應該設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f596e-242">The *Reserved* parameter is reserved and should be set to **NULL**.</span></span>

<span data-ttu-id="f596e-243">在 *pSamples* 陣列中，呼叫端必須提供下列輸入範例：</span><span class="sxs-lookup"><span data-stu-id="f596e-243">In the *pSamples* array, the caller must provide the following input samples:</span></span>

-   <span data-ttu-id="f596e-244">主要影片資料流程中目前的圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-244">The current picture from the primary video stream.</span></span>
-   <span data-ttu-id="f596e-245">向前及向後參考圖片（如果去交錯演算法有需要）。</span><span class="sxs-lookup"><span data-stu-id="f596e-245">Forward and backward reference pictures, if required by the deinterlacing algorithm.</span></span>
-   <span data-ttu-id="f596e-246">零或多個子串流圖片，最多可達15子串流。</span><span class="sxs-lookup"><span data-stu-id="f596e-246">Zero or more substream pictures, up to a maximum of 15 substreams.</span></span>

<span data-ttu-id="f596e-247">驅動程式預期此陣列是以特定順序排列，如 [輸入範例順序](#input-sample-order)中所述。</span><span class="sxs-lookup"><span data-stu-id="f596e-247">The driver expects this array to be in a particular order, as described in [Input Sample Order](#input-sample-order).</span></span>

### <a name="blit-parameters"></a><span data-ttu-id="f596e-248">Array.blit 參數</span><span class="sxs-lookup"><span data-stu-id="f596e-248">Blit Parameters</span></span>

<span data-ttu-id="f596e-249">[**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams)結構包含 array.blit 的一般參數。</span><span class="sxs-lookup"><span data-stu-id="f596e-249">The [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure contains general parameters for the blit.</span></span> <span data-ttu-id="f596e-250">最重要的參數會儲存在下列結構的成員中：</span><span class="sxs-lookup"><span data-stu-id="f596e-250">The most important parameters are stored in the following members of the structure:</span></span>

-   <span data-ttu-id="f596e-251">**TargetFrame** 是輸出框架的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-251">**TargetFrame** is the presentation time of the output frame.</span></span> <span data-ttu-id="f596e-252">針對漸進式內容，這次必須等於主要影片資料流程中目前框架的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-252">For progressive content, this time must equal the start time for the current frame from the primary video stream.</span></span> <span data-ttu-id="f596e-253">這段時間是在該輸入範例的 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **Start** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="f596e-253">This time is specified in the **Start** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure for that input sample.</span></span>

    <span data-ttu-id="f596e-254">針對交錯式內容，有兩個交錯欄位的框架會產生兩個 deinterlaced 輸出畫面格。</span><span class="sxs-lookup"><span data-stu-id="f596e-254">For interlaced content, a frame with two interleaved fields produces two deinterlaced output frames.</span></span> <span data-ttu-id="f596e-255">在第一個輸出框架上，表示時間必須等於主要影片資料流程中目前圖片的開始時間，就像漸進式內容一樣。</span><span class="sxs-lookup"><span data-stu-id="f596e-255">On the first output frame, the presentation time must equal the start time of the current picture in the primary video stream, just like progressive content.</span></span> <span data-ttu-id="f596e-256">在第二個輸出框架上，開始時間必須等於主要影片資料流程中目前圖片的開始時間，以及資料流程中下一張圖片的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-256">On the second output frame, the start time must equal the midpoint between the start time of the current picture in the primary video stream and the start time of the next picture in the stream.</span></span> <span data-ttu-id="f596e-257">例如，如果輸入影片是每秒25個畫面格 (每秒50個欄位) ，則輸出畫面將會有下表中顯示的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f596e-257">For example, if the input video is 25 frames per second (50 fields per second), the output frames will have the time stamps shown in the following table.</span></span> <span data-ttu-id="f596e-258">時間戳記會以100毫微秒的單位顯示。</span><span class="sxs-lookup"><span data-stu-id="f596e-258">Time stamps are shown in units of 100 nanoseconds.</span></span>

    

    | <span data-ttu-id="f596e-259">輸入圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-259">Input picture</span></span> | <span data-ttu-id="f596e-260">**TargetFrame** (1) </span><span class="sxs-lookup"><span data-stu-id="f596e-260">**TargetFrame** (1)</span></span> | <span data-ttu-id="f596e-261">**TargetFrame** (2) </span><span class="sxs-lookup"><span data-stu-id="f596e-261">**TargetFrame** (2)</span></span> |
    |---------------|---------------------|---------------------|
    | <span data-ttu-id="f596e-262">0</span><span class="sxs-lookup"><span data-stu-id="f596e-262">0</span></span>             | <span data-ttu-id="f596e-263">0</span><span class="sxs-lookup"><span data-stu-id="f596e-263">0</span></span>                   | <span data-ttu-id="f596e-264">200000</span><span class="sxs-lookup"><span data-stu-id="f596e-264">200000</span></span>              |
    | <span data-ttu-id="f596e-265">400000</span><span class="sxs-lookup"><span data-stu-id="f596e-265">400000</span></span>        | <span data-ttu-id="f596e-266">0</span><span class="sxs-lookup"><span data-stu-id="f596e-266">0</span></span>                   | <span data-ttu-id="f596e-267">600000</span><span class="sxs-lookup"><span data-stu-id="f596e-267">600000</span></span>              |
    | <span data-ttu-id="f596e-268">800000</span><span class="sxs-lookup"><span data-stu-id="f596e-268">800000</span></span>        | <span data-ttu-id="f596e-269">800000</span><span class="sxs-lookup"><span data-stu-id="f596e-269">800000</span></span>              | <span data-ttu-id="f596e-270">1000000</span><span class="sxs-lookup"><span data-stu-id="f596e-270">1000000</span></span>             |
    | <span data-ttu-id="f596e-271">1200000</span><span class="sxs-lookup"><span data-stu-id="f596e-271">1200000</span></span>       | <span data-ttu-id="f596e-272">1200000</span><span class="sxs-lookup"><span data-stu-id="f596e-272">1200000</span></span>             | <span data-ttu-id="f596e-273">1400000</span><span class="sxs-lookup"><span data-stu-id="f596e-273">1400000</span></span>             |

    

     

    <span data-ttu-id="f596e-274">如果交錯的內容是由單一欄位而非交錯欄位所組成，則輸出時間一律會符合輸入時間，如同漸進式內容一樣。</span><span class="sxs-lookup"><span data-stu-id="f596e-274">If interlaced content consists of single fields rather than interleaved fields, the output times always match the input times, as with progressive content.</span></span>

-   <span data-ttu-id="f596e-275">**TargetRect** 會定義目的介面內的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-275">**TargetRect** defines a rectangular region within the destination surface.</span></span> <span data-ttu-id="f596e-276">Array.blit 會將輸出寫入此區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-276">The blit will write the output to this region.</span></span> <span data-ttu-id="f596e-277">具體來說， **TargetRect** 內的每個圖元都會修改，而且不會修改 **TargetRect** 以外的任何圖元。</span><span class="sxs-lookup"><span data-stu-id="f596e-277">Specifically, every pixel inside **TargetRect** will be modified, and no pixels outside of **TargetRect** will be modified.</span></span> <span data-ttu-id="f596e-278">目標矩形會定義所有輸入影片資料流程的周框。</span><span class="sxs-lookup"><span data-stu-id="f596e-278">The target rectangle defines the bounding rectangle for all of the input video streams.</span></span> <span data-ttu-id="f596e-279">在該矩形內放置個別資料流程是透過 [**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)的 *pSamples* 參數來控制。</span><span class="sxs-lookup"><span data-stu-id="f596e-279">Placement of individual streams within that rectangle is controlled through the *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span>
-   <span data-ttu-id="f596e-280">**BackgroundColor** 會提供背景的色彩，而不會顯示任何影片影像。</span><span class="sxs-lookup"><span data-stu-id="f596e-280">**BackgroundColor** gives the color of the background wherever no video image appears.</span></span> <span data-ttu-id="f596e-281">例如，當 16 x 9 的影片影像顯示在 4 x 3 區域內時 (上下黑邊縮) ，letterboxed 區域會以背景色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="f596e-281">For example, when a 16 x 9 video image is displayed within a 4 x 3 area (letterboxing), the letterboxed regions are displayed with the background color.</span></span> <span data-ttu-id="f596e-282">背景色彩只適用于 (**TargetRect**) 的目標矩形內。</span><span class="sxs-lookup"><span data-stu-id="f596e-282">The background color applies only within the target rectangle (**TargetRect**).</span></span> <span data-ttu-id="f596e-283">**TargetRect** 之外的任何圖元都不會修改。</span><span class="sxs-lookup"><span data-stu-id="f596e-283">Any pixels outside of **TargetRect** are not modified.</span></span>
-   <span data-ttu-id="f596e-284">**DestFormat** 描述輸出影片的色彩空間，例如，是否使用 Itu-t-R BT. 709 或 BT. 601 color。</span><span class="sxs-lookup"><span data-stu-id="f596e-284">**DestFormat** describes the color space for the output video—for example, whether ITU-R BT.709 or BT.601 color is used.</span></span> <span data-ttu-id="f596e-285">這項資訊會影響影像的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="f596e-285">This information can affect how the image is displayed.</span></span> <span data-ttu-id="f596e-286">如需詳細資訊，請參閱 [擴充色彩資訊](extended-color-information.md)。</span><span class="sxs-lookup"><span data-stu-id="f596e-286">For more information, see [Extended Color Information](extended-color-information.md).</span></span>

<span data-ttu-id="f596e-287">其他參數則會在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構的參考頁面上說明。</span><span class="sxs-lookup"><span data-stu-id="f596e-287">Other parameters are described on the reference page for the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="input-samples"></a><span data-ttu-id="f596e-288">輸入範例</span><span class="sxs-lookup"><span data-stu-id="f596e-288">Input Samples</span></span>

<span data-ttu-id="f596e-289">[**IDirectXVideoProcessor：： VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)的 *pSamples* 參數會指向 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="f596e-289">The *pSamples* parameter of [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) points to an array of [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structures.</span></span> <span data-ttu-id="f596e-290">其中每個結構都包含一個輸入範例的相關資訊，以及包含範例的 Direct3D 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f596e-290">Each of these structures contains information about one input sample and a pointer to the Direct3D surface that contains the sample.</span></span> <span data-ttu-id="f596e-291">每個範例都是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="f596e-291">Each sample is one of the following:</span></span>

-   <span data-ttu-id="f596e-292">主要資料流程中目前的圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-292">The current picture from the primary stream.</span></span>
-   <span data-ttu-id="f596e-293">主要資料流程的向前或向後參考圖片，用於去交錯。</span><span class="sxs-lookup"><span data-stu-id="f596e-293">A forward or backward reference picture from the primary stream, used for deinterlacing.</span></span>
-   <span data-ttu-id="f596e-294">子流圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-294">A substream picture.</span></span>

<span data-ttu-id="f596e-295">範例必須出現在陣列中的確切順序，稍後會在 [ [輸入範例順序](#input-sample-order)] 區段中描述。</span><span class="sxs-lookup"><span data-stu-id="f596e-295">The exact order in which the samples must appear in the array is described later, in the section [Input Sample Order](#input-sample-order).</span></span>

<span data-ttu-id="f596e-296">雖然大部分的影片應用程式最多隻需要一個子串流，但可以提供最多15個子流圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-296">Up to 15 substream pictures can be provided, although most video applications need only one substream, at the most.</span></span> <span data-ttu-id="f596e-297">每次呼叫 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)時，子串流的數目可能會變更。</span><span class="sxs-lookup"><span data-stu-id="f596e-297">The number of substreams can change with each call to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).</span></span> <span data-ttu-id="f596e-298">子流圖片的表示方式是將 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **SampleFormat** 成員設定為等於 DXVA2 \_ SampleSubStream。</span><span class="sxs-lookup"><span data-stu-id="f596e-298">Substream pictures are indicated by setting the **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure equal to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="f596e-299">針對主要影片串流，此成員描述輸入影片的交錯。</span><span class="sxs-lookup"><span data-stu-id="f596e-299">For the primary video stream, this member describes the interlacing of the input video.</span></span> <span data-ttu-id="f596e-300">如需詳細資訊，請參閱 [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) 列舉。</span><span class="sxs-lookup"><span data-stu-id="f596e-300">For more information, see [**DXVA2\_SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) enumeration.</span></span>

<span data-ttu-id="f596e-301">針對主要影片資料流程， [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **開頭** 和 **結尾** 成員會提供輸入範例的開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-301">For the primary video stream, the **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the start and end times of the input sample.</span></span> <span data-ttu-id="f596e-302">針對子資料流程圖片，將這些值設定為零，因為呈現時間一律會從主要資料流程計算。</span><span class="sxs-lookup"><span data-stu-id="f596e-302">For substream pictures, set these values to zero, because the presentation time is always calculated from the primary stream.</span></span> <span data-ttu-id="f596e-303">應用程式會負責追蹤每個子串流圖片應該呈現的時間，並在適當的時間將其提交至 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 。</span><span class="sxs-lookup"><span data-stu-id="f596e-303">The application is responsible for tracking when each substream picture should be presented and submitting it to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) at the proper time.</span></span>

<span data-ttu-id="f596e-304">兩個矩形會定義每個串流的來源影片位置：</span><span class="sxs-lookup"><span data-stu-id="f596e-304">Two rectangles define how the source video is positioned for each stream:</span></span>

-   <span data-ttu-id="f596e-305">[**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **>srcrect** 成員會指定 *來源矩形*，也就是要出現在複合輸出框架中的來源圖片矩形區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-305">The **SrcRect** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure specifies the *source rectangle*, a rectangular region of the source picture that will appear in the composited output frame.</span></span> <span data-ttu-id="f596e-306">若要裁剪圖片，請將此值設定為小於框架大小的值。</span><span class="sxs-lookup"><span data-stu-id="f596e-306">To crop the picture, set this to a value smaller than the frame size.</span></span> <span data-ttu-id="f596e-307">否則，請將它設定為等於框架大小。</span><span class="sxs-lookup"><span data-stu-id="f596e-307">Otherwise, set it equal to the frame size.</span></span>
-   <span data-ttu-id="f596e-308">相同結構的 **>dstrect** 成員會指定 *目的地矩形*，也就是顯示影片框架的目的介面矩形區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-308">The **DstRect** member of the same structure specifies the *destination rectangle*, a rectangular region of the destination surface where the video frame will appear.</span></span>

<span data-ttu-id="f596e-309">驅動程式會 blits 從來源矩形到目的矩形的圖元。</span><span class="sxs-lookup"><span data-stu-id="f596e-309">The driver blits pixels from the source rectangle into the destination rectangle.</span></span> <span data-ttu-id="f596e-310">這兩個矩形可以有不同的大小或外觀比例;驅動程式會視需要調整映射。</span><span class="sxs-lookup"><span data-stu-id="f596e-310">The two rectangles can have different sizes or aspect ratios; the driver will scale the image as needed.</span></span> <span data-ttu-id="f596e-311">此外，每個輸入資料流程都可以使用不同的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="f596e-311">Moreover, each input stream can use a different scaling factor.</span></span> <span data-ttu-id="f596e-312">事實上，您可能需要進行調整，才能在輸出框架中產生正確的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f596e-312">In fact, scaling might be necessary to produce the correct aspect ratio in the output frame.</span></span> <span data-ttu-id="f596e-313">驅動程式不會將來源的圖元外觀比例納入考慮，因此，如果來源影像使用非正方形圖元，則應用程式會由應用程式計算正確的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="f596e-313">The driver does not take the source's pixel aspect ratio into account, so if the source image uses non-square pixels, it is up to the application to calculate the correct destination rectangle.</span></span>

<span data-ttu-id="f596e-314">慣用的子流格式為 AYUV 和 AI44。</span><span class="sxs-lookup"><span data-stu-id="f596e-314">The preferred substream formats are AYUV and AI44.</span></span> <span data-ttu-id="f596e-315">後者是具有16色的 palletized 格式。</span><span class="sxs-lookup"><span data-stu-id="f596e-315">The latter is a palletized format with 16 colors.</span></span> <span data-ttu-id="f596e-316">在 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **Pal** 成員中指定了調色板專案。</span><span class="sxs-lookup"><span data-stu-id="f596e-316">Palette entries are specified in the **Pal** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span> <span data-ttu-id="f596e-317"> (如果您的來源影片格式原本是以媒體基礎媒體類型表示，則會將調色板專案儲存在 [**MF \_ MT \_**](mf-mt-palette-attribute.md) 選擇區屬性中。 ) 非 palletized 格式，請將此陣列清除為零。</span><span class="sxs-lookup"><span data-stu-id="f596e-317">(If your source video format is originally expressed as a Media Foundation media type, the palette entries are stored in the [**MF\_MT\_PALETTE**](mf-mt-palette-attribute.md) attribute.) For non-palletized formats, clear this array to zero.</span></span>

## <a name="image-composition"></a><span data-ttu-id="f596e-318">影像組合</span><span class="sxs-lookup"><span data-stu-id="f596e-318">Image Composition</span></span>

<span data-ttu-id="f596e-319">每個 array.blit 作業都是由下列三個矩形所定義：</span><span class="sxs-lookup"><span data-stu-id="f596e-319">Every blit operation is defined by the following three rectangles:</span></span>

-   <span data-ttu-id="f596e-320">*目標* 矩形 (**TargetRect**) 會定義要顯示輸出的目的介面內的區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-320">The *target* rectangle (**TargetRect**) defines the region within the destination surface where the output will appear.</span></span> <span data-ttu-id="f596e-321">輸出影像會裁剪到這個矩形。</span><span class="sxs-lookup"><span data-stu-id="f596e-321">The output image is clipped to this rectangle.</span></span>
-   <span data-ttu-id="f596e-322">每個資料流程 (**>dstrect**) 的 *目的地* 矩形會定義輸入資料流程出現在複合影像中的位置。</span><span class="sxs-lookup"><span data-stu-id="f596e-322">The *destination* rectangle for each stream (**DstRect**) defines where the input stream appears in the composited image.</span></span>
-   <span data-ttu-id="f596e-323">每個資料流程 (**>srcrect**) 的 *來源* 矩形會定義要顯示的來源影像部分。</span><span class="sxs-lookup"><span data-stu-id="f596e-323">The *source* rectangle for each stream (**SrcRect**) defines which part of the source image appears.</span></span>

<span data-ttu-id="f596e-324">目標和目的地矩形會指定為相對於目的地介面。</span><span class="sxs-lookup"><span data-stu-id="f596e-324">The target and destination rectangles are specified relative to the destination surface.</span></span> <span data-ttu-id="f596e-325">會指定相對於來源影像的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="f596e-325">The source rectangle is specified relative to the source image.</span></span> <span data-ttu-id="f596e-326">所有矩形都會以圖元為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="f596e-326">All rectangles are specified in pixels.</span></span>

![顯示來源、目的地和目標矩形的圖表](images/dxva-vp-rects.gif)

<span data-ttu-id="f596e-328">影片處理裝置 Alpha 會使用下列任何一種 Alpha 資料來源來混合輸入圖片：</span><span class="sxs-lookup"><span data-stu-id="f596e-328">The video processing device alpha blends the input pictures, using any of the following sources of alpha data:</span></span>

-   <span data-ttu-id="f596e-329">來自子串流的每圖元 Alpha 資料。</span><span class="sxs-lookup"><span data-stu-id="f596e-329">Per-pixel alpha data from substreams.</span></span>
-   <span data-ttu-id="f596e-330">每個影片資料流程的平面 Alpha 值，指定于 [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **PlanarAlpha** 成員中。</span><span class="sxs-lookup"><span data-stu-id="f596e-330">A planar alpha value for each video stream, specified in the **PlanarAlpha** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure.</span></span>
-   <span data-ttu-id="f596e-331">複合影像的平面 Alpha 值，在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams)結構的 **Alpha** 成員中指定。</span><span class="sxs-lookup"><span data-stu-id="f596e-331">The planar alpha value of the composited image, specified in the **Alpha** member of the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span> <span data-ttu-id="f596e-332">這個值是用來 blend 整個合成影像與背景色彩。</span><span class="sxs-lookup"><span data-stu-id="f596e-332">This value is used to blend the entire composited image with the background color.</span></span>

<span data-ttu-id="f596e-333">本節提供一系列示範影片處理裝置如何建立輸出影像的範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-333">This section gives a series of examples that show how the video processing device creates the output image.</span></span>

### <a name="example-1-letterboxing"></a><span data-ttu-id="f596e-334">範例1：上下黑邊縮</span><span class="sxs-lookup"><span data-stu-id="f596e-334">Example 1: Letterboxing</span></span>

<span data-ttu-id="f596e-335">此範例示範如何將目的矩形設定為小於目標矩形，以黑邊來源影像。</span><span class="sxs-lookup"><span data-stu-id="f596e-335">This example shows how to letterbox the source image, by setting the destination rectangle to be smaller than the target rectangle.</span></span> <span data-ttu-id="f596e-336">此範例中的主要影片串流是720×480影像，而且應以16:9 外觀比例顯示。</span><span class="sxs-lookup"><span data-stu-id="f596e-336">The primary video stream in this example is a 720 × 480 image, and is meant to be displayed at a 16:9 aspect ratio.</span></span> <span data-ttu-id="f596e-337">目的地介面為640×480圖元 (4:3 外觀比例) 。</span><span class="sxs-lookup"><span data-stu-id="f596e-337">The destination surface is 640 × 480 pixels (4:3 aspect ratio).</span></span> <span data-ttu-id="f596e-338">若要達到正確的外觀比例，目的地矩形必須是640×360。</span><span class="sxs-lookup"><span data-stu-id="f596e-338">To achieve the correct aspect ratio, the destination rectangle must be 640 × 360.</span></span> <span data-ttu-id="f596e-339">為了簡單起見，此範例不包含子流。</span><span class="sxs-lookup"><span data-stu-id="f596e-339">For simplicity, this example does not include a substream.</span></span> <span data-ttu-id="f596e-340">下圖顯示來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="f596e-340">The following diagram shows the source and destination rectangles.</span></span>

![顯示上下黑邊縮的圖表。](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

<span data-ttu-id="f596e-342">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-342">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-343">目標矩形： {0，0，640，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-343">Target rectangle: { 0, 0, 640, 480 }</span></span>
-   <span data-ttu-id="f596e-344">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-344">Primary video:</span></span>

    -   <span data-ttu-id="f596e-345">來源矩形： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-345">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-346">目的地矩形： {0，60，640，420}</span><span class="sxs-lookup"><span data-stu-id="f596e-346">Destination rectangle: { 0, 60, 640, 420 }</span></span>

<span data-ttu-id="f596e-347">驅動程式會將影片進行逐行轉換，將 deinterlaced 框架壓縮成640×360，然後將框架 array.blit 到目的地矩形中。</span><span class="sxs-lookup"><span data-stu-id="f596e-347">The driver will deinterlace the video, shrink the deinterlaced frame to 640 × 360, and blit the frame into the destination rectangle.</span></span> <span data-ttu-id="f596e-348">目標矩形大於目的矩形，因此驅動程式會使用背景色彩來填滿框架上方和下方的水準列。</span><span class="sxs-lookup"><span data-stu-id="f596e-348">The target rectangle is larger than the destination rectangle, so the driver will use the background color to fill the horizontal bars above and below the frame.</span></span> <span data-ttu-id="f596e-349">背景色彩是在 [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) 結構中指定的。</span><span class="sxs-lookup"><span data-stu-id="f596e-349">The background color is specified in the [**DXVA2\_VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) structure.</span></span>

### <a name="example-2-stretching-substream-images"></a><span data-ttu-id="f596e-350">範例2：延展子串流映射</span><span class="sxs-lookup"><span data-stu-id="f596e-350">Example 2: Stretching Substream Images</span></span>

<span data-ttu-id="f596e-351">子串流圖片可延伸至主要的影片圖片之外。</span><span class="sxs-lookup"><span data-stu-id="f596e-351">Substream pictures can extend beyond the primary video picture.</span></span> <span data-ttu-id="f596e-352">例如，在 DVD video 中，主要影片串流在子資料流程為16:9 時可能會有4:3 的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="f596e-352">In DVD video, for example, the primary video stream can have a 4:3 aspect ratio while the substream is 16:9.</span></span> <span data-ttu-id="f596e-353">在此範例中，兩個影片串流都有相同的來源維度 (720 × 480) ，但子資料流程的設計是以16:9 的外觀比例顯示。</span><span class="sxs-lookup"><span data-stu-id="f596e-353">In this example, both video streams have the same source dimensions (720 × 480), but the substream is intended to be shown at a 16:9 aspect ratio.</span></span> <span data-ttu-id="f596e-354">為了達到此長寬比，子串流影像會水準伸展。</span><span class="sxs-lookup"><span data-stu-id="f596e-354">To achieve this aspect ratio, the substream image is stretched horizontally.</span></span> <span data-ttu-id="f596e-355">來源和目的地矩形如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-355">The source and destination rectangles are shown in the following diagram.</span></span>

![顯示子流影像延展的圖表。](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

<span data-ttu-id="f596e-357">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-357">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-358">目標矩形： {0，0，854，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-358">Target rectangle: { 0, 0, 854, 480 }</span></span>
-   <span data-ttu-id="f596e-359">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-359">Primary video:</span></span>

    -   <span data-ttu-id="f596e-360">來源矩形： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-360">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-361">目的地矩形： {0，107，474，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-361">Destination rectangle: { 0, 107, 474, 480 }</span></span>

-   <span data-ttu-id="f596e-362">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-362">Substream:</span></span>
    -   <span data-ttu-id="f596e-363">來源矩形： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-363">Source rectangle: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-364">目的地矩形： {0，0，854，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-364">Destination rectangle: { 0, 0, 854, 480 }</span></span>

<span data-ttu-id="f596e-365">這些值會保留影像高度，並以水準方式調整影像的大小。</span><span class="sxs-lookup"><span data-stu-id="f596e-365">These values preserve the image height and scale both images horizontally.</span></span> <span data-ttu-id="f596e-366">在兩張影像顯示的區域中，它們都是以 Alpha 混合。</span><span class="sxs-lookup"><span data-stu-id="f596e-366">In the regions where both images appear, they are alpha blended.</span></span> <span data-ttu-id="f596e-367">子串流圖片 exends 超過 primay 影片，而子串流則是使用背景色彩來混合使用 Alpha。</span><span class="sxs-lookup"><span data-stu-id="f596e-367">Where the substream picture exends beyond the primay video, the substream is alpha blended with the background color.</span></span> <span data-ttu-id="f596e-368">此 Alpha 混合帳戶會在圖表右手邊改變色彩。</span><span class="sxs-lookup"><span data-stu-id="f596e-368">This alpha blending accounts for the altered colors in the right-hand side of the diagram.</span></span>

### <a name="example-3-mismatched-stream-heights"></a><span data-ttu-id="f596e-369">範例3：不相符的資料流程高度</span><span class="sxs-lookup"><span data-stu-id="f596e-369">Example 3: Mismatched Stream Heights</span></span>

<span data-ttu-id="f596e-370">在上述範例中，子資料流程和主要資料流程的高度相同。</span><span class="sxs-lookup"><span data-stu-id="f596e-370">In the previous example, the substream and the primary stream are the same height.</span></span> <span data-ttu-id="f596e-371">資料流程也可以有不相符的高度，如這個範例所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-371">Streams can also have mismatched heights, as shown in this example.</span></span> <span data-ttu-id="f596e-372">目標矩形內不會顯示任何影片的區域會使用背景色彩來繪製（在此範例中為黑色）。</span><span class="sxs-lookup"><span data-stu-id="f596e-372">Areas within the target rectangle where no video appears are drawn using the background color—black in this example.</span></span> <span data-ttu-id="f596e-373">來源和目的地矩形如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-373">The source and destination rectangles are shown in the following diagram.</span></span>

![顯示不相符之資料流程高度的圖表](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

<span data-ttu-id="f596e-375">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-375">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-376">目標矩形： {0，0，150，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-376">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="f596e-377">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-377">Primary video:</span></span>
    -   <span data-ttu-id="f596e-378">來源矩形： {0，0，150，50}</span><span class="sxs-lookup"><span data-stu-id="f596e-378">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="f596e-379">目的地矩形： {0，17，150，67}</span><span class="sxs-lookup"><span data-stu-id="f596e-379">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="f596e-380">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-380">Substream:</span></span>
    -   <span data-ttu-id="f596e-381">來源矩形： {0，0，100，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-381">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="f596e-382">目的地矩形： {25，0，125，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-382">Destination rectangle: { 25, 0, 125, 85 }</span></span>

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a><span data-ttu-id="f596e-383">範例4：目標矩形小於目的介面</span><span class="sxs-lookup"><span data-stu-id="f596e-383">Example 4: Target Rectangle Smaller Than Destination Surface</span></span>

<span data-ttu-id="f596e-384">這個範例會顯示目標矩形小於目的表面的案例。</span><span class="sxs-lookup"><span data-stu-id="f596e-384">This example shows a case where the target rectangle is smaller than the destination surface.</span></span>

![顯示目的地矩形 array.blit 的圖表。](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

<span data-ttu-id="f596e-386">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-386">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-387">目的地介面： {0，0，300，200}</span><span class="sxs-lookup"><span data-stu-id="f596e-387">Destination surface: { 0, 0, 300, 200 }</span></span>
-   <span data-ttu-id="f596e-388">目標矩形： {0，0，150，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-388">Target rectangle: { 0, 0, 150, 85 }</span></span>
-   <span data-ttu-id="f596e-389">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-389">Primary video:</span></span>
    -   <span data-ttu-id="f596e-390">來源矩形： {0，0，150，50}</span><span class="sxs-lookup"><span data-stu-id="f596e-390">Source rectangle: { 0, 0, 150, 50 }</span></span>
    -   <span data-ttu-id="f596e-391">目的地矩形： {0，17，150，67}</span><span class="sxs-lookup"><span data-stu-id="f596e-391">Destination rectangle: { 0, 17, 150, 67 }</span></span>
-   <span data-ttu-id="f596e-392">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-392">Substream:</span></span>
    -   <span data-ttu-id="f596e-393">來源矩形： {0，0，100，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-393">Source rectangle: { 0, 0, 100, 85 }</span></span>
    -   <span data-ttu-id="f596e-394">目的地矩形： {25，0，125，85}</span><span class="sxs-lookup"><span data-stu-id="f596e-394">Destination rectangle: { 25, 0, 125, 85 }</span></span>

<span data-ttu-id="f596e-395">目標矩形外的圖元不會被修改，因此背景色彩只會出現在目標矩形內。</span><span class="sxs-lookup"><span data-stu-id="f596e-395">Pixels outside of the target rectangle are not modified, so the background color appears only within the target rectangle.</span></span> <span data-ttu-id="f596e-396">點狀區域表示不受 array.blit 影響的目的表面部分。</span><span class="sxs-lookup"><span data-stu-id="f596e-396">The dotted area indicates portions of the destination surface that are not affected by the blit.</span></span>

### <a name="example-5-source-rectangles"></a><span data-ttu-id="f596e-397">範例5：來源矩形</span><span class="sxs-lookup"><span data-stu-id="f596e-397">Example 5: Source Rectangles</span></span>

<span data-ttu-id="f596e-398">如果您指定的來源矩形小於來源圖片，驅動程式就只會 array.blit 該部分的圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-398">If you specify a source rectangle that is smaller than the source picture, the driver will blit just that portion of the picture.</span></span> <span data-ttu-id="f596e-399">在此範例中，來源矩形會指定主要影片資料流程的右下象限，以及圖表) 中的雜湊標記所表示之子資料流程 (的左下象限。</span><span class="sxs-lookup"><span data-stu-id="f596e-399">In this example, the source rectangles specify the lower-right quadrant of the primary video stream and the lower-left quadrant of the substream (indicated by hash marks in the diagram).</span></span> <span data-ttu-id="f596e-400">目的地矩形的大小與來源矩形相同，因此不會伸展影片。</span><span class="sxs-lookup"><span data-stu-id="f596e-400">The destination rectangles are the same sizes as the source rectangles, so the video is not stretched.</span></span> <span data-ttu-id="f596e-401">來源和目的地矩形如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-401">The source and destination rectangles are shown in the following diagram.</span></span>

![顯示兩個來源矩形 array.blit 的圖表。](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

<span data-ttu-id="f596e-403">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-403">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-404">目標矩形： {0，0，720，576}</span><span class="sxs-lookup"><span data-stu-id="f596e-404">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="f596e-405">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-405">Primary video:</span></span>
    -   <span data-ttu-id="f596e-406">來源介面大小： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-406">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-407">來源矩形： {360、240、720、480}</span><span class="sxs-lookup"><span data-stu-id="f596e-407">Source rectangle: { 360, 240, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-408">目的地矩形： {0，0，360，240}</span><span class="sxs-lookup"><span data-stu-id="f596e-408">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="f596e-409">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-409">Substream:</span></span>
    -   <span data-ttu-id="f596e-410">來源介面大小： {0，0，640，576}</span><span class="sxs-lookup"><span data-stu-id="f596e-410">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="f596e-411">來源矩形： {0，288，320，576}</span><span class="sxs-lookup"><span data-stu-id="f596e-411">Source rectangle: { 0, 288, 320, 576 }</span></span>
    -   <span data-ttu-id="f596e-412">目的地矩形： {400，0，720，288}</span><span class="sxs-lookup"><span data-stu-id="f596e-412">Destination rectangle: { 400, 0, 720, 288 }</span></span>

### <a name="example-6-intersecting-destination-rectangles"></a><span data-ttu-id="f596e-413">範例6：交集的目的地矩形</span><span class="sxs-lookup"><span data-stu-id="f596e-413">Example 6: Intersecting Destination Rectangles</span></span>

<span data-ttu-id="f596e-414">這個範例與上一個範例類似，但目的矩形交集。</span><span class="sxs-lookup"><span data-stu-id="f596e-414">This example is similar to previous one, but the destination rectangles intersect.</span></span> <span data-ttu-id="f596e-415">表面尺寸與上一個範例相同，但來源和目的地矩形則不是。</span><span class="sxs-lookup"><span data-stu-id="f596e-415">The surface dimensions are the same as in the previous example, but the source and destination rectangles are not.</span></span> <span data-ttu-id="f596e-416">同樣地，影片會裁剪但不會伸展。</span><span class="sxs-lookup"><span data-stu-id="f596e-416">Again, the video is cropped but not stretched.</span></span> <span data-ttu-id="f596e-417">來源和目的地矩形如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-417">The source and destination rectangles are shown in the following diagram.</span></span>

![顯示交集目的矩形的圖表。](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

<span data-ttu-id="f596e-419">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-419">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-420">目標矩形： {0，0，720，576}</span><span class="sxs-lookup"><span data-stu-id="f596e-420">Target rectangle: { 0, 0, 720, 576 }</span></span>
-   <span data-ttu-id="f596e-421">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-421">Primary video:</span></span>
    -   <span data-ttu-id="f596e-422">來源介面大小： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-422">Source surface size: { 0, 0, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-423">來源矩形： {260、92、720、480}</span><span class="sxs-lookup"><span data-stu-id="f596e-423">Source rectangle: { 260, 92, 720, 480 }</span></span>
    -   <span data-ttu-id="f596e-424">目的地矩形： {0，0，460，388}</span><span class="sxs-lookup"><span data-stu-id="f596e-424">Destination rectangle: { 0, 0, 460, 388 }</span></span>
-   <span data-ttu-id="f596e-425">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-425">Substream:</span></span>
    -   <span data-ttu-id="f596e-426">來源介面大小： {0，0，640，576}</span><span class="sxs-lookup"><span data-stu-id="f596e-426">Source surface size: { 0, 0, 640, 576 }</span></span>
    -   <span data-ttu-id="f596e-427">來源矩形： {0，0，460，388}</span><span class="sxs-lookup"><span data-stu-id="f596e-427">Source rectangle: { 0, 0, 460, 388 }</span></span>
    -   <span data-ttu-id="f596e-428">目的地矩形： {260、188、720、576}</span><span class="sxs-lookup"><span data-stu-id="f596e-428">Destination rectangle: { 260, 188, 720, 576 }</span></span>

### <a name="example-7-stretching-and-cropping-video"></a><span data-ttu-id="f596e-429">範例7：延展和裁剪影片</span><span class="sxs-lookup"><span data-stu-id="f596e-429">Example 7: Stretching and Cropping Video</span></span>

<span data-ttu-id="f596e-430">在此範例中，影片會伸展並裁剪。</span><span class="sxs-lookup"><span data-stu-id="f596e-430">In this example, the video is stretched as well as cropped.</span></span> <span data-ttu-id="f596e-431">每個串流的180×120區域都會延展，以涵蓋目的地矩形中的360×240區域。</span><span class="sxs-lookup"><span data-stu-id="f596e-431">A 180 × 120 region from each stream is stretched to cover a 360 × 240 area in the destination rectangle.</span></span>

![顯示延展和裁剪的圖表。](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

<span data-ttu-id="f596e-433">上圖顯示下列矩形：</span><span class="sxs-lookup"><span data-stu-id="f596e-433">The preceding diagram shows the following rectangles:</span></span>

-   <span data-ttu-id="f596e-434">目標矩形： {0，0，720，480}</span><span class="sxs-lookup"><span data-stu-id="f596e-434">Target rectangle: { 0, 0, 720, 480 }</span></span>
-   <span data-ttu-id="f596e-435">主要影片：</span><span class="sxs-lookup"><span data-stu-id="f596e-435">Primary video:</span></span>
    -   <span data-ttu-id="f596e-436">來源介面大小： {0，0，360，240}</span><span class="sxs-lookup"><span data-stu-id="f596e-436">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="f596e-437">來源矩形： {180、120、360、240}</span><span class="sxs-lookup"><span data-stu-id="f596e-437">Source rectangle: { 180, 120, 360, 240 }</span></span>
    -   <span data-ttu-id="f596e-438">目的地矩形： {0，0，360，240}</span><span class="sxs-lookup"><span data-stu-id="f596e-438">Destination rectangle: { 0, 0, 360, 240 }</span></span>
-   <span data-ttu-id="f596e-439">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-439">Substream:</span></span>
    -   <span data-ttu-id="f596e-440">來源介面大小： {0，0，360，240}</span><span class="sxs-lookup"><span data-stu-id="f596e-440">Source surface size: { 0, 0, 360, 240 }</span></span>
    -   <span data-ttu-id="f596e-441">來源矩形： {0，0，180，120}</span><span class="sxs-lookup"><span data-stu-id="f596e-441">Source rectangle: { 0, 0, 180, 120 }</span></span>
    -   <span data-ttu-id="f596e-442">目的地矩形： {360、240、720、480}</span><span class="sxs-lookup"><span data-stu-id="f596e-442">Destination rectangle: { 360, 240, 720, 480 }</span></span>

## <a name="input-sample-order"></a><span data-ttu-id="f596e-443">輸入範例順序</span><span class="sxs-lookup"><span data-stu-id="f596e-443">Input Sample Order</span></span>

<span data-ttu-id="f596e-444">[**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)方法的 *pSamples* 參數是輸入範例陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="f596e-444">The *pSamples* parameter of the [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) method is a pointer to an array of input samples.</span></span> <span data-ttu-id="f596e-445">主要影片串流中的範例會先出現，後面接著以 Z 順序顯示的子資料流程圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-445">Samples from the primary video stream appear first, followed by substream pictures in Z-order.</span></span> <span data-ttu-id="f596e-446">範例必須依照下列順序放入陣列中：</span><span class="sxs-lookup"><span data-stu-id="f596e-446">Samples must be placed into the array in the following order:</span></span>

-   <span data-ttu-id="f596e-447">主要影片串流的範例會先出現在陣列中的時態順序中。</span><span class="sxs-lookup"><span data-stu-id="f596e-447">Samples for the primary video stream appear first in the array, in temporal order.</span></span> <span data-ttu-id="f596e-448">根據 [交錯] 模式，驅動程式可能需要主要影片串流中的一或多個參考範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-448">Depending on the deinterlace mode, the driver may require one or more reference samples from the primary video stream.</span></span> <span data-ttu-id="f596e-449">[**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps)結構的 **NumForwardRefSamples** 和 **NumBackwardRefSamples** 成員會指定所需的向前和向後參考樣本數。</span><span class="sxs-lookup"><span data-stu-id="f596e-449">The **NumForwardRefSamples** and **NumBackwardRefSamples** members of the [**DXVA2\_VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) structure specify how many forward and backward reference samples are needed.</span></span> <span data-ttu-id="f596e-450">呼叫端必須提供這些參考範例，即使影片內容是漸進式的，也不需要去交錯。</span><span class="sxs-lookup"><span data-stu-id="f596e-450">The caller must provide these reference samples even if the video content is progressive and does not require deinterlacing.</span></span> <span data-ttu-id="f596e-451"> (當漸進式框架提供給去交錯裝置時（例如，當來源同時包含交錯和漸進式框架的混合時），就會發生這種情況。 ) </span><span class="sxs-lookup"><span data-stu-id="f596e-451">(This can occur when progressive frames are given to a deinterlacing device, for example when the source contains a mix of both interlaced and progressive frames.)</span></span>
-   <span data-ttu-id="f596e-452">在主要影片串流的範例之後，陣列最多可包含15個子資料流程範例（以 Z 順序排列），從下到上。</span><span class="sxs-lookup"><span data-stu-id="f596e-452">After the samples for the primary video stream, the array can contain up to 15 substream samples, arranged in Z-order, from bottom to top.</span></span> <span data-ttu-id="f596e-453">子串流一律是漸進式的，不需要參考圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-453">Substreams are always progressive and do not require reference pictures.</span></span>

<span data-ttu-id="f596e-454">在任何時間，主要影片串流都可以在交錯和漸進式內容之間切換，而子串流數目也可以變更。</span><span class="sxs-lookup"><span data-stu-id="f596e-454">At any time, the primary video stream can switch between interlaced and progressive content, and the number of substreams can change.</span></span>

<span data-ttu-id="f596e-455">[**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **SampleFormat. SampleFormat** 成員表示圖片的類型。</span><span class="sxs-lookup"><span data-stu-id="f596e-455">The **SampleFormat.SampleFormat** member of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure indicates the type of picture.</span></span> <span data-ttu-id="f596e-456">針對子流圖片，將此值設定為 DXVA2 \_ SampleSubStream。</span><span class="sxs-lookup"><span data-stu-id="f596e-456">For substream pictures, set this value to DXVA2\_SampleSubStream.</span></span> <span data-ttu-id="f596e-457">針對漸進式圖片，此值為 DXVA2 \_ SampleProgressiveFrame。</span><span class="sxs-lookup"><span data-stu-id="f596e-457">For progressive pictures, the value is DXVA2\_SampleProgressiveFrame.</span></span> <span data-ttu-id="f596e-458">若為交錯圖片，此值取決於欄位配置。</span><span class="sxs-lookup"><span data-stu-id="f596e-458">For interlaced pictures, the value depends on the field layout.</span></span>

<span data-ttu-id="f596e-459">如果驅動程式需要向前及向後參考範例，則在影片順序開始時，可能無法使用完整的樣本數。</span><span class="sxs-lookup"><span data-stu-id="f596e-459">If the driver requires forward and backward reference samples, the full number of samples might not be available at the start of the video sequence.</span></span> <span data-ttu-id="f596e-460">在此情況下，請在 *pSamples* 陣列中包含這些專案的專案，但將遺漏的範例標示為具有類型 DXVA2 \_ SampleUnknown。</span><span class="sxs-lookup"><span data-stu-id="f596e-460">In that case, include entries for them in the *pSamples* array, but mark the missing samples as having type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="f596e-461">[**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)結構的 **開頭** 和 **結尾** 成員會提供每個範例的時態位置。</span><span class="sxs-lookup"><span data-stu-id="f596e-461">The **Start** and **End** members of the [**DXVA2\_VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) structure give the temporal location of each sample.</span></span> <span data-ttu-id="f596e-462">這些值只會用於主要影片串流中的樣本。</span><span class="sxs-lookup"><span data-stu-id="f596e-462">These values are used only for samples from the primary video stream.</span></span> <span data-ttu-id="f596e-463">若為子串流圖片，請將這兩個成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="f596e-463">For substream pictures, set both members to zero.</span></span>

<span data-ttu-id="f596e-464">下列範例可能有助於澄清這些需求。</span><span class="sxs-lookup"><span data-stu-id="f596e-464">The following examples may help to clarify these requirements.</span></span>

### <a name="example-1"></a><span data-ttu-id="f596e-465">範例 1</span><span class="sxs-lookup"><span data-stu-id="f596e-465">Example 1</span></span>

<span data-ttu-id="f596e-466">最簡單的情況是在沒有子串流時，而且去交錯演算法不需要參考範例 (**NumForwardRefSamples** 和 **NumBackwardRefSamples** 都是零) 。</span><span class="sxs-lookup"><span data-stu-id="f596e-466">The simplest case occurs when there are no substreams and the deinterlacing algorithm does not require reference samples (**NumForwardRefSamples** and **NumBackwardRefSamples** are both zero).</span></span> <span data-ttu-id="f596e-467">Bob 去交錯是這類演算法的範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-467">Bob deinterlacing is an example of such an algorithm.</span></span> <span data-ttu-id="f596e-468">在此情況下， *pSamples* 陣列應包含單一輸入介面，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-468">In this case, the *pSamples* array should contain a single input surface, as shown in the following table.</span></span>



| <span data-ttu-id="f596e-469">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-469">Index</span></span>           | <span data-ttu-id="f596e-470">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-470">Surface type</span></span>        | <span data-ttu-id="f596e-471">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-471">Temporal location</span></span> |
|-----------------|---------------------|-------------------|
| <span data-ttu-id="f596e-472">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-472">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-473">交錯圖片。</span><span class="sxs-lookup"><span data-stu-id="f596e-473">Interlaced picture.</span></span> | <span data-ttu-id="f596e-474">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-474">*T*</span></span>               |



 

<span data-ttu-id="f596e-475">時間值 *T* 會假設為目前影片框架的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-475">The time value *T* is assumed to be the start time of the current video frame.</span></span>

### <a name="example-2"></a><span data-ttu-id="f596e-476">範例 2</span><span class="sxs-lookup"><span data-stu-id="f596e-476">Example 2</span></span>

<span data-ttu-id="f596e-477">在此範例中，應用程式會混用兩個子串流與主要串流。</span><span class="sxs-lookup"><span data-stu-id="f596e-477">In this example, the application mixes two substreams with the primary stream.</span></span> <span data-ttu-id="f596e-478">去交錯演算法不需要參考範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-478">The deinterlacing algorithm does not require reference samples.</span></span> <span data-ttu-id="f596e-479">下表顯示如何在 *pSamples* 陣列中排列這些範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-479">The following table shows how these samples are arranged in the *pSamples* array.</span></span>



| <span data-ttu-id="f596e-480">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-480">Index</span></span>           | <span data-ttu-id="f596e-481">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-481">Surface type</span></span>       | <span data-ttu-id="f596e-482">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-482">Temporal location</span></span> | <span data-ttu-id="f596e-483">Z 順序</span><span class="sxs-lookup"><span data-stu-id="f596e-483">Z-order</span></span> |
|-----------------|--------------------|-------------------|---------|
| <span data-ttu-id="f596e-484">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-484">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-485">交錯圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-485">Interlaced picture</span></span> | <span data-ttu-id="f596e-486">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-486">*T*</span></span>               | <span data-ttu-id="f596e-487">0</span><span class="sxs-lookup"><span data-stu-id="f596e-487">0</span></span>       |
| <span data-ttu-id="f596e-488">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-488">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-489">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-489">Substream</span></span>          | <span data-ttu-id="f596e-490">0</span><span class="sxs-lookup"><span data-stu-id="f596e-490">0</span></span>                 | <span data-ttu-id="f596e-491">1</span><span class="sxs-lookup"><span data-stu-id="f596e-491">1</span></span>       |
| <span data-ttu-id="f596e-492">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-492">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-493">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-493">Substream</span></span>          | <span data-ttu-id="f596e-494">0</span><span class="sxs-lookup"><span data-stu-id="f596e-494">0</span></span>                 | <span data-ttu-id="f596e-495">2</span><span class="sxs-lookup"><span data-stu-id="f596e-495">2</span></span>       |



 

### <a name="example-3"></a><span data-ttu-id="f596e-496">範例 3</span><span class="sxs-lookup"><span data-stu-id="f596e-496">Example 3</span></span>

<span data-ttu-id="f596e-497">現在假設去交錯演算法需要一個反向參考範例和一個向前參考範例。</span><span class="sxs-lookup"><span data-stu-id="f596e-497">Now suppose that the deinterlacing algorithm requires one backward reference sample and one forward reference sample.</span></span> <span data-ttu-id="f596e-498">此外，還提供兩個子流圖片，總共五個表面。</span><span class="sxs-lookup"><span data-stu-id="f596e-498">In addition, two substream pictures are provided, for a total of five surfaces.</span></span> <span data-ttu-id="f596e-499">下表顯示正確的順序。</span><span class="sxs-lookup"><span data-stu-id="f596e-499">The correct ordering is shown in the following table.</span></span>



| <span data-ttu-id="f596e-500">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-500">Index</span></span>           | <span data-ttu-id="f596e-501">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-501">Surface type</span></span>                   | <span data-ttu-id="f596e-502">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-502">Temporal location</span></span> | <span data-ttu-id="f596e-503">Z 順序</span><span class="sxs-lookup"><span data-stu-id="f596e-503">Z-order</span></span>        |
|-----------------|--------------------------------|-------------------|----------------|
| <span data-ttu-id="f596e-504">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-504">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-505">交錯式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-505">Interlaced picture (reference)</span></span> | <span data-ttu-id="f596e-506">*T* −1</span><span class="sxs-lookup"><span data-stu-id="f596e-506">*T* −1</span></span>            | <span data-ttu-id="f596e-507">不適用</span><span class="sxs-lookup"><span data-stu-id="f596e-507">Not applicable</span></span> |
| <span data-ttu-id="f596e-508">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-508">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-509">交錯圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-509">Interlaced picture</span></span>             | <span data-ttu-id="f596e-510">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-510">*T*</span></span>               | <span data-ttu-id="f596e-511">0</span><span class="sxs-lookup"><span data-stu-id="f596e-511">0</span></span>              |
| <span data-ttu-id="f596e-512">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-512">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-513">交錯式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-513">Interlaced picture (reference)</span></span> | <span data-ttu-id="f596e-514">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="f596e-514">*T* +1</span></span>            | <span data-ttu-id="f596e-515">不適用</span><span class="sxs-lookup"><span data-stu-id="f596e-515">Not applicable</span></span> |
| <span data-ttu-id="f596e-516">*pSamples* \[3\]</span><span class="sxs-lookup"><span data-stu-id="f596e-516">*pSamples*\[3\]</span></span> | <span data-ttu-id="f596e-517">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-517">Substream</span></span>                      | <span data-ttu-id="f596e-518">0</span><span class="sxs-lookup"><span data-stu-id="f596e-518">0</span></span>                 | <span data-ttu-id="f596e-519">1</span><span class="sxs-lookup"><span data-stu-id="f596e-519">1</span></span>              |
| <span data-ttu-id="f596e-520">*pSamples* \[億\]</span><span class="sxs-lookup"><span data-stu-id="f596e-520">*pSamples*\[4\]</span></span> | <span data-ttu-id="f596e-521">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-521">Substream</span></span>                      | <span data-ttu-id="f596e-522">0</span><span class="sxs-lookup"><span data-stu-id="f596e-522">0</span></span>                 | <span data-ttu-id="f596e-523">2</span><span class="sxs-lookup"><span data-stu-id="f596e-523">2</span></span>              |



 

<span data-ttu-id="f596e-524">時間 *T* −1是目前畫面格之前的框架開始時間，而 *T* + 1 是下列框架的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f596e-524">The time *T* −1 is the start time of the frame before the current frame, and *T* +1 is the start time of the following frame.</span></span>

<span data-ttu-id="f596e-525">如果影片資料流程切換至漸進式內容（使用相同的去交錯模式），應用程式必須提供相同的樣本數，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="f596e-525">If the video stream switches to progressive content, using the same deinterlacing mode, the application must provide the same number of samples, as shown in the following table.</span></span>



| <span data-ttu-id="f596e-526">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-526">Index</span></span>           | <span data-ttu-id="f596e-527">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-527">Surface type</span></span>                    | <span data-ttu-id="f596e-528">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-528">Temporal location</span></span> | <span data-ttu-id="f596e-529">Z 順序</span><span class="sxs-lookup"><span data-stu-id="f596e-529">Z-order</span></span>        |
|-----------------|---------------------------------|-------------------|----------------|
| <span data-ttu-id="f596e-530">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-530">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-531">漸進式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-531">Progressive picture (reference)</span></span> | <span data-ttu-id="f596e-532">*T* −1</span><span class="sxs-lookup"><span data-stu-id="f596e-532">*T* −1</span></span>            | <span data-ttu-id="f596e-533">不適用</span><span class="sxs-lookup"><span data-stu-id="f596e-533">Not applicable</span></span> |
| <span data-ttu-id="f596e-534">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-534">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-535">漸進式圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-535">Progressive picture</span></span>             | <span data-ttu-id="f596e-536">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-536">*T*</span></span>               | <span data-ttu-id="f596e-537">0</span><span class="sxs-lookup"><span data-stu-id="f596e-537">0</span></span>              |
| <span data-ttu-id="f596e-538">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-538">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-539">漸進式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-539">Progressive picture (reference)</span></span> | <span data-ttu-id="f596e-540">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="f596e-540">*T* +1</span></span>            | <span data-ttu-id="f596e-541">不適用</span><span class="sxs-lookup"><span data-stu-id="f596e-541">Not applicable</span></span> |
| <span data-ttu-id="f596e-542">*pSamples* \[3\]</span><span class="sxs-lookup"><span data-stu-id="f596e-542">*pSamples*\[3\]</span></span> | <span data-ttu-id="f596e-543">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-543">Substream</span></span>                       | <span data-ttu-id="f596e-544">0</span><span class="sxs-lookup"><span data-stu-id="f596e-544">0</span></span>                 | <span data-ttu-id="f596e-545">1</span><span class="sxs-lookup"><span data-stu-id="f596e-545">1</span></span>              |
| <span data-ttu-id="f596e-546">*pSamples* \[億\]</span><span class="sxs-lookup"><span data-stu-id="f596e-546">*pSamples*\[4\]</span></span> | <span data-ttu-id="f596e-547">子串流</span><span class="sxs-lookup"><span data-stu-id="f596e-547">Substream</span></span>                       | <span data-ttu-id="f596e-548">0</span><span class="sxs-lookup"><span data-stu-id="f596e-548">0</span></span>                 | <span data-ttu-id="f596e-549">2</span><span class="sxs-lookup"><span data-stu-id="f596e-549">2</span></span>              |



 

### <a name="example-4"></a><span data-ttu-id="f596e-550">範例 4</span><span class="sxs-lookup"><span data-stu-id="f596e-550">Example 4</span></span>

<span data-ttu-id="f596e-551">在影片順序開始時，向前和向後參考範例可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="f596e-551">At the start of a video sequence, forward and backward reference samples might not be available.</span></span> <span data-ttu-id="f596e-552">發生這種情況時，遺漏範例的專案會包含在 *pSamples* 陣列中，其範例類型為 DXVA2 \_ SampleUnknown。</span><span class="sxs-lookup"><span data-stu-id="f596e-552">When this happens, entries for the missing samples are included in the *pSamples* array, with sample type DXVA2\_SampleUnknown.</span></span>

<span data-ttu-id="f596e-553">假設去交錯模式需要一個向前和一個反向參考範例，則前三個對 [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) 的呼叫會有下列三個數據表中所顯示的輸入序列。</span><span class="sxs-lookup"><span data-stu-id="f596e-553">Assuming that the deinterlacing mode needs one forward and one backward reference sample, the first three calls to [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) would have the sequences of inputs shown in the following three tables.</span></span>



| <span data-ttu-id="f596e-554">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-554">Index</span></span>           | <span data-ttu-id="f596e-555">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-555">Surface type</span></span>                   | <span data-ttu-id="f596e-556">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-556">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="f596e-557">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-557">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-558">Unknown</span><span class="sxs-lookup"><span data-stu-id="f596e-558">Unknown</span></span>                        | <span data-ttu-id="f596e-559">0</span><span class="sxs-lookup"><span data-stu-id="f596e-559">0</span></span>                 |
| <span data-ttu-id="f596e-560">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-560">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-561">Unknown</span><span class="sxs-lookup"><span data-stu-id="f596e-561">Unknown</span></span>                        | <span data-ttu-id="f596e-562">0</span><span class="sxs-lookup"><span data-stu-id="f596e-562">0</span></span>                 |
| <span data-ttu-id="f596e-563">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-563">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-564">交錯式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-564">Interlaced picture (reference)</span></span> | <span data-ttu-id="f596e-565">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="f596e-565">*T* +1</span></span>            |



 



| <span data-ttu-id="f596e-566">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-566">Index</span></span>           | <span data-ttu-id="f596e-567">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-567">Surface type</span></span>                   | <span data-ttu-id="f596e-568">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-568">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="f596e-569">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-569">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-570">Unknown</span><span class="sxs-lookup"><span data-stu-id="f596e-570">Unknown</span></span>                        | <span data-ttu-id="f596e-571">0</span><span class="sxs-lookup"><span data-stu-id="f596e-571">0</span></span>                 |
| <span data-ttu-id="f596e-572">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-572">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-573">交錯圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-573">Interlaced picture</span></span>             | <span data-ttu-id="f596e-574">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-574">*T*</span></span>               |
| <span data-ttu-id="f596e-575">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-575">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-576">交錯式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-576">Interlaced picture (reference)</span></span> | <span data-ttu-id="f596e-577">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="f596e-577">*T* +1</span></span>            |



 



| <span data-ttu-id="f596e-578">索引</span><span class="sxs-lookup"><span data-stu-id="f596e-578">Index</span></span>           | <span data-ttu-id="f596e-579">介面類別型</span><span class="sxs-lookup"><span data-stu-id="f596e-579">Surface type</span></span>                   | <span data-ttu-id="f596e-580">時態性位置</span><span class="sxs-lookup"><span data-stu-id="f596e-580">Temporal location</span></span> |
|-----------------|--------------------------------|-------------------|
| <span data-ttu-id="f596e-581">*pSamples* \[0\]</span><span class="sxs-lookup"><span data-stu-id="f596e-581">*pSamples*\[0\]</span></span> | <span data-ttu-id="f596e-582">交錯圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-582">Interlaced picture</span></span>             | <span data-ttu-id="f596e-583">*T* −1</span><span class="sxs-lookup"><span data-stu-id="f596e-583">*T* −1</span></span>            |
| <span data-ttu-id="f596e-584">*pSamples* \[單\]</span><span class="sxs-lookup"><span data-stu-id="f596e-584">*pSamples*\[1\]</span></span> | <span data-ttu-id="f596e-585">交錯圖片</span><span class="sxs-lookup"><span data-stu-id="f596e-585">Interlaced picture</span></span>             | <span data-ttu-id="f596e-586">*T*</span><span class="sxs-lookup"><span data-stu-id="f596e-586">*T*</span></span>               |
| <span data-ttu-id="f596e-587">*pSamples* \[二級\]</span><span class="sxs-lookup"><span data-stu-id="f596e-587">*pSamples*\[2\]</span></span> | <span data-ttu-id="f596e-588">交錯式圖片 (參考) </span><span class="sxs-lookup"><span data-stu-id="f596e-588">Interlaced picture (reference)</span></span> | <span data-ttu-id="f596e-589">*T* + 1</span><span class="sxs-lookup"><span data-stu-id="f596e-589">*T* +1</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="f596e-590">相關主題</span><span class="sxs-lookup"><span data-stu-id="f596e-590">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f596e-591">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="f596e-591">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="f596e-592">DXVA2 \_ VideoProc 範例</span><span class="sxs-lookup"><span data-stu-id="f596e-592">DXVA2\_VideoProc Sample</span></span>](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
