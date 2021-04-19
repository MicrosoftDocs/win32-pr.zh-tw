---
description: 調整影片資料流程的大小。
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: " (Wmcodecdsp 的影片尺寸調整) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971688"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="e9bbc-103">影片尺寸調整 DSP</span><span class="sxs-lookup"><span data-stu-id="e9bbc-103">Video Resizer DSP</span></span>

<span data-ttu-id="e9bbc-104">調整影片資料流程的大小。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="e9bbc-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="e9bbc-105">CLSID</span></span>

<span data-ttu-id="e9bbc-106">CLSID \_ CResizerDMO</span><span class="sxs-lookup"><span data-stu-id="e9bbc-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="e9bbc-107">介面</span><span class="sxs-lookup"><span data-stu-id="e9bbc-107">Interfaces</span></span>

-   [<span data-ttu-id="e9bbc-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="e9bbc-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="e9bbc-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="e9bbc-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="e9bbc-112">**IWMResizerProps**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="e9bbc-113">格式</span><span class="sxs-lookup"><span data-stu-id="e9bbc-113">Formats</span></span>

<span data-ttu-id="e9bbc-114">影片調整器 DSP 在作為 DirectX 媒體物件時，支援下列輸入/輸出媒體子類型 (的) 。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="e9bbc-115">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="e9bbc-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="e9bbc-116">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e9bbc-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="e9bbc-117">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="e9bbc-118">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="e9bbc-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="e9bbc-119">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e9bbc-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="e9bbc-120">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="e9bbc-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="e9bbc-121">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e9bbc-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="e9bbc-122">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e9bbc-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="e9bbc-123">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e9bbc-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="e9bbc-124">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="e9bbc-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="e9bbc-125">MEDIASUBTYPE \_ V216</span><span class="sxs-lookup"><span data-stu-id="e9bbc-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="e9bbc-126">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="e9bbc-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="e9bbc-127">影片調整器 DSP 支援下列輸入/輸出媒體子類型作為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="e9bbc-128">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="e9bbc-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="e9bbc-129">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="e9bbc-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="e9bbc-130">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="e9bbc-131">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="e9bbc-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="e9bbc-132">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="e9bbc-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="e9bbc-133">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="e9bbc-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="e9bbc-134">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="e9bbc-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="e9bbc-135">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="e9bbc-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="e9bbc-136">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="e9bbc-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="e9bbc-137">MFVideoFormat \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="e9bbc-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="e9bbc-138">MFVideoFormat \_ V216</span><span class="sxs-lookup"><span data-stu-id="e9bbc-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="e9bbc-139">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="e9bbc-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="e9bbc-140">屬性</span><span class="sxs-lookup"><span data-stu-id="e9bbc-140">Properties</span></span>

-   [<span data-ttu-id="e9bbc-141">MFPKEY \_ 調整 \_ SRC \_ 左方</span><span class="sxs-lookup"><span data-stu-id="e9bbc-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="e9bbc-142">MFPKEY \_ 調整 \_ SRC \_ TOP</span><span class="sxs-lookup"><span data-stu-id="e9bbc-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="e9bbc-143">MFPKEY \_ 調整 \_ SRC \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="e9bbc-144">MFPKEY \_ 調整 \_ SRC \_ 高度大小</span><span class="sxs-lookup"><span data-stu-id="e9bbc-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="e9bbc-145">MFPKEY \_ 將 \_ DST \_ 左大小調整</span><span class="sxs-lookup"><span data-stu-id="e9bbc-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="e9bbc-146">MFPKEY \_ 調整 \_ DST \_ 頂端</span><span class="sxs-lookup"><span data-stu-id="e9bbc-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="e9bbc-147">MFPKEY \_ 調整 \_ DST \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="e9bbc-148">MFPKEY \_ 調整 \_ DST \_ 高度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="e9bbc-149">MFPKEY \_ 調整 \_ 品質</span><span class="sxs-lookup"><span data-stu-id="e9bbc-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="e9bbc-150">MFPKEY 重 \_ 設大小 \_ 交錯</span><span class="sxs-lookup"><span data-stu-id="e9bbc-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="e9bbc-151">MFPKEY 重 \_ 設大小 \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="e9bbc-152">MFPKEY 重 \_ 設大小 \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="e9bbc-153">MFPKEY 重 \_ 設大小 \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="e9bbc-154">MFPKEY 重 \_ 設大小 \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="e9bbc-155">MFPKEY 重 \_ 設大小 \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="e9bbc-156">MFPKEY 重 \_ 設大小 \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="e9bbc-157">MFPKEY 重 \_ 設大小 \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="e9bbc-158">MFPKEY 重 \_ 設大小 \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="e9bbc-159">MFPKEY 重 \_ 設大小 \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="e9bbc-160">MFPKEY 重 \_ 設大小 \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="e9bbc-161">MFPKEY 重 \_ 設大小 \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="e9bbc-162">MFPKEY 重 \_ 設大小 \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="e9bbc-163">MFPKEY \_ PIXELASPECTRATIO</span><span class="sxs-lookup"><span data-stu-id="e9bbc-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="e9bbc-164">備註</span><span class="sxs-lookup"><span data-stu-id="e9bbc-164">Remarks</span></span>

<span data-ttu-id="e9bbc-165">影片調整器 DSP 會實作為可做為 www.contoso.com 或 MFT 的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="e9bbc-166">此物件具有單一類別識別碼 (CLSID) ，不論它是否可作為一或一個 MFT。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="e9bbc-167">如需有關 DSP 作為一或是 MFT 之時機的詳細資訊，請參閱 [數位訊號處理器](windowsmediadigitalsignalprocessors.md)。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="e9bbc-168">針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據 DSP 是以 SQL-DMO 或 MFT 的方式而有所不同。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="e9bbc-169">非 RGB 媒體子類型的 Guid 是相同的，不論 DSP 是以 SQL-DMO 或 MFT 作為的。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="e9bbc-170">如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="e9bbc-171">這個 DSP 可以在影片影像上執行裁剪和縮放。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="e9bbc-172">輸出類型的格式必須符合輸入類型的格式。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="e9bbc-173">DSP 不會執行色彩空間轉換。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="e9bbc-174">設定輸出類型之前，您可以使用下表所列的屬性來定義下列任何區域。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="e9bbc-175">區域</span><span class="sxs-lookup"><span data-stu-id="e9bbc-175">Region</span></span>                   | <span data-ttu-id="e9bbc-176">屬性</span><span class="sxs-lookup"><span data-stu-id="e9bbc-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bbc-177">來源矩形</span><span class="sxs-lookup"><span data-stu-id="e9bbc-177">Source rectangle</span></span>         | <span data-ttu-id="e9bbc-178">MFPKEY \_ 調整 \_ SRC \_ 左方</span><span class="sxs-lookup"><span data-stu-id="e9bbc-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="e9bbc-179">MFPKEY \_ 調整 \_ SRC \_ TOP</span><span class="sxs-lookup"><span data-stu-id="e9bbc-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="e9bbc-180">MFPKEY \_ 調整 \_ SRC \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="e9bbc-181">MFPKEY \_ 調整 \_ SRC \_ 高度大小</span><span class="sxs-lookup"><span data-stu-id="e9bbc-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="e9bbc-182">目的地矩形</span><span class="sxs-lookup"><span data-stu-id="e9bbc-182">Destination rectangle</span></span>    | <span data-ttu-id="e9bbc-183">MFPKEY \_ 將 \_ DST \_ 左大小調整</span><span class="sxs-lookup"><span data-stu-id="e9bbc-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="e9bbc-184">MFPKEY \_ 調整 \_ DST \_ 頂端</span><span class="sxs-lookup"><span data-stu-id="e9bbc-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="e9bbc-185">MFPKEY \_ 調整 \_ DST \_ 寬度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="e9bbc-186">MFPKEY \_ 調整 \_ DST \_ 高度</span><span class="sxs-lookup"><span data-stu-id="e9bbc-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="e9bbc-187">幾何光圈</span><span class="sxs-lookup"><span data-stu-id="e9bbc-187">Geometric aperture</span></span>       | <span data-ttu-id="e9bbc-188">MFPKEY 重 \_ 設大小 \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="e9bbc-189">MFPKEY 重 \_ 設大小 \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="e9bbc-190">MFPKEY 重 \_ 設大小 \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="e9bbc-191">MFPKEY 重 \_ 設大小 \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="e9bbc-192">最小顯示光圈</span><span class="sxs-lookup"><span data-stu-id="e9bbc-192">Minimum display aperture</span></span> | <span data-ttu-id="e9bbc-193">MFPKEY 重 \_ 設大小 \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="e9bbc-194">MFPKEY 重 \_ 設大小 \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="e9bbc-195">MFPKEY 重 \_ 設大小 \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="e9bbc-196">MFPKEY 重 \_ 設大小 \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="e9bbc-197">Pan/掃描區域</span><span class="sxs-lookup"><span data-stu-id="e9bbc-197">Pan/scan region</span></span>          | <span data-ttu-id="e9bbc-198">MFPKEY 重 \_ 設大小 \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="e9bbc-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="e9bbc-199">MFPKEY 重 \_ 設大小 \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="e9bbc-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="e9bbc-200">MFPKEY 重 \_ 設大小 \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="e9bbc-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="e9bbc-201">MFPKEY 重 \_ 設大小 \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="e9bbc-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="e9bbc-202">在每個案例中，您必須設定所有相關聯的屬性，設定才會生效。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="e9bbc-203">DSP 會複製來源矩形所定義之來源影像的部分，並將它伸展或壓縮到輸出緩衝區上的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="e9bbc-204">來源和目的地矩形不需要相同的大小。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="e9bbc-205">輸出媒體類型中的框架大小必須夠大，才能容納目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="e9bbc-206">幾何光圈、最小顯示光圈和平移/掃描區域不會影響 DSP 調整影片的大小。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="e9bbc-207">不過，它們可能會影響下游元件解讀影片框架的方式。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="e9bbc-208">尤其是，增強型影片轉譯器 (EVR) 在計算圖片外觀比例和顯示區域時，會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="e9bbc-209">如果您使用媒體基礎媒體類型，則可以直接在輸出媒體類型中設定幾何光圈、最小顯示光圈和平移/掃描區域。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="e9bbc-210">否則，如果您使用的是 SQL-DMO 媒體類型，請使用屬性進行設定。</span><span class="sxs-lookup"><span data-stu-id="e9bbc-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="e9bbc-211">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="e9bbc-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="e9bbc-212">**MF \_ MT \_ 幾何 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="e9bbc-213">**MF \_ MT \_ 最小 \_ 顯示 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="e9bbc-214">**MF \_ MT \_ 平移 \_ 掃描 \_ 光圈**</span><span class="sxs-lookup"><span data-stu-id="e9bbc-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="e9bbc-215">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9bbc-215">Requirements</span></span>



| <span data-ttu-id="e9bbc-216">需求</span><span class="sxs-lookup"><span data-stu-id="e9bbc-216">Requirement</span></span> | <span data-ttu-id="e9bbc-217">值</span><span class="sxs-lookup"><span data-stu-id="e9bbc-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bbc-218">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9bbc-218">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bbc-219">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9bbc-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e9bbc-220">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9bbc-220">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bbc-221">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9bbc-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9bbc-222">標頭</span><span class="sxs-lookup"><span data-stu-id="e9bbc-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9bbc-223"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bbc-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="e9bbc-224">DLL</span><span class="sxs-lookup"><span data-stu-id="e9bbc-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9bbc-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9bbc-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9bbc-226">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9bbc-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bbc-227">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="e9bbc-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
