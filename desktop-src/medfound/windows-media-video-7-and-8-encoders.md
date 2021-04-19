---
description: Windows Media 視訊7/8 編碼器會實施舊版的 Windows Media 視訊編碼器。
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: 'Windows Media 視訊7/8 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999708"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="c9344-103">Windows Media 視訊7/8 編碼器</span><span class="sxs-lookup"><span data-stu-id="c9344-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="c9344-104">Windows Media 視訊7/8 編碼器會實施舊版的 Windows Media 視訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="c9344-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="c9344-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="c9344-105">Class Identifier</span></span>

<span data-ttu-id="c9344-106">Windows Media 視訊7/8 編碼器 (CLSID) 的類別識別碼是 **clsid \_ CWMVXEncMediaObject**。</span><span class="sxs-lookup"><span data-stu-id="c9344-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="c9344-107">您可以藉由呼叫 **CoCreateInstance** 來建立編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="c9344-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="c9344-108">介面</span><span class="sxs-lookup"><span data-stu-id="c9344-108">Interfaces</span></span>

<span data-ttu-id="c9344-109">影片編碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="c9344-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="c9344-110">影片編碼器會根據您取得的介面和執行的 Windows 版本，以一或一種方式來運作。</span><span class="sxs-lookup"><span data-stu-id="c9344-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="c9344-111">下表顯示影片編碼器以 SQL-DMO 或 MFT 作為的條件。</span><span class="sxs-lookup"><span data-stu-id="c9344-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="c9344-112">作業系統</span><span class="sxs-lookup"><span data-stu-id="c9344-112">Operating system</span></span>            | <span data-ttu-id="c9344-113">編碼器行為</span><span class="sxs-lookup"><span data-stu-id="c9344-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9344-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9344-114">Windows XP</span></span>                  | <span data-ttu-id="c9344-115">Windows Media video 編碼器一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="c9344-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="c9344-116">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9344-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="c9344-117">Windows Media 影片編碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="c9344-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="c9344-118">如果您在影片編碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="c9344-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="c9344-119">輸入格式</span><span class="sxs-lookup"><span data-stu-id="c9344-119">Input Formats</span></span>

<span data-ttu-id="c9344-120">當 Windows Media 視訊編碼器作為一種時，支援下列輸入媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="c9344-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="c9344-121">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="c9344-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="c9344-122">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="c9344-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="c9344-123">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="c9344-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="c9344-124">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="c9344-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="c9344-125">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="c9344-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="c9344-126">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="c9344-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="c9344-127">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="c9344-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="c9344-128">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="c9344-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="c9344-129">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="c9344-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="c9344-130">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="c9344-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="c9344-131">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="c9344-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="c9344-132">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="c9344-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="c9344-133">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="c9344-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="c9344-134">MEDIASUBTYPE \_ PHOTOMOTION</span><span class="sxs-lookup"><span data-stu-id="c9344-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="c9344-135">當 Windows Media 視訊編碼器作為 MFT 時，支援下列輸入媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="c9344-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="c9344-136">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="c9344-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="c9344-137">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="c9344-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="c9344-138">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="c9344-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="c9344-139">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="c9344-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="c9344-140">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="c9344-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="c9344-141">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="c9344-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="c9344-142">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="c9344-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="c9344-143">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="c9344-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="c9344-144">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="c9344-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="c9344-145">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="c9344-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="c9344-146">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="c9344-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="c9344-147">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="c9344-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="c9344-148">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="c9344-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="c9344-149">MEDIASUBTYPE \_ PHOTOMOTION</span><span class="sxs-lookup"><span data-stu-id="c9344-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="c9344-150">輸出格式</span><span class="sxs-lookup"><span data-stu-id="c9344-150">Output Formats</span></span>

<span data-ttu-id="c9344-151">下錶針對 Windows Media 視訊7/8 編碼器所支援的輸出類型，顯示四個字元的代碼 (FOURCCs) 。</span><span class="sxs-lookup"><span data-stu-id="c9344-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="c9344-152">類別</span><span class="sxs-lookup"><span data-stu-id="c9344-152">Category</span></span>              | <span data-ttu-id="c9344-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c9344-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="c9344-154">Windows Media 視訊7</span><span class="sxs-lookup"><span data-stu-id="c9344-154">Windows Media Video 7</span></span> | <span data-ttu-id="c9344-155">"WMV1"</span><span class="sxs-lookup"><span data-stu-id="c9344-155">"WMV1"</span></span> |
| <span data-ttu-id="c9344-156">Windows Media 視訊8</span><span class="sxs-lookup"><span data-stu-id="c9344-156">Windows Media Video 8</span></span> | <span data-ttu-id="c9344-157">"WMV2"</span><span class="sxs-lookup"><span data-stu-id="c9344-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="c9344-158">屬性</span><span class="sxs-lookup"><span data-stu-id="c9344-158">Properties</span></span>

