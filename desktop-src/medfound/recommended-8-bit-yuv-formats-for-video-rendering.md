---
description: 適用于影片轉譯的建議8位 YUV 格式
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: 適用于影片轉譯的建議8位 YUV 格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691623"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="aa153-103">適用于影片轉譯的建議8位 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="aa153-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="aa153-104">Gary Sullivan 和 Stephen Estrop</span><span class="sxs-lookup"><span data-stu-id="aa153-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="aa153-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="aa153-105">Microsoft Corporation</span></span>

<span data-ttu-id="aa153-106">2002年4月，更新的2008年11月</span><span class="sxs-lookup"><span data-stu-id="aa153-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="aa153-107">本主題說明在 Windows 作業系統中，建議用於影片轉譯的8位 YUV 色彩格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="aa153-108">本文提供在 YUV 和 RGB 格式之間進行轉換的技巧，也提供 upsampling YUV 格式的技巧。</span><span class="sxs-lookup"><span data-stu-id="aa153-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="aa153-109">本文適用于在 Windows 中使用 YUV 影片解碼或轉譯的任何人。</span><span class="sxs-lookup"><span data-stu-id="aa153-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="aa153-110">簡介</span><span class="sxs-lookup"><span data-stu-id="aa153-110">Introduction</span></span>

