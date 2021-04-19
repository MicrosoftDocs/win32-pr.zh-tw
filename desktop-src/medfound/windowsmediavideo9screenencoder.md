---
description: Windows Media 視訊9螢幕編碼器最適合用來從電腦監視器編碼連續螢幕擷取畫面。
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: 'Windows Media 視訊9螢幕編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979534"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="a6ae4-103">Windows Media 視訊9螢幕編碼器</span><span class="sxs-lookup"><span data-stu-id="a6ae4-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="a6ae4-104">Windows Media 視訊9螢幕編碼器最適合用來從電腦監視器編碼連續螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a6ae4-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="a6ae4-105">Class Identifier</span></span>

<span data-ttu-id="a6ae4-106">Windows Media 視訊9螢幕編碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMSSCEncMediaObject2** 來表示。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="a6ae4-107">您可以藉由呼叫 **CoCreateInstance** 來建立編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="a6ae4-108">輸入類型</span><span class="sxs-lookup"><span data-stu-id="a6ae4-108">Input Types</span></span>

<span data-ttu-id="a6ae4-109">第9版螢幕編碼程式支援下列輸入類型，當它用來作為 DirectX 媒體物件時 (的) 。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="a6ae4-110">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a6ae4-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="a6ae4-111">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a6ae4-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="a6ae4-112">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="a6ae4-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="a6ae4-113">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a6ae4-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="a6ae4-114">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a6ae4-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="a6ae4-115">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a6ae4-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="a6ae4-116">當第9版的螢幕編碼器作為媒體基礎轉換 (MFT) 時，支援下列輸入類型。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="a6ae4-117">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="a6ae4-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="a6ae4-118">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="a6ae4-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="a6ae4-119">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="a6ae4-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="a6ae4-120">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="a6ae4-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="a6ae4-121">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="a6ae4-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="a6ae4-122">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="a6ae4-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="a6ae4-123">輸出型別</span><span class="sxs-lookup"><span data-stu-id="a6ae4-123">Output Types</span></span>

<span data-ttu-id="a6ae4-124">適用于 Windows Media 視訊螢幕第9版編碼內容的四個字元的程式碼 (FOURCC) 為 "MSS2"。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="a6ae4-125">第9版螢幕編碼器支援下列輸出類型。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="a6ae4-126">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="a6ae4-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="a6ae4-127">編碼器屬性</span><span class="sxs-lookup"><span data-stu-id="a6ae4-127">Encoder Properties</span></span>

