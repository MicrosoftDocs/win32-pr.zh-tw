---
description: Windows Media 視訊9解碼器會將 Windows Media 視訊編碼器編碼的影片串流解碼。
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: 'Windows Media 視訊9解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992992"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="8ee33-103">Windows Media 視訊9解碼器</span><span class="sxs-lookup"><span data-stu-id="8ee33-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="8ee33-104">Windows Media 視訊9解碼器會將 [**Windows Media 視訊編碼器**](windowsmediavideo9encoder.md)編碼的影片串流解碼。</span><span class="sxs-lookup"><span data-stu-id="8ee33-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="8ee33-105">編碼器和解碼器支援下列四種編碼影片類別。</span><span class="sxs-lookup"><span data-stu-id="8ee33-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="8ee33-106">Windows Media 視訊9簡單的設定檔</span><span class="sxs-lookup"><span data-stu-id="8ee33-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="8ee33-107">Windows Media 視訊9主要設定檔</span><span class="sxs-lookup"><span data-stu-id="8ee33-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="8ee33-108">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="8ee33-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="8ee33-109">Windows Media 視訊9.1 影像</span><span class="sxs-lookup"><span data-stu-id="8ee33-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="8ee33-110">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="8ee33-110">Class Identifier</span></span>

<span data-ttu-id="8ee33-111">Windows Media 視訊解碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CWMVDecMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="8ee33-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="8ee33-112">您可以藉由呼叫 **CoCreateInstance** 來建立影片解碼的實例。</span><span class="sxs-lookup"><span data-stu-id="8ee33-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="8ee33-113">介面</span><span class="sxs-lookup"><span data-stu-id="8ee33-113">Interfaces</span></span>

