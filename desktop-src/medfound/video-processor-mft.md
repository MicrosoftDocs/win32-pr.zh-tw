---
description: 影片處理器 MFT 是 Microsoft 媒體基礎轉換 (MFT) ，可執行 colorspace 轉換、影片調整大小、去交錯、畫面播放速率轉換、旋轉、裁剪、空間左方和右視圖打開包裝，以及鏡像。
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: '視頻處理器 MFT (Camerauicontrol .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995067"
---
# <a name="video-processor-mft"></a><span data-ttu-id="964cd-103">視頻處理器 MFT</span><span class="sxs-lookup"><span data-stu-id="964cd-103">Video Processor MFT</span></span>

<span data-ttu-id="964cd-104">影片處理器 MFT 是 Microsoft 媒體基礎轉換 (MFT) ，可執行 colorspace 轉換、影片調整大小、去交錯、畫面播放速率轉換、旋轉、裁剪、空間左方和右視圖打開包裝，以及鏡像。</span><span class="sxs-lookup"><span data-stu-id="964cd-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="964cd-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="964cd-105">CLSID</span></span>

<span data-ttu-id="964cd-106">CLSID \_ VideoProcessorMFT</span><span class="sxs-lookup"><span data-stu-id="964cd-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="964cd-107">介面</span><span class="sxs-lookup"><span data-stu-id="964cd-107">Interfaces</span></span>

-   [<span data-ttu-id="964cd-108">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="964cd-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="964cd-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="964cd-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="964cd-110">**IMFVideoProcessorControl**</span><span class="sxs-lookup"><span data-stu-id="964cd-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="964cd-111">輸入格式</span><span class="sxs-lookup"><span data-stu-id="964cd-111">Input Formats</span></span>

-   <span data-ttu-id="964cd-112">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="964cd-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="964cd-113">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="964cd-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="964cd-114">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="964cd-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="964cd-115">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="964cd-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="964cd-116">**MFVideoFormat \_ NV11**</span><span class="sxs-lookup"><span data-stu-id="964cd-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="964cd-117">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="964cd-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="964cd-118">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="964cd-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="964cd-119">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="964cd-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="964cd-120">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="964cd-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="964cd-121">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="964cd-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="964cd-122">**MFVideoFormat \_ RGB8**</span><span class="sxs-lookup"><span data-stu-id="964cd-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="964cd-123">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="964cd-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="964cd-124">**MFVideoFormat \_ v410**</span><span class="sxs-lookup"><span data-stu-id="964cd-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="964cd-125">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="964cd-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="964cd-126">**MFVideoFormat \_ Y41P**</span><span class="sxs-lookup"><span data-stu-id="964cd-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="964cd-127">**MFVideoFormat \_ Y41T**</span><span class="sxs-lookup"><span data-stu-id="964cd-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="964cd-128">**MFVideoFormat \_ Y42T**</span><span class="sxs-lookup"><span data-stu-id="964cd-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="964cd-129">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="964cd-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="964cd-130">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="964cd-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="964cd-131">**MFVideoFormat \_ YVYU**</span><span class="sxs-lookup"><span data-stu-id="964cd-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="964cd-132">輸出格式</span><span class="sxs-lookup"><span data-stu-id="964cd-132">Output Formats</span></span>

-   <span data-ttu-id="964cd-133">**MFVideoFormat \_ ARGB32**</span><span class="sxs-lookup"><span data-stu-id="964cd-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="964cd-134">**MFVideoFormat \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="964cd-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="964cd-135">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="964cd-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="964cd-136">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="964cd-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="964cd-137">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="964cd-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="964cd-138">**MFVideoFormat \_ RGB24**</span><span class="sxs-lookup"><span data-stu-id="964cd-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="964cd-139">**MFVideoFormat \_ RGB32**</span><span class="sxs-lookup"><span data-stu-id="964cd-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="964cd-140">**MFVideoFormat \_ RGB555**</span><span class="sxs-lookup"><span data-stu-id="964cd-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="964cd-141">**MFVideoFormat \_ RGB565**</span><span class="sxs-lookup"><span data-stu-id="964cd-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="964cd-142">**MFVideoFormat \_ UYVY**</span><span class="sxs-lookup"><span data-stu-id="964cd-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="964cd-143">**MFVideoFormat \_ Y216**</span><span class="sxs-lookup"><span data-stu-id="964cd-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="964cd-144">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="964cd-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="964cd-145">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="964cd-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="964cd-146">不支援每個輸入和輸出格式的組合。</span><span class="sxs-lookup"><span data-stu-id="964cd-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="964cd-147">若要測試是否支援轉換，請設定輸入類型，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)。</span><span class="sxs-lookup"><span data-stu-id="964cd-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="964cd-148">如需這些格式的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="964cd-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="964cd-149">備註</span><span class="sxs-lookup"><span data-stu-id="964cd-149">Remarks</span></span>

