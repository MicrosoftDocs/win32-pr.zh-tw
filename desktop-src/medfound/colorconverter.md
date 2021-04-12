---
description: 在色彩格式之間轉換影片串流。
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: '色彩轉換器 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468640"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="55386-103">色彩轉換器 DSP</span><span class="sxs-lookup"><span data-stu-id="55386-103">Color Converter DSP</span></span>

<span data-ttu-id="55386-104">在色彩格式之間轉換影片串流。</span><span class="sxs-lookup"><span data-stu-id="55386-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="55386-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="55386-105">CLSID</span></span>

<span data-ttu-id="55386-106">CLSID \_ CColorConvertDMO</span><span class="sxs-lookup"><span data-stu-id="55386-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="55386-107">介面</span><span class="sxs-lookup"><span data-stu-id="55386-107">Interfaces</span></span>

-   [<span data-ttu-id="55386-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="55386-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="55386-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="55386-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="55386-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="55386-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="55386-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="55386-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="55386-112">IWMColorConvProps</span><span class="sxs-lookup"><span data-stu-id="55386-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="55386-113">輸入格式</span><span class="sxs-lookup"><span data-stu-id="55386-113">Input Formats</span></span>

-   <span data-ttu-id="55386-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="55386-114">RGB 24</span></span>
-   <span data-ttu-id="55386-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="55386-115">RGB 32</span></span>
-   <span data-ttu-id="55386-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="55386-116">RGB 555</span></span>
-   <span data-ttu-id="55386-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="55386-117">RGB 565</span></span>
-   <span data-ttu-id="55386-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="55386-118">RGB 8</span></span>
-   <span data-ttu-id="55386-119">AYUV</span><span class="sxs-lookup"><span data-stu-id="55386-119">AYUV</span></span>
-   <span data-ttu-id="55386-120">I420</span><span class="sxs-lookup"><span data-stu-id="55386-120">I420</span></span>
-   <span data-ttu-id="55386-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="55386-121">IYUV</span></span>
-   <span data-ttu-id="55386-122">NV11</span><span class="sxs-lookup"><span data-stu-id="55386-122">NV11</span></span>
-   <span data-ttu-id="55386-123">NV12</span><span class="sxs-lookup"><span data-stu-id="55386-123">NV12</span></span>
-   <span data-ttu-id="55386-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="55386-124">UYVY</span></span>
-   <span data-ttu-id="55386-125">V216</span><span class="sxs-lookup"><span data-stu-id="55386-125">V216</span></span>
-   <span data-ttu-id="55386-126">V410</span><span class="sxs-lookup"><span data-stu-id="55386-126">V410</span></span>
-   <span data-ttu-id="55386-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="55386-127">Y41P</span></span>
-   <span data-ttu-id="55386-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="55386-128">Y41T</span></span>
-   <span data-ttu-id="55386-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="55386-129">Y42T</span></span>
-   <span data-ttu-id="55386-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="55386-130">YUY2</span></span>
-   <span data-ttu-id="55386-131">YV12</span><span class="sxs-lookup"><span data-stu-id="55386-131">YV12</span></span>
-   <span data-ttu-id="55386-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="55386-132">YVU9</span></span>
-   <span data-ttu-id="55386-133">YVYU</span><span class="sxs-lookup"><span data-stu-id="55386-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="55386-134">輸出格式</span><span class="sxs-lookup"><span data-stu-id="55386-134">Output Formats</span></span>

-   <span data-ttu-id="55386-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="55386-135">RGB 24</span></span>
-   <span data-ttu-id="55386-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="55386-136">RGB 32</span></span>
-   <span data-ttu-id="55386-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="55386-137">RGB 555</span></span>
-   <span data-ttu-id="55386-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="55386-138">RGB 565</span></span>
-   <span data-ttu-id="55386-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="55386-139">RGB 8</span></span>
-   <span data-ttu-id="55386-140">AYUV</span><span class="sxs-lookup"><span data-stu-id="55386-140">AYUV</span></span>
-   <span data-ttu-id="55386-141">I420</span><span class="sxs-lookup"><span data-stu-id="55386-141">I420</span></span>
-   <span data-ttu-id="55386-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="55386-142">IYUV</span></span>
-   <span data-ttu-id="55386-143">NV11</span><span class="sxs-lookup"><span data-stu-id="55386-143">NV11</span></span>
-   <span data-ttu-id="55386-144">NV12</span><span class="sxs-lookup"><span data-stu-id="55386-144">NV12</span></span>
-   <span data-ttu-id="55386-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="55386-145">UYVY</span></span>
-   <span data-ttu-id="55386-146">V216</span><span class="sxs-lookup"><span data-stu-id="55386-146">V216</span></span>
-   <span data-ttu-id="55386-147">V410</span><span class="sxs-lookup"><span data-stu-id="55386-147">V410</span></span>
-   <span data-ttu-id="55386-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="55386-148">YUY2</span></span>
-   <span data-ttu-id="55386-149">YV12</span><span class="sxs-lookup"><span data-stu-id="55386-149">YV12</span></span>
-   <span data-ttu-id="55386-150">YVYU</span><span class="sxs-lookup"><span data-stu-id="55386-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="55386-151">屬性</span><span class="sxs-lookup"><span data-stu-id="55386-151">Properties</span></span>

-   [<span data-ttu-id="55386-152">MFPKEY \_ COLORCONV \_ SRCLEFT</span><span class="sxs-lookup"><span data-stu-id="55386-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="55386-153">MFPKEY \_ COLORCONV \_ SRCTOP</span><span class="sxs-lookup"><span data-stu-id="55386-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="55386-154">MFPKEY \_ COLORCONV \_ DSTLEFT</span><span class="sxs-lookup"><span data-stu-id="55386-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="55386-155">MFPKEY \_ COLORCONV \_ DSTTOP</span><span class="sxs-lookup"><span data-stu-id="55386-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="55386-156">MFPKEY \_ COLORCONV \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="55386-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="55386-157">MFPKEY \_ COLORCONV \_ HEIGHT</span><span class="sxs-lookup"><span data-stu-id="55386-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="55386-158">MFPKEY \_ COLORCONV \_ 模式</span><span class="sxs-lookup"><span data-stu-id="55386-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="55386-159">備註</span><span class="sxs-lookup"><span data-stu-id="55386-159">Remarks</span></span>

<span data-ttu-id="55386-160">色彩轉換器 DSP 會實作為 COM 物件，此物件可做為 DirectXMedia 物件 (的) 或媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="55386-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="55386-161">此物件具有單一類別識別碼 (CLSID) ，不論它是否可作為一或一個 MFT。</span><span class="sxs-lookup"><span data-stu-id="55386-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="55386-162">如需有關 DSP 作為一或是 MFT 之時機的詳細資訊，請參閱 [數位訊號處理器](windowsmediadigitalsignalprocessors.md)。</span><span class="sxs-lookup"><span data-stu-id="55386-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="55386-163">針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據 DSP 是以 SQL-DMO 或 MFT 的方式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="55386-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="55386-164">非 RGB 媒體子類型的 Guid 是相同的，不論 DSP 是以 SQL-DMO 或 MFT 作為的。</span><span class="sxs-lookup"><span data-stu-id="55386-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="55386-165">如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="55386-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="55386-166">根據預設，這個 DSP 會將整個來源影像複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="55386-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="55386-167">（選擇性）您可以指定來源和目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="55386-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="55386-168">DSP 會複製來源矩形所定義之來源影像的部分，並將它寫入輸出緩衝區的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="55386-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="55386-169">DSP 不會執行任何調整;來源和目的地矩形的大小必須相同。</span><span class="sxs-lookup"><span data-stu-id="55386-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="55386-170">來源和目的地矩形不能超過影片框架的界限。</span><span class="sxs-lookup"><span data-stu-id="55386-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="55386-171">除了 [**MFPKEY \_ COLORCONV \_ 模式**](mfpkey-colorconv-mode.md) 以外的所有屬性都必須在群組中設定。</span><span class="sxs-lookup"><span data-stu-id="55386-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="55386-172">如果您設定任何這些屬性，則必須設定其他屬性。</span><span class="sxs-lookup"><span data-stu-id="55386-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="55386-173">否則，來源和目的地矩形可能無效，在這種情況下， [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 和 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) 方法都會傳回 **E \_ INVALIDARG**。</span><span class="sxs-lookup"><span data-stu-id="55386-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="55386-174">色彩轉換器不支援輸入格式和輸出格式的每個組合。</span><span class="sxs-lookup"><span data-stu-id="55386-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="55386-175">通常，您應該設定您知道的媒體格式，也就是輸入或輸出，然後在相反的資料流程上列舉可用的格式。</span><span class="sxs-lookup"><span data-stu-id="55386-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="55386-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="55386-176">Requirements</span></span>



| <span data-ttu-id="55386-177">需求</span><span class="sxs-lookup"><span data-stu-id="55386-177">Requirement</span></span> | <span data-ttu-id="55386-178">值</span><span class="sxs-lookup"><span data-stu-id="55386-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55386-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55386-179">Minimum supported client</span></span><br/> | <span data-ttu-id="55386-180">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55386-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="55386-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55386-181">Minimum supported server</span></span><br/> | <span data-ttu-id="55386-182">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55386-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55386-183">標頭</span><span class="sxs-lookup"><span data-stu-id="55386-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="55386-184"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="55386-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="55386-185">DLL</span><span class="sxs-lookup"><span data-stu-id="55386-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55386-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55386-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55386-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55386-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55386-188">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="55386-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
