---
description: Windows Media 視訊9編碼器會編碼影片串流。
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: 'Windows Media 視訊9編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979535"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="41c8a-103">Windows Media 視訊9編碼器</span><span class="sxs-lookup"><span data-stu-id="41c8a-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="41c8a-104">Windows Media 視訊9編碼器會編碼影片串流。</span><span class="sxs-lookup"><span data-stu-id="41c8a-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="41c8a-105">編碼器支援下列四種編碼輸出的類別。</span><span class="sxs-lookup"><span data-stu-id="41c8a-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="41c8a-106">Windows Media 視訊9簡單的設定檔</span><span class="sxs-lookup"><span data-stu-id="41c8a-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="41c8a-107">Windows Media 視訊9主要設定檔</span><span class="sxs-lookup"><span data-stu-id="41c8a-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="41c8a-108">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="41c8a-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="41c8a-109">Windows Media 視訊9.1 影像</span><span class="sxs-lookup"><span data-stu-id="41c8a-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="41c8a-110">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="41c8a-110">Class Identifier</span></span>

<span data-ttu-id="41c8a-111">Windows Media 視訊編碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMV9EncMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="41c8a-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="41c8a-112">您可以藉由呼叫 **CoCreateInstance** 來建立影片編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="41c8a-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="41c8a-113">介面</span><span class="sxs-lookup"><span data-stu-id="41c8a-113">Interfaces</span></span>

<span data-ttu-id="41c8a-114">影片編碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="41c8a-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="41c8a-115">影片編碼器會根據您取得的介面和執行的 Windows 版本，以一或一種方式來運作。</span><span class="sxs-lookup"><span data-stu-id="41c8a-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="41c8a-116">下表顯示影片編碼器以 SQL-DMO 或 MFT 作為的條件。</span><span class="sxs-lookup"><span data-stu-id="41c8a-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="41c8a-117">作業系統</span><span class="sxs-lookup"><span data-stu-id="41c8a-117">Operating system</span></span>            | <span data-ttu-id="41c8a-118">編碼器行為</span><span class="sxs-lookup"><span data-stu-id="41c8a-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c8a-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41c8a-119">Windows XP</span></span>                  | <span data-ttu-id="41c8a-120">Windows Media video 編碼器一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="41c8a-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="41c8a-121">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="41c8a-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="41c8a-122">Windows Media 影片編碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="41c8a-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="41c8a-123">如果您在影片編碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="41c8a-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="41c8a-124">輸入格式</span><span class="sxs-lookup"><span data-stu-id="41c8a-124">Input Formats</span></span>

<span data-ttu-id="41c8a-125">當 Windows Media 視訊編碼器作為一種時，支援下列輸入媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="41c8a-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="41c8a-126">MEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="41c8a-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="41c8a-127">MEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="41c8a-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="41c8a-128">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="41c8a-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="41c8a-129">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="41c8a-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="41c8a-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="41c8a-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="41c8a-131">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="41c8a-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="41c8a-132">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="41c8a-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="41c8a-133">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="41c8a-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="41c8a-134">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="41c8a-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="41c8a-135">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="41c8a-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="41c8a-136">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="41c8a-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="41c8a-137">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="41c8a-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="41c8a-138">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="41c8a-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="41c8a-139">MEDIASUBTYPE \_ PHOTOMOTION</span><span class="sxs-lookup"><span data-stu-id="41c8a-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="41c8a-140">當 Windows Media 視訊編碼器作為 MFT 時，支援下列輸入媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="41c8a-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="41c8a-141">MFVideoFormat \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="41c8a-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="41c8a-142">MFVideoFormat \_ I420</span><span class="sxs-lookup"><span data-stu-id="41c8a-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="41c8a-143">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="41c8a-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="41c8a-144">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="41c8a-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="41c8a-145">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="41c8a-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="41c8a-146">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="41c8a-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="41c8a-147">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="41c8a-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="41c8a-148">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="41c8a-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="41c8a-149">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="41c8a-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="41c8a-150">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="41c8a-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="41c8a-151">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="41c8a-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="41c8a-152">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="41c8a-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="41c8a-153">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="41c8a-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="41c8a-154">MEDIASUBTYPE \_ PHOTOMOTION</span><span class="sxs-lookup"><span data-stu-id="41c8a-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="41c8a-155">輸出格式</span><span class="sxs-lookup"><span data-stu-id="41c8a-155">Output Formats</span></span>