<span data-ttu-id="8ee33-114">影片解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="8ee33-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="8ee33-115">根據您取得的介面以及正在執行的 Windows 版本而定，影片解碼會以一或 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="8ee33-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="8ee33-116">下表顯示的是以 SQL-DMO 或 MFT 表示的影片解碼器行為的條件。</span><span class="sxs-lookup"><span data-stu-id="8ee33-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="8ee33-117">作業系統</span><span class="sxs-lookup"><span data-stu-id="8ee33-117">Operating system</span></span>            | <span data-ttu-id="8ee33-118">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="8ee33-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee33-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8ee33-119">Windows XP</span></span>                  | <span data-ttu-id="8ee33-120">Windows Media video 解碼器一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="8ee33-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="8ee33-121">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ee33-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="8ee33-122">根據預設，Windows Media video 解碼會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="8ee33-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="8ee33-123">如果您在視頻解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="8ee33-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="8ee33-124">從 Windows 7 開始，Windows Media 視訊的解碼器會實 [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="8ee33-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="8ee33-125">輸入格式</span><span class="sxs-lookup"><span data-stu-id="8ee33-125">Input Formats</span></span>

<span data-ttu-id="8ee33-126">下表顯示四個字元的代碼 (FOURCCs) ，其對應至 Windows Media 視訊的解碼器所支援的編碼輸入分類。</span><span class="sxs-lookup"><span data-stu-id="8ee33-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="8ee33-127">類別</span><span class="sxs-lookup"><span data-stu-id="8ee33-127">Category</span></span>                               | <span data-ttu-id="8ee33-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="8ee33-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="8ee33-129">Windows Media 視訊9簡單的設定檔</span><span class="sxs-lookup"><span data-stu-id="8ee33-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="8ee33-130">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="8ee33-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="8ee33-131">Windows Media 視訊9主要設定檔</span><span class="sxs-lookup"><span data-stu-id="8ee33-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="8ee33-132">"WMV3"</span><span class="sxs-lookup"><span data-stu-id="8ee33-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="8ee33-133">Windows Media 視訊 9 Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="8ee33-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="8ee33-134">"WVC1"</span><span class="sxs-lookup"><span data-stu-id="8ee33-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="8ee33-135">Windows Media 視訊9.1 影像</span><span class="sxs-lookup"><span data-stu-id="8ee33-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="8ee33-136">"WMVP" 代表9.1，"WVP2" 代表9.1 第2版</span><span class="sxs-lookup"><span data-stu-id="8ee33-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="8ee33-137">輸出格式</span><span class="sxs-lookup"><span data-stu-id="8ee33-137">Output Formats</span></span>

<span data-ttu-id="8ee33-138">當 Windows Media 視訊的解碼器作為一種時，可支援下列輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="8ee33-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="8ee33-139">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="8ee33-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="8ee33-140">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="8ee33-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="8ee33-141">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="8ee33-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="8ee33-142">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="8ee33-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="8ee33-143">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="8ee33-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="8ee33-144">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="8ee33-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="8ee33-145">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="8ee33-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="8ee33-146">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="8ee33-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="8ee33-147">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="8ee33-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="8ee33-148">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="8ee33-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="8ee33-149">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="8ee33-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="8ee33-150">當 Windows Media 視訊解碼器作為 MFT 時，支援下列輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="8ee33-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="8ee33-151">MFVideoFormat \_ NV12</span><span class="sxs-lookup"><span data-stu-id="8ee33-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="8ee33-152">MFVideoFormat \_ YV12</span><span class="sxs-lookup"><span data-stu-id="8ee33-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="8ee33-153">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="8ee33-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="8ee33-154">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="8ee33-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="8ee33-155">MFVideoFormat \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="8ee33-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="8ee33-156">MFVideoFormat \_ NV11</span><span class="sxs-lookup"><span data-stu-id="8ee33-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="8ee33-157">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="8ee33-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="8ee33-158">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="8ee33-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="8ee33-159">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="8ee33-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="8ee33-160">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="8ee33-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="8ee33-161">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="8ee33-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="8ee33-162">屬性</span><span class="sxs-lookup"><span data-stu-id="8ee33-162">Properties</span></span>

<span data-ttu-id="8ee33-163">Windows Media 視訊的解碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8ee33-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ee33-164">屬性</span><span class="sxs-lookup"><span data-stu-id="8ee33-164">Property</span></span></th>
<th><span data-ttu-id="8ee33-165">描述</span><span class="sxs-lookup"><span data-stu-id="8ee33-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ee33-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="8ee33-167">指定編解碼器是否將經過壓縮資料流程的交錯式影片框架解碼為漸進式框架。</span><span class="sxs-lookup"><span data-stu-id="8ee33-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="8ee33-168">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-168">Windows XP and later.</span></span><br />
<span data-ttu-id="8ee33-169">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="8ee33-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="8ee33-170">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ee33-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee33-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="8ee33-172">指定解碼器是否會使用 DirectX video 加速硬體（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8ee33-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="8ee33-173">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-173">Windows XP and later.</span></span><br />
<span data-ttu-id="8ee33-174">簡單設定檔、主要設定檔、Advanced Profile。</span><span class="sxs-lookup"><span data-stu-id="8ee33-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="8ee33-175">唯寫。</span><span class="sxs-lookup"><span data-stu-id="8ee33-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee33-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="8ee33-177">指定此解碼器的電源等級。</span><span class="sxs-lookup"><span data-stu-id="8ee33-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="8ee33-178">Windows 7。</span><span class="sxs-lookup"><span data-stu-id="8ee33-178">Windows 7.</span></span><br />
<span data-ttu-id="8ee33-179">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="8ee33-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="8ee33-180">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ee33-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee33-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="8ee33-182">指定解碼器是否應使用框架插補。</span><span class="sxs-lookup"><span data-stu-id="8ee33-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="8ee33-183">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-183">Windows XP and later.</span></span><br />
<span data-ttu-id="8ee33-184">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="8ee33-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="8ee33-185">唯寫。</span><span class="sxs-lookup"><span data-stu-id="8ee33-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee33-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="8ee33-187">指定此解碼器是否支援框架插補。</span><span class="sxs-lookup"><span data-stu-id="8ee33-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="8ee33-188">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-188">Windows XP and later.</span></span><br />
<span data-ttu-id="8ee33-189">簡單設定檔、主要設定檔、Advanced Profile、Image</span><span class="sxs-lookup"><span data-stu-id="8ee33-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="8ee33-190">唯讀。</span><span class="sxs-lookup"><span data-stu-id="8ee33-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee33-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="8ee33-192">指定此解碼器將使用的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8ee33-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="8ee33-193">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="8ee33-194">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="8ee33-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="8ee33-195">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8ee33-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ee33-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="8ee33-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="8ee33-197">指定此解碼器的後置處理模式。</span><span class="sxs-lookup"><span data-stu-id="8ee33-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="8ee33-198">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="8ee33-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="8ee33-199">簡單設定檔、主要設定檔、Advanced Profile、Image。</span><span class="sxs-lookup"><span data-stu-id="8ee33-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="8ee33-200">唯寫。</span><span class="sxs-lookup"><span data-stu-id="8ee33-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ee33-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="8ee33-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="8ee33-202">指定是否應清空解碼器。</span><span class="sxs-lookup"><span data-stu-id="8ee33-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="8ee33-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ee33-203">Windows 8</span></span><br />
<span data-ttu-id="8ee33-204">唯讀。</span><span class="sxs-lookup"><span data-stu-id="8ee33-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="8ee33-205">Windows Media 格式執行時間會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8ee33-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="8ee33-206">屬性類型為 <strong>VARIANT_BOOL</strong>。</span><span class="sxs-lookup"><span data-stu-id="8ee33-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="8ee33-207">如果此值為 <strong>VARIANT_TRUE</strong>，則應在不連續的情況下清空此解碼器。</span><span class="sxs-lookup"><span data-stu-id="8ee33-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="8ee33-208">如需有關清空 MFT 的詳細資訊，請參閱 <a href="basic-mft-processing-model.md">基本的 Mft 處理模型</a>。</span><span class="sxs-lookup"><span data-stu-id="8ee33-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ee33-209">若要查詢這個屬性，請使用 <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="8ee33-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8ee33-210">備註</span><span class="sxs-lookup"><span data-stu-id="8ee33-210">Remarks</span></span>

<span data-ttu-id="8ee33-211">Windows Media 視訊9解碼器所允許的最大解析度是4096x4096。</span><span class="sxs-lookup"><span data-stu-id="8ee33-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee33-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ee33-212">Requirements</span></span>



| <span data-ttu-id="8ee33-213">需求</span><span class="sxs-lookup"><span data-stu-id="8ee33-213">Requirement</span></span> | <span data-ttu-id="8ee33-214">值</span><span class="sxs-lookup"><span data-stu-id="8ee33-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee33-215">用戶端</span><span class="sxs-lookup"><span data-stu-id="8ee33-215">Client</span></span><br/> | <span data-ttu-id="8ee33-216">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ee33-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="8ee33-217">標頭</span><span class="sxs-lookup"><span data-stu-id="8ee33-217">Header</span></span><br/> | <dl> <span data-ttu-id="8ee33-218"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee33-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="8ee33-219">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee33-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="8ee33-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee33-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee33-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ee33-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee33-222">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="8ee33-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="8ee33-223">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="8ee33-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