<span data-ttu-id="aa153-111">整個影片產業都有定義許多的 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="aa153-112">本文說明在 Windows 中針對影片轉譯所建議的8位 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="aa153-113">建議您將「解碼器廠商」和「顯示廠商」支援本文中所述的格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="aa153-114">本文不會解決其他使用的 YUV 色彩，例如靜止攝影。</span><span class="sxs-lookup"><span data-stu-id="aa153-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="aa153-115">本文中所述的格式，全都使用8個位的每圖元位置來編碼 Y 通道 (也稱為 luma 通道) ，並使用每個樣本8個位來編碼每個 U 或 V 色度範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="aa153-116">不過，大部分的 YUV 格式平均都會使用小於24位的每個圖元，因為它們包含的樣本數較少，而 V 小於 Y。本文未涵蓋具有10位或更高 Y 通道的 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="aa153-117">基於本文的目的，「U」一詞相當於 Cb，而「V」一詞則相當於「Cr」。</span><span class="sxs-lookup"><span data-stu-id="aa153-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="aa153-118">本文章涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="aa153-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="aa153-119">[YUV 取樣](#yuv-sampling)。</span><span class="sxs-lookup"><span data-stu-id="aa153-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="aa153-120">描述最常見的 YUV 取樣技術。</span><span class="sxs-lookup"><span data-stu-id="aa153-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="aa153-121">[介面定義](#surface-definitions)。</span><span class="sxs-lookup"><span data-stu-id="aa153-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="aa153-122">描述建議的 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="aa153-123">[色彩空間和色度取樣率轉換](#color-space-and-chroma-sampling-rate-conversions)。</span><span class="sxs-lookup"><span data-stu-id="aa153-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="aa153-124">提供在 YUV 和 RGB 格式之間進行轉換，以及在不同的 YUV 格式之間進行轉換的一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="aa153-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="aa153-125">[識別媒體基礎中的 YUV 格式](#identifying-yuv-formats-in-media-foundation)。</span><span class="sxs-lookup"><span data-stu-id="aa153-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="aa153-126">說明如何在媒體基礎中描述 YUV 格式類型。</span><span class="sxs-lookup"><span data-stu-id="aa153-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="aa153-127">YUV 取樣</span><span class="sxs-lookup"><span data-stu-id="aa153-127">YUV Sampling</span></span>

<span data-ttu-id="aa153-128">色度通道的取樣率可能會比 luma 通道低，而不會大幅喪失感知品質。</span><span class="sxs-lookup"><span data-stu-id="aa153-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="aa153-129">稱為 "A:B： C" 標記法的標記法可用來描述取樣的頻率，以及相對於 Y 的取樣頻率：</span><span class="sxs-lookup"><span data-stu-id="aa153-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="aa153-130">4:4:4 表示不含色度通道的縮減。</span><span class="sxs-lookup"><span data-stu-id="aa153-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="aa153-131">4:2:2 表示2:1 水準縮小，不含垂直的縮減取樣。</span><span class="sxs-lookup"><span data-stu-id="aa153-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="aa153-132">每個掃描行都包含每兩個 U 或 V 範例的四個 Y 樣本。</span><span class="sxs-lookup"><span data-stu-id="aa153-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="aa153-133">4:2:0 表示2:1 水準縮小取樣，具有2:1 垂直縮減取樣。</span><span class="sxs-lookup"><span data-stu-id="aa153-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="aa153-134">4:1:1 表示4:1 水準縮小，不含垂直的縮減取樣。</span><span class="sxs-lookup"><span data-stu-id="aa153-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="aa153-135">每個掃描行都包含四個適用于您和 V 範例的 Y 範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="aa153-136">4:1:1 取樣與其他格式較不常見，在本文中不會詳細討論。</span><span class="sxs-lookup"><span data-stu-id="aa153-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="aa153-137">下圖顯示如何針對每個縮減取樣率取樣色度。</span><span class="sxs-lookup"><span data-stu-id="aa153-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="aa153-138">Luma 範例是以十字線表示，而色度樣本則是以圓圈表示。</span><span class="sxs-lookup"><span data-stu-id="aa153-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![圖1。](images/yuv-sampling-grids.png)

<span data-ttu-id="aa153-141">4:2:2 取樣的主要形式定義于 ITU-R 建議 BT. 601。</span><span class="sxs-lookup"><span data-stu-id="aa153-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="aa153-142">4:2:0 取樣有兩種常見的變化。</span><span class="sxs-lookup"><span data-stu-id="aa153-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="aa153-143">其中一種用於 MPEG-2 影片，而另一種則用於 MPEG-2 和 ITU-T 建議261和 .H。</span><span class="sxs-lookup"><span data-stu-id="aa153-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="aa153-144">相較于 MPEG-2 配置，在 MPEG-2 配置和針對4:2:2 和4:4:4 格式定義的取樣方格之間進行轉換比較容易。</span><span class="sxs-lookup"><span data-stu-id="aa153-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="aa153-145">基於這個理由，在 Windows 中偏好採用 MPEG-2 配置，且應視為4:2:0 格式的預設轉譯。</span><span class="sxs-lookup"><span data-stu-id="aa153-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="aa153-146">介面定義</span><span class="sxs-lookup"><span data-stu-id="aa153-146">Surface Definitions</span></span>

<span data-ttu-id="aa153-147">本節說明針對影片轉譯建議的8位 YUV 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="aa153-148">這些分為幾個類別：</span><span class="sxs-lookup"><span data-stu-id="aa153-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="aa153-149">4:4:4 格式，每圖元32位</span><span class="sxs-lookup"><span data-stu-id="aa153-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="aa153-150">4:2:2 格式，每圖元16個位</span><span class="sxs-lookup"><span data-stu-id="aa153-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="aa153-151">4:2:0 格式，每圖元16個位</span><span class="sxs-lookup"><span data-stu-id="aa153-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="aa153-152">4:2:0 格式，每圖元12個位</span><span class="sxs-lookup"><span data-stu-id="aa153-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="aa153-153">首先，您應該注意下列概念，以瞭解如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="aa153-154">*介面原點*。</span><span class="sxs-lookup"><span data-stu-id="aa153-154">*Surface origin*.</span></span> <span data-ttu-id="aa153-155">針對本文所述的 YUV 格式，原點 (0，0) 一律是表面的左上角。</span><span class="sxs-lookup"><span data-stu-id="aa153-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="aa153-156">*Stride*。</span><span class="sxs-lookup"><span data-stu-id="aa153-156">*Stride*.</span></span> <span data-ttu-id="aa153-157">表面的 stride （有時稱為「音調」）是指介面的寬度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="aa153-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="aa153-158">在左上角有一個表面原點，stride 一律是正數。</span><span class="sxs-lookup"><span data-stu-id="aa153-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="aa153-159">*對齊*。</span><span class="sxs-lookup"><span data-stu-id="aa153-159">*Alignment*.</span></span> <span data-ttu-id="aa153-160">表面的對齊是由圖形顯示器驅動程式來決定。</span><span class="sxs-lookup"><span data-stu-id="aa153-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="aa153-161">介面必須一律對齊 DWORD;也就是說，介面內的個別線條保證是源自32位 (DWORD) 界限。</span><span class="sxs-lookup"><span data-stu-id="aa153-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="aa153-162">根據硬體的需求而定，對齊可以大於32位。</span><span class="sxs-lookup"><span data-stu-id="aa153-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="aa153-163">壓縮格式與平面格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-163">Packed format versus planar format.</span></span> <span data-ttu-id="aa153-164">YUV 格式分為 *壓縮* 格式和 *平面* 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="aa153-165">在封裝格式中，Y、U 和 V 元件會儲存在單一陣列中。</span><span class="sxs-lookup"><span data-stu-id="aa153-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="aa153-166">圖元會組織成 macropixels 的群組，其版面配置取決於格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="aa153-167">在平面格式中，Y、U 和 V 元件會儲存為三個不同的平面。</span><span class="sxs-lookup"><span data-stu-id="aa153-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="aa153-168">本文中所述的每個 YUV 格式都有指派的 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="aa153-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="aa153-169">FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="aa153-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="aa153-170">4:4:4 (32 bpp) </span><span class="sxs-lookup"><span data-stu-id="aa153-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="aa153-171">AYUV</span><span class="sxs-lookup"><span data-stu-id="aa153-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="aa153-172">4:2:2 (16 bpp) </span><span class="sxs-lookup"><span data-stu-id="aa153-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="aa153-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="aa153-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="aa153-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="aa153-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="aa153-175">4:2:0 (16 bpp) </span><span class="sxs-lookup"><span data-stu-id="aa153-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="aa153-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="aa153-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="aa153-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="aa153-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="aa153-178">4:2:0 (12 bpp) </span><span class="sxs-lookup"><span data-stu-id="aa153-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="aa153-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="aa153-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="aa153-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="aa153-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="aa153-181">YV12</span><span class="sxs-lookup"><span data-stu-id="aa153-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="aa153-182">NV12</span><span class="sxs-lookup"><span data-stu-id="aa153-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="aa153-183">4:4:4 格式，每圖元32位</span><span class="sxs-lookup"><span data-stu-id="aa153-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="aa153-184">AYUV</span><span class="sxs-lookup"><span data-stu-id="aa153-184">AYUV</span></span>

<span data-ttu-id="aa153-185">建議您使用 FOURCC 程式碼 AYUV 的單一4:4:4 格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="aa153-186">這是一種壓縮格式，其中每個圖元會編碼為四個連續位元組，並依照下圖所示的順序排列。</span><span class="sxs-lookup"><span data-stu-id="aa153-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![[圖 2]](images/yuvformats01.gif)

<span data-ttu-id="aa153-189">標記為的位元組包含 Alpha 的值。</span><span class="sxs-lookup"><span data-stu-id="aa153-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="aa153-190">4:2:2 格式，每圖元16個位</span><span class="sxs-lookup"><span data-stu-id="aa153-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="aa153-191">建議採用兩種4:2:2 格式，但有下列 FOURCC 碼：</span><span class="sxs-lookup"><span data-stu-id="aa153-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="aa153-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="aa153-192">YUY2</span></span>
-   <span data-ttu-id="aa153-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="aa153-193">UYVY</span></span>

<span data-ttu-id="aa153-194">兩者都是封裝格式，其中每個 macropixel 都是以四個連續位元組編碼的兩個圖元。</span><span class="sxs-lookup"><span data-stu-id="aa153-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="aa153-195">如此一來，就會以2的因數將色度的水準縮減取樣。</span><span class="sxs-lookup"><span data-stu-id="aa153-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="aa153-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="aa153-196">YUY2</span></span>

<span data-ttu-id="aa153-197">在 YUY2 格式中，資料可視為不帶正負號的 **char** 值陣列，其中第一個位元組包含第一個 Y 樣本、第二個位元組包含第一個 U (Cb) 範例、第三個位元組包含第二個 y 樣本，而第四個位元組包含第一個 V (Cr) 範例，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="aa153-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![圖3。](images/yuvformats02.gif)

<span data-ttu-id="aa153-200">如果影像是以位元組由小到小的 **字** 值陣列來定址，則第一個 **單字** 會包含最不重要的位中的第一個 Y 樣本 (LSBs) 以及最有效位中的第一個 U (Cb) 範例 (MSBs) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="aa153-201">第二個 **單字** 包含 LSBs 中的第二個 Y 樣本，以及 MSBs 中的第一個 V (Cr) 範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="aa153-202">YUY2 是 Microsoft DirectX Video 加速 (DirectX VA) 慣用的4:2:2 像素格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="aa153-203">這應該是支援4:2:2 影片的 DirectX VA 加速器的中繼詞彙需求。</span><span class="sxs-lookup"><span data-stu-id="aa153-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="aa153-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="aa153-204">UYVY</span></span>

<span data-ttu-id="aa153-205">此格式與 YUY2 格式相同，不同之處在于位元組順序是反向的，也就是說，色度和 luma 位元組會翻轉 (圖 4) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="aa153-206">如果影像是以兩個位元組由小到大的 **單字** 值陣列來定址，則第一個 **單字** 會在 MSBs 中的 LSBs 和 Y0 中包含 U，而第二個 **單字** 則在 MSBs 中的 LSBs 和 Y1 中包含 V。</span><span class="sxs-lookup"><span data-stu-id="aa153-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![[圖 4]](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="aa153-209">4:2:0 格式，每圖元16個位</span><span class="sxs-lookup"><span data-stu-id="aa153-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="aa153-210">建議使用兩個 4:2:0 16 位的每個圖元 (bpp) 格式，但有下列 FOURCC 碼：</span><span class="sxs-lookup"><span data-stu-id="aa153-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="aa153-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="aa153-211">IMC1</span></span>
-   <span data-ttu-id="aa153-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="aa153-212">IMC3</span></span>

<span data-ttu-id="aa153-213">這兩種 YUV 格式都是平面格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="aa153-214">在水準和垂直維度中，會以兩個因數來 subsampled 色度通道。</span><span class="sxs-lookup"><span data-stu-id="aa153-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="aa153-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="aa153-215">IMC1</span></span>

<span data-ttu-id="aa153-216">所有 Y 範例都會先出現在記憶體中，做為不帶正負號之 **char** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="aa153-217">後面接著所有 V (Cr) 範例，然後所有 U (Cb) 範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="aa153-218">V 和 U 平面的 stride 與 Y 平面相同，因而產生未使用的記憶體區域（如 [圖 5] 所示）。</span><span class="sxs-lookup"><span data-stu-id="aa153-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="aa153-219">您和 V 平面必須在記憶體界限（這是16行的倍數）上啟動。</span><span class="sxs-lookup"><span data-stu-id="aa153-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="aa153-220">[圖 5] 顯示 352 x 240 影片框架的您和 V 原點。</span><span class="sxs-lookup"><span data-stu-id="aa153-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="aa153-221">您和 V 平面的起始位址計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="aa153-222">其中， *.py* 是記憶體陣列開頭的位元組指標，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="aa153-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![[圖 5]。](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="aa153-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="aa153-225">IMC3</span></span>

<span data-ttu-id="aa153-226">此格式與 IMC1 相同，不同之處在于您和 V 平面會交換，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="aa153-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![[圖 6]。](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="aa153-229">4:2:0 格式，每圖元12個位</span><span class="sxs-lookup"><span data-stu-id="aa153-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="aa153-230">建議使用四種 4:2:0 12-bpp 格式，但有下列 FOURCC 碼：</span><span class="sxs-lookup"><span data-stu-id="aa153-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="aa153-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="aa153-231">IMC2</span></span>
-   <span data-ttu-id="aa153-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="aa153-232">IMC4</span></span>
-   <span data-ttu-id="aa153-233">YV12</span><span class="sxs-lookup"><span data-stu-id="aa153-233">YV12</span></span>
-   <span data-ttu-id="aa153-234">NV12</span><span class="sxs-lookup"><span data-stu-id="aa153-234">NV12</span></span>

<span data-ttu-id="aa153-235">在這些格式中，會以兩個水準和垂直維度的因數來 subsampled 色度通道。</span><span class="sxs-lookup"><span data-stu-id="aa153-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="aa153-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="aa153-236">IMC2</span></span>

<span data-ttu-id="aa153-237">這種格式與 IMC1 相同，但有下列差異： V (Cr) 和 U (Cb) 行會在半跨距界限上交錯。</span><span class="sxs-lookup"><span data-stu-id="aa153-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="aa153-238">換句話說，在色度區域中的每個全 stride 線都會以一條 V 範例開始，後面接著一個從下半跨距界限開始的 U 個範例， (圖 7) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="aa153-239">此配置可讓您更有效率地使用位址空間，而不是 IMC1。</span><span class="sxs-lookup"><span data-stu-id="aa153-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="aa153-240">它會將色度位址空間剪下一半，因而將總位址空間減少25%。</span><span class="sxs-lookup"><span data-stu-id="aa153-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="aa153-241">在4:2:0 格式中，IMC2 是 NV12 之後第二個最優先的格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="aa153-242">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="aa153-242">The following image illustrates this process.</span></span>

![[圖 7]。](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="aa153-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="aa153-245">IMC4</span></span>

<span data-ttu-id="aa153-246">此格式與 IMC2 相同，不同之處在于 U (Cb) 和 V (Cr) 行已交換，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="aa153-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![圖8。](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="aa153-249">YV12</span><span class="sxs-lookup"><span data-stu-id="aa153-249">YV12</span></span>

<span data-ttu-id="aa153-250">所有 Y 範例都會先出現在記憶體中，做為不帶正負號之 **char** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="aa153-251">這個陣列緊接在所有 V (Cr) 範例中。</span><span class="sxs-lookup"><span data-stu-id="aa153-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="aa153-252">V 平面的 stride 是 Y 平面的一半跨距;而且，V 平面所包含的一半與 Y 平面的行數相同。</span><span class="sxs-lookup"><span data-stu-id="aa153-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="aa153-253">V 平面緊接在所有 U (Cb) 範例中，並以相同的 stride 和行數作為 V 平面，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="aa153-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![[圖 9]。](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="aa153-256">NV12</span><span class="sxs-lookup"><span data-stu-id="aa153-256">NV12</span></span>

<span data-ttu-id="aa153-257">所有的 Y 範例都會先顯示在記憶體中，做為不帶正負號的 **char** 值陣列，並具有偶數的行數。</span><span class="sxs-lookup"><span data-stu-id="aa153-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="aa153-258">Y 平面後面緊接著不帶正負號的 **char** 值陣列，其中包含封裝的 U (Cb) 和 V (Cr) 範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="aa153-259">當結合的 U-V 陣列定址為位元組由小到小的 **字** 值陣列時，LSBs 會包含 U 值，而 MSBs 則包含 V 值。</span><span class="sxs-lookup"><span data-stu-id="aa153-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="aa153-260">NV12 是適用于 DirectX VA 的慣用4:2:0 像素格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="aa153-261">這應該是支援4:2:0 影片的 DirectX VA 加速器的中繼詞彙需求。</span><span class="sxs-lookup"><span data-stu-id="aa153-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="aa153-262">下圖顯示 Y 平面以及包含封裝您和 V 範例的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![[圖 10]](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="aa153-265">色彩空間和色度取樣率轉換</span><span class="sxs-lookup"><span data-stu-id="aa153-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="aa153-266">本節提供在 YUV 和 RGB 之間進行轉換的指導方針，以及在某些不同的 YUV 格式之間進行轉換的指導方針。</span><span class="sxs-lookup"><span data-stu-id="aa153-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="aa153-267">在本節中，我們會考慮兩種 RGB 編碼配置： *8 位電腦 RGB*，也稱為 sRGB 或「全形」 rgb 和 *studio video rgb*，或「具有前端房間和 toe 房間的 rgb」。</span><span class="sxs-lookup"><span data-stu-id="aa153-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="aa153-268">這些定義如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-268">These are defined as follows:</span></span>

-   <span data-ttu-id="aa153-269">電腦 RGB 針對紅色、綠色和藍色的每個樣本使用8個位。</span><span class="sxs-lookup"><span data-stu-id="aa153-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="aa153-270">黑色由 R = G = B = 0 表示，白色則以 R = G = B = 255 表示。</span><span class="sxs-lookup"><span data-stu-id="aa153-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="aa153-271">Studio video RGB 會針對紅色、綠色和藍色的每個樣本使用一些位數 N，其中 N 是8個以上的值。</span><span class="sxs-lookup"><span data-stu-id="aa153-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="aa153-272">Studio video RGB 使用與電腦 RGB 不同的縮放比例，且具有位移。</span><span class="sxs-lookup"><span data-stu-id="aa153-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="aa153-273">黑色是由 R = G = B = 16 \* 2 ^ (n-1) ，而白色則由 r = g = b = 235 \* 2 ^ (N-8) 表示。</span><span class="sxs-lookup"><span data-stu-id="aa153-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="aa153-274">不過，實際值可能落在此範圍之外。</span><span class="sxs-lookup"><span data-stu-id="aa153-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="aa153-275">Studio video RGB 是 Windows 中適用于影片的慣用 RGB 定義，而電腦 RGB 則是適用于非影片應用程式的慣用 RGB 定義。</span><span class="sxs-lookup"><span data-stu-id="aa153-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="aa153-276">無論是哪一種形式的 RGB，chromaticity 座標都如同在 [RGB 色彩主要複本] 的定義中，709中所指定。</span><span class="sxs-lookup"><span data-stu-id="aa153-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="aa153-277">R、G 和 B 的 (x，y) 座標分別是 (0.64、0.33) 、 (0.30、0.60) 和 (0.15、0.06) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="aa153-278">參考白色是以座標 (0.3127、0.3290) D65。</span><span class="sxs-lookup"><span data-stu-id="aa153-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="aa153-279">名義 gamma 是 1/0.45 (大約 2.2) ，其中包含在 ITU-R BT. 709 中詳細定義精確的 gamma。</span><span class="sxs-lookup"><span data-stu-id="aa153-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="aa153-280">**RGB 和 4:4:4 YUV 之間的轉換**</span><span class="sxs-lookup"><span data-stu-id="aa153-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="aa153-281">我們會先描述 RGB 和 4:4:4 YUV 之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="aa153-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="aa153-282">若要將4:2:0 或 4:2:2 YUV 轉換成 RGB，建議您將 YUV 資料轉換為 4:4:4 YUV，然後從 4:4:4 YUV 轉換為 RGB。</span><span class="sxs-lookup"><span data-stu-id="aa153-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="aa153-283">AYUV 格式（4:4:4 格式）在 Y、U 和 V 範例中都會使用8個位。</span><span class="sxs-lookup"><span data-stu-id="aa153-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="aa153-284">您也可以針對某些應用程式，使用每個樣本超過8個位來定義 YUV。</span><span class="sxs-lookup"><span data-stu-id="aa153-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="aa153-285">已為數位視訊定義了 RGB 的兩個主要 YUV 轉換。</span><span class="sxs-lookup"><span data-stu-id="aa153-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="aa153-286">兩者都是以稱為「ITU-R 建議709」的規格為基礎。</span><span class="sxs-lookup"><span data-stu-id="aa153-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="aa153-287">第一個轉換是針對709中的 50-Hz 所定義的較舊的 YUV 形式。</span><span class="sxs-lookup"><span data-stu-id="aa153-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="aa153-288">它與 ITU-R 建議 BT. 601 中指定的關聯性相同，也就是舊名稱 CCIR 601。</span><span class="sxs-lookup"><span data-stu-id="aa153-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="aa153-289">您應將其視為標準定義電視解析度的慣用 YUV 格式 (720 x 576) 和較低解析度的影片。</span><span class="sxs-lookup"><span data-stu-id="aa153-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="aa153-290">它是以兩個常數的值為 *Kr* 和 *Kb* 的特性：</span><span class="sxs-lookup"><span data-stu-id="aa153-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="aa153-291">第二次轉換是針對709中的 60-Hz 所定義的較新的 YUV 格式，應視為 SDTV 上述影片解析度的慣用格式。</span><span class="sxs-lookup"><span data-stu-id="aa153-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="aa153-292">這兩個常數的特性具有不同的值：</span><span class="sxs-lookup"><span data-stu-id="aa153-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="aa153-293">從 RGB 轉換成 YUV 的定義方式如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="aa153-294">接著會取得 YUV 值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa153-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="aa153-295">其中</span><span class="sxs-lookup"><span data-stu-id="aa153-295">where</span></span>

-   <span data-ttu-id="aa153-296">M 是每個 YUV 樣本的位數 (M >= 8) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="aa153-297">Z 是黑色層級變數。</span><span class="sxs-lookup"><span data-stu-id="aa153-297">Z is the black-level variable.</span></span> <span data-ttu-id="aa153-298">若為電腦 RGB，Z 等於0。</span><span class="sxs-lookup"><span data-stu-id="aa153-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="aa153-299">針對 studio video RGB，Z 等於 16 \* 2 ^ (N-8) ，其中 N 是每個 RGB 範例的位數， (N >= 8) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="aa153-300">S 是調整變數。</span><span class="sxs-lookup"><span data-stu-id="aa153-300">S is the scaling variable.</span></span> <span data-ttu-id="aa153-301">若是電腦 RGB，S 等於255。</span><span class="sxs-lookup"><span data-stu-id="aa153-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="aa153-302">針對 studio video RGB，S 等於 219 \* 2 ^ (N-8) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="aa153-303">函數 floor (x) 傳回小於或等於 x 的最大整數。</span><span class="sxs-lookup"><span data-stu-id="aa153-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="aa153-304">函數 clip3 (x，y，z) 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="aa153-305">clip3 應該實作為函式，而不是預處理器宏;否則將會發生多個引數評估。</span><span class="sxs-lookup"><span data-stu-id="aa153-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="aa153-306">Y 範例表示亮度，而您和 V 範例分別代表藍色和紅色的色彩偏差。</span><span class="sxs-lookup"><span data-stu-id="aa153-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="aa153-307">Y 的名義範圍是 16 \* 2 ^ (m-8) 至 235 \* 2 ^ (M-8) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="aa153-308">黑色表示為 16 \* 2 ^ (M-8) ，白色則表示為 235 \* 2 ^ (M-8) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="aa153-309">您和 V 的名義範圍是 16 \* 2 ^ (m-8) 至 240 \* 2 ^ (M-8) ，值 128 \* 2 ^ (m-8) 表示中性的色度。</span><span class="sxs-lookup"><span data-stu-id="aa153-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="aa153-310">不過，實際的值可能落在這些範圍之外。</span><span class="sxs-lookup"><span data-stu-id="aa153-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="aa153-311">針對 studio video RGB 形式的輸入資料，必須要有剪輯作業，才能將您和 V 值放在0到 (2 ^ M) -1 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="aa153-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="aa153-312">如果輸入是電腦 RGB，則不需要剪切作業，因為轉換公式無法產生此範圍以外的值。</span><span class="sxs-lookup"><span data-stu-id="aa153-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="aa153-313">這些是沒有近似值的精確公式。</span><span class="sxs-lookup"><span data-stu-id="aa153-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="aa153-314">本檔中的所有內容都是從這些公式所衍生。</span><span class="sxs-lookup"><span data-stu-id="aa153-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="aa153-315">本節將描述下列轉換：</span><span class="sxs-lookup"><span data-stu-id="aa153-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="aa153-316">將 RGB888 轉換成 YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="aa153-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="aa153-317">將8位 YUV 轉換成 RGB888</span><span class="sxs-lookup"><span data-stu-id="aa153-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="aa153-318">將 4:2:0 YUV 轉換為 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="aa153-319">將 4:2:2 YUV 轉換為 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="aa153-320">將 4:2:0 YUV 轉換為 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="aa153-321">將 RGB888 轉換成 YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="aa153-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="aa153-322">在電腦 RGB 輸入和8位 BT. 601 YUV 輸出中，我們相信上一節中指定的公式可以合理地近似如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="aa153-323">這些公式會使用不超過8位 (不帶正負號) 精確度的係數來產生8位結果。</span><span class="sxs-lookup"><span data-stu-id="aa153-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="aa153-324">中繼結果最多需要16個位的精確度。</span><span class="sxs-lookup"><span data-stu-id="aa153-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="aa153-325">將8位 YUV 轉換成 RGB888</span><span class="sxs-lookup"><span data-stu-id="aa153-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="aa153-326">從原始的 RGB 到 YUV 公式，可以為 BT. 601 衍生下列關聯性。</span><span class="sxs-lookup"><span data-stu-id="aa153-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="aa153-327">因此，請提供：</span><span class="sxs-lookup"><span data-stu-id="aa153-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="aa153-328">將 YUV 轉換成 RGB 的公式可以衍生如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="aa153-329">其中 `clip()` 表示裁剪至0到255的範圍。 \[ \]</span><span class="sxs-lookup"><span data-stu-id="aa153-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="aa153-330">我們相信這些公式可以合理地逼近，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa153-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="aa153-331">這些公式使用的一些係數需要8個以上的精確度來產生每個8位的結果，而中繼結果將需要16位以上的精確度。</span><span class="sxs-lookup"><span data-stu-id="aa153-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="aa153-332">若要將4:2:0 或 4:2:2 YUV 轉換成 RGB，建議您將 YUV 資料轉換為 4:4:4 YUV，然後從 4:4:4 YUV 轉換為 RGB。</span><span class="sxs-lookup"><span data-stu-id="aa153-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="aa153-333">接下來的章節會提供將4:2:0 和4:2:2 格式轉換為4:4:4 的一些方法。</span><span class="sxs-lookup"><span data-stu-id="aa153-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="aa153-334">將 4:2:0 YUV 轉換為 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="aa153-335">將 4:2:0 YUV 轉換為 4:2:2 YUV 需要以兩個因數的垂直 upconversion。</span><span class="sxs-lookup"><span data-stu-id="aa153-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="aa153-336">本節說明執行 upconversion 的範例方法。</span><span class="sxs-lookup"><span data-stu-id="aa153-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="aa153-337">方法會假設影片圖片是漸進式掃描。</span><span class="sxs-lookup"><span data-stu-id="aa153-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="aa153-338">4:2:0 到4:2:2 交錯式掃描轉換程式呈現非典型的問題，而且很難實行。</span><span class="sxs-lookup"><span data-stu-id="aa153-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="aa153-339">本文無法解決將交錯式掃描從4:2:0 轉換至4:2:2 的問題。</span><span class="sxs-lookup"><span data-stu-id="aa153-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="aa153-340">讓輸入色度範例的每個垂直線都是 `Cin[]` 範圍從0到 n-1 的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="aa153-341">輸出影像的對應垂直線將會是 `Cout[]` 範圍從0到 2n-1 的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="aa153-342">若要轉換每一條垂直線，請執行下列程式：</span><span class="sxs-lookup"><span data-stu-id="aa153-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="aa153-343">其中剪輯 () 表示裁剪至0到255的範圍。 \[ \]</span><span class="sxs-lookup"><span data-stu-id="aa153-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="aa153-344">處理邊緣的方程式可透過數學方式簡化。</span><span class="sxs-lookup"><span data-stu-id="aa153-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="aa153-345">這會顯示在此表單中，以說明圖片邊緣的固定效果。</span><span class="sxs-lookup"><span data-stu-id="aa153-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="aa153-346">實際上，這個方法會將曲線插到四個連續的圖元上（加權至兩個最接近圖元的值），以計算每個遺漏值 ([圖 11]) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="aa153-347">此範例中使用的特定插補方法會使用稱為 Catmull-Rom 插補的已知方法（也稱為三倍整數插補），在半整數位置產生遺漏的範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![[圖 11]](images/yuvformats14.gif)

<span data-ttu-id="aa153-350">在「信號處理」詞彙中，垂直 upconversion 應該包含階段變換補償，以考慮4:2:0 取樣線的位置與每個其他4:2:2 取樣線的位置之間的輸出4:2:2 取樣方格， (相對於輸出取樣方格的) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="aa153-351">不過，引入此位移會增加產生範例所需的處理量，並使其無法從 upsampled 4:2:2 映射重建原始的4:2:0 範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="aa153-352">此外，也無法將影片直接解碼成4:2:2 介面，然後使用這些表面作為參考圖片，以解碼資料流程中的後續圖片。</span><span class="sxs-lookup"><span data-stu-id="aa153-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="aa153-353">因此，此處提供的方法不會考慮樣本的精確垂直對齊。</span><span class="sxs-lookup"><span data-stu-id="aa153-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="aa153-354">如此一來，在合理的圖片解析度上可能不會有太大的傷害。</span><span class="sxs-lookup"><span data-stu-id="aa153-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="aa153-355">如果您從使用261、.H 或 MPEG-2 影片中所定義之取樣方格的4:2:0 影片開始，輸出4:2:2 色度範例的階段也會與 luma 取樣方格上的間距相對的半圖元水準位移， (相對於4:2:2 色度取樣方格) 間距的四分之一圖元位移。</span><span class="sxs-lookup"><span data-stu-id="aa153-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="aa153-356">不過，4:2:0 影片的 MPEG-2 格式可能較常用於電腦，而且不會受到此問題的影響。</span><span class="sxs-lookup"><span data-stu-id="aa153-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="aa153-357">此外，在合理的圖片解析度上，差別可能不會有太大的傷害。</span><span class="sxs-lookup"><span data-stu-id="aa153-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="aa153-358">嘗試修正此問題，將會建立與垂直階段位移相關的相同問題類型。</span><span class="sxs-lookup"><span data-stu-id="aa153-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="aa153-359">將 4:2:2 YUV 轉換為 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="aa153-360">將 4:2:2 YUV 轉換為 4:4:4 YUV 需要以兩個因數水準 upconversion。</span><span class="sxs-lookup"><span data-stu-id="aa153-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="aa153-361">先前針對垂直 upconversion 所述的方法也可以套用到水準 upconversion。</span><span class="sxs-lookup"><span data-stu-id="aa153-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="aa153-362">針對 MPEG-2 和 ITU-R BT. 601 影片，這個方法會產生具有正確階段對齊的範例。</span><span class="sxs-lookup"><span data-stu-id="aa153-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="aa153-363">將 4:2:0 YUV 轉換為 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="aa153-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="aa153-364">若要將 4:2:0 YUV 轉換為 4:4:4 YUV，您只要遵循先前所述的兩種方法即可。</span><span class="sxs-lookup"><span data-stu-id="aa153-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="aa153-365">將4:2:0 影像轉換為4:2:2，然後將4:2:2 影像轉換為4:4:4。</span><span class="sxs-lookup"><span data-stu-id="aa153-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="aa153-366">您也可以切換這兩個 upconversion 程式的順序，因為作業的順序對結果的視覺品質並不重要。</span><span class="sxs-lookup"><span data-stu-id="aa153-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="aa153-367">其他 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="aa153-367">Other YUV Formats</span></span>

<span data-ttu-id="aa153-368">另外還有一些較不常用的 YUV 格式包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="aa153-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="aa153-369">AI44 是調色盤 YUV 格式，每個樣本8個位。</span><span class="sxs-lookup"><span data-stu-id="aa153-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="aa153-370">每個範例都包含4個最重要的位中的索引 (MSBs) ，以及4個最不重要的位中的 Alpha 值 (LSBs) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="aa153-371">索引指的是 YUV 調色板專案的陣列，這些專案必須在格式的媒體類型中定義。</span><span class="sxs-lookup"><span data-stu-id="aa153-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="aa153-372">此格式主要用於子圖片影像。</span><span class="sxs-lookup"><span data-stu-id="aa153-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="aa153-373">NV11 是4:1:1 平面格式，每圖元12個位。</span><span class="sxs-lookup"><span data-stu-id="aa153-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="aa153-374">Y 範例會先出現在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="aa153-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="aa153-375">Y 平面後面接著封裝 U (Cb) 和 V (Cr) 範例的陣列。</span><span class="sxs-lookup"><span data-stu-id="aa153-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="aa153-376">當結合的 U-V 陣列以位元組由小到大的 **單字** 值陣列來定址時，u 範例會包含在每個 **單字** 的 LSBs 中，而 V 範例會包含在 MSBs 中。</span><span class="sxs-lookup"><span data-stu-id="aa153-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="aa153-377"> (此記憶體配置類似于 NV12，雖然色度取樣不同。 ) </span><span class="sxs-lookup"><span data-stu-id="aa153-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="aa153-378">Y41P 是4:1:1 壓縮格式，每四個圖元的水準取樣。</span><span class="sxs-lookup"><span data-stu-id="aa153-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="aa153-379">每個 macropixel 都包含三個位元組的8個圖元，具有下列位元組配置： `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="aa153-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="aa153-380">Y41T 與 Y41P 相同，不同之處在于每個 Y 範例的最小位都指定了色度鍵 (0 = 透明，1 = 不透明) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="aa153-381">Y42T 與 UYVY 相同，不同之處在于每個 Y 範例的最小位都指定了色度鍵 (0 = 透明，1 = 不透明) 。</span><span class="sxs-lookup"><span data-stu-id="aa153-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="aa153-382">YVYU 相當於 YUYV，但您和 V 範例會交換。</span><span class="sxs-lookup"><span data-stu-id="aa153-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="aa153-383">在媒體基礎中識別 YUV 格式</span><span class="sxs-lookup"><span data-stu-id="aa153-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="aa153-384">本文中所述的每個 YUV 格式都有指派的 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="aa153-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="aa153-385">FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="aa153-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="aa153-386">有各種 C/c + + 宏，可讓您更輕鬆地在原始程式碼中宣告 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="aa153-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="aa153-387">例如， **MAKEFOURCC** 宏是在 Mmsystem 中宣告，而 **FCC** 宏則是在 Aviriff 中宣告。</span><span class="sxs-lookup"><span data-stu-id="aa153-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="aa153-388">使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="aa153-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="aa153-389">您也可以藉由反轉字元順序，直接將 FOURCC 程式碼宣告為字串常值。</span><span class="sxs-lookup"><span data-stu-id="aa153-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="aa153-390">例如：</span><span class="sxs-lookup"><span data-stu-id="aa153-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="aa153-391">需要反轉順序是必要的，因為 Windows 作業系統使用的是位元組由大到小的架構。</span><span class="sxs-lookup"><span data-stu-id="aa153-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="aa153-392">' Y ' = 0x59，' U ' = 0x55，' 2 ' = 0x32，因此 ' 2YUY ' 為0x32595559。</span><span class="sxs-lookup"><span data-stu-id="aa153-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="aa153-393">在媒體基礎中，格式是以主要類型 GUID 和子類型 GUID 來識別。</span><span class="sxs-lookup"><span data-stu-id="aa153-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="aa153-394">電腦影片格式的主要類型一律為 MFMediaType \_ video。</span><span class="sxs-lookup"><span data-stu-id="aa153-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="aa153-395">您可以將 FOURCC 程式碼對應至 GUID 來建立子類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa153-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="aa153-396">其中 `XXXXXXXX` 是 FOURCC 程式碼。</span><span class="sxs-lookup"><span data-stu-id="aa153-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="aa153-397">因此，YUY2 的子類型 GUID 為：</span><span class="sxs-lookup"><span data-stu-id="aa153-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="aa153-398">最常見的 YUV 格式 Guid 的常數定義于標頭檔 mfapi 中。</span><span class="sxs-lookup"><span data-stu-id="aa153-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="aa153-399">如需這些常數的清單，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="aa153-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa153-400">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa153-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa153-401">關於 YUV 影片</span><span class="sxs-lookup"><span data-stu-id="aa153-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="aa153-402">影片媒體類型</span><span class="sxs-lookup"><span data-stu-id="aa153-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