<span data-ttu-id="41c8a-156">下表顯示對應至編碼輸出分類 (FOURCCs) 的四個字元的代碼。</span><span class="sxs-lookup"><span data-stu-id="41c8a-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="41c8a-157">類別</span><span class="sxs-lookup"><span data-stu-id="41c8a-157">Category</span></span>                               | <span data-ttu-id="41c8a-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="41c8a-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="41c8a-159">Windows Media 視訊9簡單的設定檔</span><span class="sxs-lookup"><span data-stu-id="41c8a-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="41c8a-160">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="41c8a-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="41c8a-161">Windows Media 視訊9主要設定檔</span><span class="sxs-lookup"><span data-stu-id="41c8a-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="41c8a-162">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="41c8a-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="41c8a-163">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="41c8a-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="41c8a-164">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="41c8a-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="41c8a-165">Windows Media 視訊9.1 影像</span><span class="sxs-lookup"><span data-stu-id="41c8a-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="41c8a-166">"WMVP" 代表9.1，"WVP2" 代表9.1 第2版</span><span class="sxs-lookup"><span data-stu-id="41c8a-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="41c8a-167">若要區分簡單的設定檔和主要設定檔，請設定 [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="41c8a-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="41c8a-168">屬性</span><span class="sxs-lookup"><span data-stu-id="41c8a-168">Properties</span></span>