<span data-ttu-id="964cd-150">您可以使用下列其中一種方式來建立影片處理器的實例：</span><span class="sxs-lookup"><span data-stu-id="964cd-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="964cd-151">藉由呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)。</span><span class="sxs-lookup"><span data-stu-id="964cd-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="964cd-152">影片處理器會註冊在 [MFT 類別] 的 [ **\_ \_ 視頻 \_ 處理器** ] 類別之下。</span><span class="sxs-lookup"><span data-stu-id="964cd-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="964cd-153">藉由呼叫 COM 函式， **CoCreateInstance** 將 clsid **clsid \_ VideoProcessorMFT** 傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="964cd-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="964cd-154">下列備註適用于在 **視頻處理器 MFT** 中使用來源矩形和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="964cd-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="964cd-155">來源和目的地矩形會以 [**IMFVideoProcessorControl：： SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) 和 [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) 設定，而某些時間使用 [**IMFMediaEngineEx：： UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream)。</span><span class="sxs-lookup"><span data-stu-id="964cd-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="964cd-156">來源矩形應該對齊並舍入，以符合輸入至視頻處理器之畫面格的色彩格式需求。</span><span class="sxs-lookup"><span data-stu-id="964cd-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="964cd-157">這點很重要，因為像是420和422的格式有關于可建立和存取之維度和位移的需求。</span><span class="sxs-lookup"><span data-stu-id="964cd-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="964cd-158">例如，當輸入格式為420時，{1，0，319，240} (左、上、右、下) 的來源矩形會舍入為 {2，0，320，240}。</span><span class="sxs-lookup"><span data-stu-id="964cd-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="964cd-159">目的地和來源矩形一律會壓制，以納入其各自的框架中，也就是來源框架和目的地矩形的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="964cd-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="964cd-160">這表示負數值沒有意義，它們一律會壓制為0。</span><span class="sxs-lookup"><span data-stu-id="964cd-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="964cd-161">來源矩形位於目的框架的座標系統中，減去任何目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="964cd-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="964cd-162">這表示轉換（例如旋轉）在來源矩形上是「復原」。</span><span class="sxs-lookup"><span data-stu-id="964cd-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="964cd-163">因此，您不需要知道影片是旋轉或立體解壓縮。</span><span class="sxs-lookup"><span data-stu-id="964cd-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="964cd-164">例如，您可以在影片標記的最上方繪製一個矩形， (相對於影片標籤) 的相對座標，將其正規化 (範圍0到 1) 並將其以來源矩形的形式傳遞，且應該如預期般運作，即使影片正在旋轉也一樣。</span><span class="sxs-lookup"><span data-stu-id="964cd-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="964cd-165">影片處理器支援使用 Microsoft Direct3D 11 的 GPU 加速影片處理。</span><span class="sxs-lookup"><span data-stu-id="964cd-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="964cd-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="964cd-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="964cd-167">Stereoscopic 影片</span><span class="sxs-lookup"><span data-stu-id="964cd-167">Stereoscopic Video</span></span>

<span data-ttu-id="964cd-168">影片處理器支援3D 影片畫面上的「觀看解壓縮」操作：</span><span class="sxs-lookup"><span data-stu-id="964cd-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="964cd-169">如果輸入框架包含兩個在相同框架中封裝的視圖，則影片處理器可以將這些視圖分割成不同的緩衝區，或將基底視圖解壓縮並捨棄第二個視圖。</span><span class="sxs-lookup"><span data-stu-id="964cd-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="964cd-170">若要啟用視圖解壓縮，請將 [ [MF \_ 啟用 \_ 3DVIDEO \_ 輸出](mf-enable-3dvideo-output.md) ] 屬性設定為 **MF3DVideoOutputType \_ 身歷聲** 或 **MF3DVideoOutputType \_ 基礎**。</span><span class="sxs-lookup"><span data-stu-id="964cd-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="964cd-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="964cd-171">Requirements</span></span>



| <span data-ttu-id="964cd-172">需求</span><span class="sxs-lookup"><span data-stu-id="964cd-172">Requirement</span></span> | <span data-ttu-id="964cd-173">值</span><span class="sxs-lookup"><span data-stu-id="964cd-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="964cd-174">標頭</span><span class="sxs-lookup"><span data-stu-id="964cd-174">Header</span></span><br/> | <dl> <span data-ttu-id="964cd-175"><dt>Camerauicontrol。h</dt></span><span class="sxs-lookup"><span data-stu-id="964cd-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="964cd-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="964cd-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="964cd-177">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="964cd-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