<span data-ttu-id="a6ae4-128">Windows Media 視訊9螢幕編碼器支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a6ae4-129">屬性</span><span class="sxs-lookup"><span data-stu-id="a6ae4-129">Property</span></span></th>
<th><span data-ttu-id="a6ae4-130">描述</span><span class="sxs-lookup"><span data-stu-id="a6ae4-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a6ae4-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="a6ae4-132">以位元組為單位，指定用來儲存壓縮內容之容器所需的額外負荷（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="a6ae4-133">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-133">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-134">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="a6ae4-136">以毫秒為單位，以毫秒為單位，指定限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="a6ae4-137">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-137">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="a6ae4-140">以毫秒為單位，以毫秒為單位指定受限制的變數位速率 (VBR) 資料流程的尖峰位速率 (由 <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>) 指定。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="a6ae4-141">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-141">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-142">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="a6ae4-144">指定編碼的影片位資料流程是否包含每個主要畫面格的緩衝區填滿值。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="a6ae4-145">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-145">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-146">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="a6ae4-148">指定編解碼器編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="a6ae4-149">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-149">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-150">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="a6ae4-152">指定實際包含資料之編解碼器所編碼的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="a6ae4-153">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-153">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-154">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="a6ae4-156">這個屬性會由 <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>取代。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="a6ae4-158">指定編碼器演算法的複雜度。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="a6ae4-159">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="a6ae4-160">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="a6ae4-162">指定在編解碼器輸出中，動作平滑與影像品質之間的取捨的數值標記法。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="a6ae4-163">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-163">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-164">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="a6ae4-166">指定編碼期間卸載的影片框架數目。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="a6ae4-167">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-167">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-168">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="a6ae4-170">指定編碼傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="a6ae4-171">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-171">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-172">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="a6ae4-174">指定可識別您要使用之編碼器的 FOURCC。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="a6ae4-175">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-175">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-176">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="a6ae4-178">指定編解碼器輸出中主要畫面格之間的最長時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="a6ae4-179">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-179">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-180">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="a6ae4-182">已過時。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="a6ae4-184">指定編解碼器所支援的最大傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="a6ae4-185">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-185">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-186">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="a6ae4-188">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-188">Windows XP and later.</span></span> <span data-ttu-id="a6ae4-189">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-189">Read/write.</span></span><br/> <span data-ttu-id="a6ae4-190">指定編解碼器將用來編碼內容的傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="a6ae4-191">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-191">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-192">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="a6ae4-194">指定 QP。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-194">Specifies QP.</span></span> <span data-ttu-id="a6ae4-195">可能的值為1.0 到31.0。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="a6ae4-196">Windows Vista （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="a6ae4-197">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="a6ae4-199">指定平均位元速率（以每秒位數為單位），用於2次傳遞變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a6ae4-200">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-200">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-201">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="a6ae4-203">指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a6ae4-204">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-204">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-205">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="a6ae4-207">指定在編碼過程中傳遞給編碼器的影片畫面數。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="a6ae4-208">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-208">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-209">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="a6ae4-211">指定編解碼器是否會使用變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a6ae4-212">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-212">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-213">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a6ae4-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="a6ae4-215">指定以品質為基礎的實際品質層級 (1-傳遞) 可變位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="a6ae4-216">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-216">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-217">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a6ae4-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="a6ae4-219">可符合模型緩衝區的內容數量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="a6ae4-220">Windows XP 及更新版本，</span><span class="sxs-lookup"><span data-stu-id="a6ae4-220">Windows XP and later,</span></span><br />
<span data-ttu-id="a6ae4-221">唯寫。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a6ae4-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="a6ae4-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="a6ae4-223">指定已略過的影片畫面格數目，因為它們與先前的畫面格重複。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="a6ae4-224">Windows XP （含）以後版本。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-224">Windows XP and later.</span></span><br />
<span data-ttu-id="a6ae4-225">唯讀。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a6ae4-226">備註</span><span class="sxs-lookup"><span data-stu-id="a6ae4-226">Remarks</span></span>

<span data-ttu-id="a6ae4-227">螢幕編碼器物件會公開 **IMediaObject** 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 **IMFTransform** 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a6ae4-228">螢幕編碼器會根據您取得的介面和執行的 Windows 版本，以一或一種方式來運作。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a6ae4-229">下表所顯示的條件如下：螢幕編碼器的行為。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a6ae4-230">作業系統</span><span class="sxs-lookup"><span data-stu-id="a6ae4-230">Operating system</span></span>            | <span data-ttu-id="a6ae4-231">編碼器行為</span><span class="sxs-lookup"><span data-stu-id="a6ae4-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ae4-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6ae4-232">Windows XP</span></span>                  | <span data-ttu-id="a6ae4-233">Windows Media Screen 編碼器一律會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="a6ae4-234">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6ae4-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="a6ae4-235">Windows Media Screen 編碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="a6ae4-236">如果您在螢幕編碼器上取得 **IMFTransform** 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="a6ae4-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a6ae4-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6ae4-237">Requirements</span></span>



| <span data-ttu-id="a6ae4-238">需求</span><span class="sxs-lookup"><span data-stu-id="a6ae4-238">Requirement</span></span> | <span data-ttu-id="a6ae4-239">值</span><span class="sxs-lookup"><span data-stu-id="a6ae4-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ae4-240">用戶端</span><span class="sxs-lookup"><span data-stu-id="a6ae4-240">Client</span></span><br/> | <span data-ttu-id="a6ae4-241">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6ae4-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a6ae4-242">標頭</span><span class="sxs-lookup"><span data-stu-id="a6ae4-242">Header</span></span><br/> | <dl> <span data-ttu-id="a6ae4-243"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae4-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a6ae4-244">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ae4-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="a6ae4-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae4-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ae4-246">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6ae4-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ae4-247">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="a6ae4-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a6ae4-248">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="a6ae4-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="a6ae4-249">使用 Windows Media 視訊9螢幕編解碼器</span><span class="sxs-lookup"><span data-stu-id="a6ae4-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="a6ae4-250">Windows Media 視訊9螢幕解碼</span><span class="sxs-lookup"><span data-stu-id="a6ae4-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