<span data-ttu-id="41c8a-169">Windows Media 視訊9編碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="41c8a-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="41c8a-170">屬性</span><span class="sxs-lookup"><span data-stu-id="41c8a-170">Property</span></span></th>
<th><span data-ttu-id="41c8a-171">描述</span><span class="sxs-lookup"><span data-stu-id="41c8a-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41c8a-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-173">以位元組為單位，指定用來儲存壓縮內容的容器所需的額外負荷（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c8a-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="41c8a-174">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-174">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-175">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-176">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-178">指定影片內容的平均畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c8a-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="41c8a-179">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-179">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-180">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-181">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-183">以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="41c8a-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="41c8a-184">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-184">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-185">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-186">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-188">指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。</span><span class="sxs-lookup"><span data-stu-id="41c8a-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="41c8a-189">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-189">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-190">主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-191">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-193">以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="41c8a-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="41c8a-194">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-194">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-195">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-196">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-198">指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。</span><span class="sxs-lookup"><span data-stu-id="41c8a-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="41c8a-199">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-199">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-200">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-201">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-203">指定要在一組圖片的開頭使用的編碼模式。</span><span class="sxs-lookup"><span data-stu-id="41c8a-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="41c8a-204">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-205">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-206">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-208">指定編解碼器編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="41c8a-209">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-209">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-210">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-211">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-213">指定實際包含資料之編解碼器所編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="41c8a-214">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-214">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-215">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-216">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-218">這個屬性會由 <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>取代。</span><span class="sxs-lookup"><span data-stu-id="41c8a-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-220">指定編碼器演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="41c8a-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="41c8a-221">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-222">簡單設定檔，主要設定檔。</span><span class="sxs-lookup"><span data-stu-id="41c8a-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="41c8a-223">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-223">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-224">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-226">指定要用於 Windows Media 視訊 9 Advanced Profile 編解碼器的優化類型。</span><span class="sxs-lookup"><span data-stu-id="41c8a-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="41c8a-227">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-227">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-228">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-229">寫入。</span><span class="sxs-lookup"><span data-stu-id="41c8a-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-231">指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。</span><span class="sxs-lookup"><span data-stu-id="41c8a-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="41c8a-232">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-232">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-233">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-234">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-236">未使用。</span><span class="sxs-lookup"><span data-stu-id="41c8a-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-238">指定編碼內容符合的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="41c8a-239">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-239">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-240">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-241">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-243">指定您想要用於影片編碼的裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-244">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-244">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-245">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-246">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-248">指定用來對動作向量資訊進行編碼的方法。</span><span class="sxs-lookup"><span data-stu-id="41c8a-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="41c8a-249">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-249">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-250">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-251">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-253">指定編解碼器是否會在編碼時使用雜訊篩選器。</span><span class="sxs-lookup"><span data-stu-id="41c8a-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-254">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-254">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-255">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-256">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-258">針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼方式，指定所需的品質等級。</span><span class="sxs-lookup"><span data-stu-id="41c8a-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-259">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-260">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-261">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-263">指定編碼期間卸載的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-264">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-264">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-265">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-266">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-268">指定編碼傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="41c8a-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="41c8a-269">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-269">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-270">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-271">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-273">為編碼的影片指定中繼框架高度。</span><span class="sxs-lookup"><span data-stu-id="41c8a-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="41c8a-274">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-274">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-275">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-275">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-276">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-278">指定編碼影片的中繼框架寬度。</span><span class="sxs-lookup"><span data-stu-id="41c8a-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="41c8a-279">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-279">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-280">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-280">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-281">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-283">指定編解碼器是否應在編碼期間使用中位數篩選。</span><span class="sxs-lookup"><span data-stu-id="41c8a-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-284">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-284">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-285">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-286">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-288">指定可識別您要使用之編碼器的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="41c8a-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="41c8a-289">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-289">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-290">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-291">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-293">已過時。</span><span class="sxs-lookup"><span data-stu-id="41c8a-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-295">指定是否允許編碼器卸載框架。</span><span class="sxs-lookup"><span data-stu-id="41c8a-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="41c8a-296">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-296">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-297">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-298">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-300">指定是否要將編解碼器輸出交錯。</span><span class="sxs-lookup"><span data-stu-id="41c8a-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="41c8a-301">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-301">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-302">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-302">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-303">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-305">指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c8a-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="41c8a-306">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-306">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-307">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-308">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-310">未使用。</span><span class="sxs-lookup"><span data-stu-id="41c8a-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-312">指定在將目前的框架編碼之前，編解碼器將評估之目前畫面格的框架數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="41c8a-313">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-313">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-314">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-315">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-317">指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。</span><span class="sxs-lookup"><span data-stu-id="41c8a-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-318">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-318">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-319">主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-320">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-322">指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。</span><span class="sxs-lookup"><span data-stu-id="41c8a-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="41c8a-323">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-323">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-324">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-325">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-327">指定要用於動作比對的方法。</span><span class="sxs-lookup"><span data-stu-id="41c8a-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="41c8a-328">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-328">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-329">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-330">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-332">指定用於移動搜尋作業的影片資訊類型。</span><span class="sxs-lookup"><span data-stu-id="41c8a-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="41c8a-333">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-333">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-334">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-335">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-337">指定用於移動搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="41c8a-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="41c8a-338">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-338">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-339">主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-340">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-342">指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。</span><span class="sxs-lookup"><span data-stu-id="41c8a-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="41c8a-343">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-343">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-344">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-345">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-347">指定 (B 框架) 的雙向預測框架數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="41c8a-348">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-348">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-349">主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-350">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-352">指定編解碼器將用於編碼的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-353">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-353">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-354">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-355">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-357">指定編解碼器所支援的最大傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="41c8a-358">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-358">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-359">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-360">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-362">指定編解碼器將用來編碼內容的傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="41c8a-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="41c8a-363">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-363">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-364">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-365">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-367">指定編解碼器在編碼時是否應該使用保守感知優化。</span><span class="sxs-lookup"><span data-stu-id="41c8a-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-368">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-368">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-369">主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-370">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-372">指定編碼器是否會在位流中產生重複框架的虛擬框架專案。</span><span class="sxs-lookup"><span data-stu-id="41c8a-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="41c8a-373">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-373">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-374">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-375">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-377">指定 QP。</span><span class="sxs-lookup"><span data-stu-id="41c8a-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="41c8a-378">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-379">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-380">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-382">指定編解碼器應減少影片有效色彩範圍的程度。</span><span class="sxs-lookup"><span data-stu-id="41c8a-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="41c8a-383">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-383">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-384">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-384">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-385">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-387">指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="41c8a-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-388">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-388">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-389">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-390">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-392">指定編碼器是否使用以 RD 為基礎的子圖元 MV 搜尋。</span><span class="sxs-lookup"><span data-stu-id="41c8a-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="41c8a-393">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-393">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-394">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-395">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-397">若為區段重新編碼，則指定緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="41c8a-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="41c8a-398">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-399">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-400">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-402">若為區段重新編碼，則指定要重新編碼之區段的持續時間。</span><span class="sxs-lookup"><span data-stu-id="41c8a-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="41c8a-403">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-404">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-405">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-407">針對區段重新編碼，指定開始區段之前的框架 quantizer。</span><span class="sxs-lookup"><span data-stu-id="41c8a-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="41c8a-408">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-409">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-410">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-412">若為區段重新編碼，則指定起始緩衝區飽和度。</span><span class="sxs-lookup"><span data-stu-id="41c8a-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="41c8a-413">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-414">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-415">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-417">指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 。</span><span class="sxs-lookup"><span data-stu-id="41c8a-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="41c8a-418">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-418">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-419">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-420">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-422">指定在編碼過程中傳遞給編碼器的影片畫面數。</span><span class="sxs-lookup"><span data-stu-id="41c8a-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="41c8a-423">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-423">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-424">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-425">唯讀。</span><span class="sxs-lookup"><span data-stu-id="41c8a-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-427">指定編解碼器是否會使用變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="41c8a-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-428">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-428">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-429">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-430">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41c8a-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-432">指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="41c8a-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="41c8a-433">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-433">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-434">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-435">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-437">指定編解碼器是否會使用影片調整優化。</span><span class="sxs-lookup"><span data-stu-id="41c8a-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="41c8a-438">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-438">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-439">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-440">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-442">指定可符合模型緩衝區的內容數量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="41c8a-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="41c8a-443">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-443">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-444">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-444">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-445">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-447">若為區段重新編碼，則指定要重新編碼之檔案的編解碼器私用資料。</span><span class="sxs-lookup"><span data-stu-id="41c8a-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="41c8a-448">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="41c8a-449">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="41c8a-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="41c8a-450">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c8a-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-452">指定編解碼器將用來偵測交錯式來源影片的邏輯類型。</span><span class="sxs-lookup"><span data-stu-id="41c8a-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="41c8a-453">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-453">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-454">Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-454">Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-455">唯寫。</span><span class="sxs-lookup"><span data-stu-id="41c8a-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c8a-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="41c8a-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="41c8a-457">指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。</span><span class="sxs-lookup"><span data-stu-id="41c8a-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="41c8a-458">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="41c8a-458">Windows XP and later.</span></span><br />
<span data-ttu-id="41c8a-459">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="41c8a-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="41c8a-460">唯讀</span><span class="sxs-lookup"><span data-stu-id="41c8a-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="41c8a-461">規格需求</span><span class="sxs-lookup"><span data-stu-id="41c8a-461">Requirements</span></span>



| <span data-ttu-id="41c8a-462">需求</span><span class="sxs-lookup"><span data-stu-id="41c8a-462">Requirement</span></span> | <span data-ttu-id="41c8a-463">值</span><span class="sxs-lookup"><span data-stu-id="41c8a-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c8a-464">用戶端</span><span class="sxs-lookup"><span data-stu-id="41c8a-464">Client</span></span><br/> | <span data-ttu-id="41c8a-465">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="41c8a-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="41c8a-466">標頭</span><span class="sxs-lookup"><span data-stu-id="41c8a-466">Header</span></span><br/> | <dl> <span data-ttu-id="41c8a-467"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="41c8a-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="41c8a-468">DLL</span><span class="sxs-lookup"><span data-stu-id="41c8a-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="41c8a-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c8a-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c8a-470">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41c8a-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c8a-471">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="41c8a-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="41c8a-472">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="41c8a-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