<span data-ttu-id="c9344-159">Windows Media 視訊7/8 編碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c9344-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c9344-160">屬性</span><span class="sxs-lookup"><span data-stu-id="c9344-160">Property</span></span></th>
<th><span data-ttu-id="c9344-161">描述</span><span class="sxs-lookup"><span data-stu-id="c9344-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9344-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="c9344-163">以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9344-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="c9344-164">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-164">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-165">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="c9344-167">指定影片內容的平均畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9344-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="c9344-168">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-168">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-169">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="c9344-171">以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="c9344-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="c9344-172">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-172">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-173">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="c9344-175">以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="c9344-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="c9344-176">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-176">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-177">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="c9344-179">指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。</span><span class="sxs-lookup"><span data-stu-id="c9344-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="c9344-180">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-180">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-181">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-183">指定編解碼器編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="c9344-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="c9344-184">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-184">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-185">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-187">指定實際包含資料之編解碼器所編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="c9344-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="c9344-188">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-188">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-189">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="c9344-191">這個屬性會由 <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>取代。</span><span class="sxs-lookup"><span data-stu-id="c9344-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="c9344-193">指定編碼器演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="c9344-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="c9344-194">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="c9344-195">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="c9344-197">指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。</span><span class="sxs-lookup"><span data-stu-id="c9344-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="c9344-198">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-198">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-199">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="c9344-201">指定編碼內容符合的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="c9344-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="c9344-202">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-202">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-203">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="c9344-205">指定您想要用於影片編碼的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="c9344-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="c9344-206">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-206">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-207">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-209">指定編碼期間卸載的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="c9344-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="c9344-210">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-210">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-211">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="c9344-213">指定編碼傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="c9344-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="c9344-214">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-214">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-215">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="c9344-217">指定可識別您要使用之編碼器的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="c9344-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="c9344-218">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-218">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-219">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="c9344-221">指定是否要將編解碼器輸出交錯。</span><span class="sxs-lookup"><span data-stu-id="c9344-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="c9344-222">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-222">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-223">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="c9344-225">指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9344-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="c9344-226">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-226">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-227">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="c9344-229">指定編解碼器所支援的最大傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="c9344-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="c9344-230">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-230">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-231">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="c9344-233">指定編解碼器將用來編碼內容的傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="c9344-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="c9344-234">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-234">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-235">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-237">指定編碼器是否會在位流中產生重複框架的虛擬框架專案。</span><span class="sxs-lookup"><span data-stu-id="c9344-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="c9344-238">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-238">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-239">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="c9344-241">指定 QP。</span><span class="sxs-lookup"><span data-stu-id="c9344-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="c9344-242">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="c9344-243">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="c9344-245">指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="c9344-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c9344-246">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-246">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-247">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="c9344-249">指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 。</span><span class="sxs-lookup"><span data-stu-id="c9344-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="c9344-250">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-250">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-251">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-253">指定在編碼過程中傳遞給編碼器的影片畫面數。</span><span class="sxs-lookup"><span data-stu-id="c9344-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="c9344-254">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-254">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-255">唯讀。</span><span class="sxs-lookup"><span data-stu-id="c9344-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="c9344-257">指定編解碼器是否會使用變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="c9344-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c9344-258">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-258">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-259">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c9344-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="c9344-261">指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="c9344-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c9344-262">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-262">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-263">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9344-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="c9344-265">指定可符合模型緩衝區的內容數量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="c9344-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="c9344-266">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-266">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-267">唯寫。</span><span class="sxs-lookup"><span data-stu-id="c9344-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9344-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c9344-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c9344-269">指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。</span><span class="sxs-lookup"><span data-stu-id="c9344-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="c9344-270">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="c9344-270">Windows XP and later.</span></span><br />
<span data-ttu-id="c9344-271">唯讀</span><span class="sxs-lookup"><span data-stu-id="c9344-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c9344-272">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9344-272">Requirements</span></span>



| <span data-ttu-id="c9344-273">需求</span><span class="sxs-lookup"><span data-stu-id="c9344-273">Requirement</span></span> | <span data-ttu-id="c9344-274">值</span><span class="sxs-lookup"><span data-stu-id="c9344-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9344-275">用戶端</span><span class="sxs-lookup"><span data-stu-id="c9344-275">Client</span></span><br/> | <span data-ttu-id="c9344-276">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9344-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="c9344-277">標頭</span><span class="sxs-lookup"><span data-stu-id="c9344-277">Header</span></span><br/> | <dl> <span data-ttu-id="c9344-278"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9344-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="c9344-279">DLL</span><span class="sxs-lookup"><span data-stu-id="c9344-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="c9344-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9344-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9344-281">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9344-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9344-282">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="c9344-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="c9344-283">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="c9344-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="c9344-284">影片子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="c9344-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
