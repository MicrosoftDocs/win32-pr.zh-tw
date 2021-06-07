---
description: 本主題介紹漸進式解碼，以及如何在應用程式中使用漸進式解碼。
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: 漸進式解碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b9708802b082a880f358b969d9dd4beb1e481
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443669"
---
# <a name="progressive-decoding-overview"></a><span data-ttu-id="3e24a-103">漸進式解碼總覽</span><span class="sxs-lookup"><span data-stu-id="3e24a-103">Progressive Decoding Overview</span></span>

<span data-ttu-id="3e24a-104">本主題介紹漸進式解碼，以及如何在應用程式中使用漸進式解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-104">This topic introduces progressive decoding and how to use progressive decoding in applications.</span></span> <span data-ttu-id="3e24a-105">它也會提供建立支援漸進解碼之編解碼器的指導方針。</span><span class="sxs-lookup"><span data-stu-id="3e24a-105">It also provides guidelines for creating codecs that support progressive decoding.</span></span>

<span data-ttu-id="3e24a-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="3e24a-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e24a-107">簡介</span><span class="sxs-lookup"><span data-stu-id="3e24a-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3e24a-108">什麼是漸進式解碼？</span><span class="sxs-lookup"><span data-stu-id="3e24a-108">What is Progressive Decoding?</span></span>](#what-is-progressive-decoding)
-   [<span data-ttu-id="3e24a-109">Windows 7 中的漸進解碼支援</span><span class="sxs-lookup"><span data-stu-id="3e24a-109">Progressive Decoding Support in Windows 7</span></span>](#progressive-decoding-support-in-windows-7)
-   [<span data-ttu-id="3e24a-110">JPEG 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-110">JPEG Progressive Decoding</span></span>](#jpeg-progressive-decoding)
-   [<span data-ttu-id="3e24a-111">PNG/GIF 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-111">PNG/GIF Progressive Decoding</span></span>](#pnggif-progressive-decoding)
    -   [<span data-ttu-id="3e24a-112">PNG 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-112">PNG Progressive Decoding</span></span>](#png-progressive-decoding)
    -   [<span data-ttu-id="3e24a-113">GIF 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-113">GIF Progressive Decoding</span></span>](#gif-progressive-decoding)
-   [<span data-ttu-id="3e24a-114">應用程式中的漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-114">Progressive Decoding in Applications</span></span>](#progressive-decoding-in-applications)
-   [<span data-ttu-id="3e24a-115">漸進式解碼的自訂編解碼器支援</span><span class="sxs-lookup"><span data-stu-id="3e24a-115">Custom Codec Support for Progressive Decoding</span></span>](#custom-codec-support-for-progressive-decoding)
-   [<span data-ttu-id="3e24a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e24a-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="3e24a-117">簡介</span><span class="sxs-lookup"><span data-stu-id="3e24a-117">Introduction</span></span>

<span data-ttu-id="3e24a-118">漸進式解碼能讓您在整個影像下載完成之前，以累加方式解碼和轉譯部分影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-118">Progressive decoding provides the ability to incrementally decode and render portions of an image before the entire image has finished downloading.</span></span> <span data-ttu-id="3e24a-119">這項功能可大幅改善使用者在從網際網路觀看影像時的體驗，因為使用者不需要等待整個映射下載，就可以開始進行解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-119">This feature greatly improves the user's experience when viewing images from the Internet, because the user does not have to wait for the entire image to download before decoding can begin.</span></span> <span data-ttu-id="3e24a-120">在下載整個影像之前，使用者可以看到有可用資料的影像預覽。</span><span class="sxs-lookup"><span data-stu-id="3e24a-120">Users are able to see an image preview with available data long before the entire image is downloaded.</span></span> <span data-ttu-id="3e24a-121">這項功能對於任何用來從網際網路或受限頻寬的資料來源來查看影像的應用程式而言是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="3e24a-121">This feature is essential for any application used to view images from the Internet or from data sources with limited bandwidth.</span></span>

<span data-ttu-id="3e24a-122">Windows 7 中的 Windows 影像處理元件 (WIC) 支援像是 JPEG、PNG 和 GIF 等常用影像格式的漸進式解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-122">The Windows Imaging Component (WIC) in Windows 7 supports progressive decoding of popular image formats such as JPEG, PNG, and GIF.</span></span> <span data-ttu-id="3e24a-123">WIC 也支援任何已啟用 WIC 的非 Microsoft 編解碼器，可執行漸進式解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-123">WIC also supports any WIC-enabled non-Microsoft codecs that implement progressive decoding.</span></span> <span data-ttu-id="3e24a-124">目前的 WIC 版本不支援漸進式編碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-124">Progressive encoding is not supported in the current release of WIC.</span></span> <span data-ttu-id="3e24a-125">本主題概要說明 Windows 7 中的漸進解碼，以及在您的應用程式中啟用漸進式解碼的程式。</span><span class="sxs-lookup"><span data-stu-id="3e24a-125">This topic outlines progressive decoding in Windows 7 and the procedure for enabling progressive decoding in your applications.</span></span>

## <a name="what-is-progressive-decoding"></a><span data-ttu-id="3e24a-126">什麼是漸進式解碼？</span><span class="sxs-lookup"><span data-stu-id="3e24a-126">What is Progressive Decoding?</span></span>

<span data-ttu-id="3e24a-127">漸進式解碼是能夠以累加方式將影像的部分從不完整的影像檔解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-127">Progressive decoding is the ability to incrementally decode portions of an image from an incomplete image file.</span></span> <span data-ttu-id="3e24a-128">傳統解碼需要完整的影像檔案，才能開始進行解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-128">Traditional decoding requires a complete image file before decoding can begin.</span></span> <span data-ttu-id="3e24a-129">漸進式解碼會在影像的漸進式層級下載完成之後開始。</span><span class="sxs-lookup"><span data-stu-id="3e24a-129">Progressive decoding starts after a progressive level of an image has finished downloading.</span></span> <span data-ttu-id="3e24a-130">此解碼器會對影像的目前漸進式層級執行解碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="3e24a-130">The decoder performs a decoding pass on the image's current progressive level.</span></span> <span data-ttu-id="3e24a-131">然後，它會在每一個漸進層級下載時，對影像執行多個解碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="3e24a-131">It then performs multiple decoding passes on the image as each progressive level is downloaded.</span></span> <span data-ttu-id="3e24a-132">每次解碼行程都會顯示更多影像，直到映射完全下載和解碼為止。</span><span class="sxs-lookup"><span data-stu-id="3e24a-132">Each decoding pass reveals more of the image until the image is fully downloaded and decoded.</span></span> <span data-ttu-id="3e24a-133">解碼完整映射所需的行程數目取決於影像檔案格式，以及用來建立映射的編碼程式。</span><span class="sxs-lookup"><span data-stu-id="3e24a-133">The number of passes required to decode a full image depends on the image file format and the encoding process used to create the image.</span></span>

<span data-ttu-id="3e24a-134">影像必須經過明確編碼，才能執行漸進式解碼，但並非所有影像格式都支援它。</span><span class="sxs-lookup"><span data-stu-id="3e24a-134">Images must be specifically encoded to implement progressive decoding, but not all image formats support it.</span></span> <span data-ttu-id="3e24a-135">下列清單摘要說明使用漸進式解碼的需求。</span><span class="sxs-lookup"><span data-stu-id="3e24a-135">The following list summarizes the requirements for using progressive decoding.</span></span>

-   <span data-ttu-id="3e24a-136">影像檔必須支援漸進式解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-136">The image file must support progressive decoding.</span></span> <span data-ttu-id="3e24a-137">大部分的影像格式都不支援漸進式解碼，雖然常用的影像格式是 JPEG、PNG 和 GIF。</span><span class="sxs-lookup"><span data-stu-id="3e24a-137">Most image formats do not support progressive decoding, although the popular image formats JPEG, PNG, and GIF do.</span></span>
-   <span data-ttu-id="3e24a-138">影像檔案必須編碼為漸進式影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-138">The image file must be encoded as a progressive image.</span></span> <span data-ttu-id="3e24a-139">使用漸進式影像編碼所建立的影像檔無法執行漸進式解碼，即使檔案格式也會支援它。</span><span class="sxs-lookup"><span data-stu-id="3e24a-139">Image files that were not created with the progressive image encoding cannot implement progressive decoding, even where the file format would otherwise support it.</span></span>
-   <span data-ttu-id="3e24a-140">支援漸進式解碼的編解碼器必須可用。</span><span class="sxs-lookup"><span data-stu-id="3e24a-140">A codec that supports progressive decoding must be available.</span></span> <span data-ttu-id="3e24a-141">如果編解碼器不支援漸進式解碼，則以漸進式影像編碼的影像將會解碼為傳統影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-141">If a codec does not support progressive decoding, an image encoded as a progressive image will be decoded as a traditional image.</span></span>

## <a name="progressive-decoding-support-in-windows-7"></a><span data-ttu-id="3e24a-142">Windows 7 中的漸進解碼支援</span><span class="sxs-lookup"><span data-stu-id="3e24a-142">Progressive Decoding Support in Windows 7</span></span>

<span data-ttu-id="3e24a-143">Windows 7 提供內建的編解碼器，可支援 JPEG、PNG 和 GIF 影像格式的漸進式解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-143">Windows 7 provides built-in codecs that support progressive decoding for JPEG, PNG, and GIF image formats.</span></span> <span data-ttu-id="3e24a-144">上述每個 Windows 7 編解碼器都會在映射上執行多個解碼傳遞。</span><span class="sxs-lookup"><span data-stu-id="3e24a-144">Each of these Windows 7 codecs perform multiple decoding passes on an image.</span></span> <span data-ttu-id="3e24a-145">每個傳遞都會對應至特定層級和已解碼的影像部分，最後會到達完整解碼的影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-145">Each pass corresponds to a particular level and portion of the image that is decoded, eventually leading to a fully decoded image.</span></span>

<span data-ttu-id="3e24a-146">每個影像格式都會以不同的方式處理漸進解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-146">Each image format handles progressive decoding in a different manner.</span></span> <span data-ttu-id="3e24a-147">下表提供有關漸進層級數目的資訊，以及 Windows 7 漸進解碼格式所支援的解碼方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e24a-147">The following table provides information about the number of progressive levels and the decoding method supported by the Windows 7 progressive decoding formats.</span></span> 

| <span data-ttu-id="3e24a-148">映像格式</span><span class="sxs-lookup"><span data-stu-id="3e24a-148">Image Format</span></span> | <span data-ttu-id="3e24a-149">支援的漸進層級數目</span><span class="sxs-lookup"><span data-stu-id="3e24a-149">Number of progressive levels supported</span></span> | <span data-ttu-id="3e24a-150">漸進式解碼方法</span><span class="sxs-lookup"><span data-stu-id="3e24a-150">Progressive decoding method</span></span> |
|--------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="3e24a-151">JPEG</span><span class="sxs-lookup"><span data-stu-id="3e24a-151">JPEG</span></span>         | <span data-ttu-id="3e24a-152">由影像定義</span><span class="sxs-lookup"><span data-stu-id="3e24a-152">Defined by Image</span></span>                       | <span data-ttu-id="3e24a-153">增加解析度</span><span class="sxs-lookup"><span data-stu-id="3e24a-153">Increasing resolution</span></span>       |
| <span data-ttu-id="3e24a-154">PNG</span><span class="sxs-lookup"><span data-stu-id="3e24a-154">PNG</span></span>          | <span data-ttu-id="3e24a-155">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-155">7</span></span>                                      | <span data-ttu-id="3e24a-156">交錯</span><span class="sxs-lookup"><span data-stu-id="3e24a-156">Interlacing</span></span>                 |
| <span data-ttu-id="3e24a-157">GIF</span><span class="sxs-lookup"><span data-stu-id="3e24a-157">GIF</span></span>          | <span data-ttu-id="3e24a-158">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-158">4</span></span>                                      | <span data-ttu-id="3e24a-159">交錯</span><span class="sxs-lookup"><span data-stu-id="3e24a-159">Interlacing</span></span>                 |



 

<span data-ttu-id="3e24a-160">此外，您可以藉由提供漸進式介面和方法的支援，在編解碼器中實作為漸進解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-160">In addition, progressive decoding can be implemented in codecs by providing support for progressive interfaces and methods.</span></span> <span data-ttu-id="3e24a-161">如果編解碼器不支援漸進解碼，則在呼叫這些方法時，應該會傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3e24a-161">If progressive decoding is not supported in a codec, then appropriate error messages should be returned if these methods are called.</span></span>

## <a name="jpeg-progressive-decoding"></a><span data-ttu-id="3e24a-162">JPEG 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-162">JPEG Progressive Decoding</span></span>

<span data-ttu-id="3e24a-163">JPEG 漸進式解碼會以更高的解析度呈現每個層級的影像資料，直到可以使用完整解析度的影像為止。</span><span class="sxs-lookup"><span data-stu-id="3e24a-163">JPEG progressive decoding presents image data at increasingly higher resolutions for each level, until the full-resolution image is available.</span></span> <span data-ttu-id="3e24a-164">影像的每個層級都會設定為提供不同的解決層級。</span><span class="sxs-lookup"><span data-stu-id="3e24a-164">Each level of the image is set to provide a different resolution level.</span></span> <span data-ttu-id="3e24a-165">由於有更多漸進層級可供使用，因此影像會以較高的解析度顯示，直到解析完整解析度的影像為止。</span><span class="sxs-lookup"><span data-stu-id="3e24a-165">As more progressive levels become available, the image is displayed at higher resolutions, until the full resolution image is resolved.</span></span>

<span data-ttu-id="3e24a-166">可用層級數目和每個層級所設定的解析度，完全取決於編碼的 JPEG。</span><span class="sxs-lookup"><span data-stu-id="3e24a-166">The number of available levels and the resolution set at each level depends entirely on the encoded JPEG.</span></span> <span data-ttu-id="3e24a-167">下列兩個影像顯示在兩個漸進層級的 JPEG 漸進式解碼範例。</span><span class="sxs-lookup"><span data-stu-id="3e24a-167">The following two images show an example of JPEG progressive decoding at two progressive levels.</span></span>

![jpeg 漸進式解碼範例](graphics/Progressive_JPEG_Comparison.jpg)

<span data-ttu-id="3e24a-169">左邊的影像會在累進層級0進行解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-169">The image on the left is decoded at progressive level 0.</span></span> <span data-ttu-id="3e24a-170">右邊的影像會在五個漸進式層級之後完整解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-170">The image on right is fully decoded after five progressive levels.</span></span>

## <a name="pnggif-progressive-decoding"></a><span data-ttu-id="3e24a-171">PNG/GIF 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-171">PNG/GIF Progressive Decoding</span></span>

<span data-ttu-id="3e24a-172">PNG 和 GIF 漸進式解碼都使用交錯式漸進式解碼方法。</span><span class="sxs-lookup"><span data-stu-id="3e24a-172">Both PNG and GIF progressive decoding use an interlaced progressive decoding method.</span></span> <span data-ttu-id="3e24a-173">這兩種格式的解碼程式都非常類似。</span><span class="sxs-lookup"><span data-stu-id="3e24a-173">The decoding process for both formats is very similar.</span></span>

### <a name="png-progressive-decoding"></a><span data-ttu-id="3e24a-174">PNG 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-174">PNG Progressive Decoding</span></span>

<span data-ttu-id="3e24a-175">PNG 影像檔提供七個漸進式層級進行解碼，如 PNG 規格中所述。</span><span class="sxs-lookup"><span data-stu-id="3e24a-175">PNG image files provide seven progressive levels for decoding, as described in the PNG specification.</span></span> <span data-ttu-id="3e24a-176">藉由在每次的解碼器行程上解碼指定的圖元模式來實作為 PNG 漸進解碼。</span><span class="sxs-lookup"><span data-stu-id="3e24a-176">PNG progressive decoding is implemented by decoding a specified pattern of pixels on each pass of the decoder.</span></span> <span data-ttu-id="3e24a-177">下表中的 PNG 規格的模式是在整個影像上進行複寫。</span><span class="sxs-lookup"><span data-stu-id="3e24a-177">The pattern in the following table from the PNG specification is replicated over the entire image.</span></span> <span data-ttu-id="3e24a-178">每個數位代表要將對應的圖元解碼的漸進式層級。</span><span class="sxs-lookup"><span data-stu-id="3e24a-178">Each number represents the progressive level in which the corresponding pixel will be decoded.</span></span>



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="3e24a-179">1</span><span class="sxs-lookup"><span data-stu-id="3e24a-179">1</span></span>   | <span data-ttu-id="3e24a-180">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-180">6</span></span>   | <span data-ttu-id="3e24a-181">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-181">4</span></span>   | <span data-ttu-id="3e24a-182">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-182">6</span></span>   | <span data-ttu-id="3e24a-183">2</span><span class="sxs-lookup"><span data-stu-id="3e24a-183">2</span></span>   | <span data-ttu-id="3e24a-184">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-184">6</span></span>   | <span data-ttu-id="3e24a-185">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-185">4</span></span>   | <span data-ttu-id="3e24a-186">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-186">6</span></span>   |
| <span data-ttu-id="3e24a-187">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-187">7</span></span>   | <span data-ttu-id="3e24a-188">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-188">7</span></span>   | <span data-ttu-id="3e24a-189">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-189">7</span></span>   | <span data-ttu-id="3e24a-190">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-190">7</span></span>   | <span data-ttu-id="3e24a-191">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-191">7</span></span>   | <span data-ttu-id="3e24a-192">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-192">7</span></span>   | <span data-ttu-id="3e24a-193">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-193">7</span></span>   | <span data-ttu-id="3e24a-194">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-194">7</span></span>   |
| <span data-ttu-id="3e24a-195">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-195">5</span></span>   | <span data-ttu-id="3e24a-196">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-196">6</span></span>   | <span data-ttu-id="3e24a-197">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-197">5</span></span>   | <span data-ttu-id="3e24a-198">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-198">6</span></span>   | <span data-ttu-id="3e24a-199">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-199">5</span></span>   | <span data-ttu-id="3e24a-200">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-200">6</span></span>   | <span data-ttu-id="3e24a-201">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-201">5</span></span>   | <span data-ttu-id="3e24a-202">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-202">6</span></span>   |
| <span data-ttu-id="3e24a-203">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-203">7</span></span>   | <span data-ttu-id="3e24a-204">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-204">7</span></span>   | <span data-ttu-id="3e24a-205">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-205">7</span></span>   | <span data-ttu-id="3e24a-206">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-206">7</span></span>   | <span data-ttu-id="3e24a-207">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-207">7</span></span>   | <span data-ttu-id="3e24a-208">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-208">7</span></span>   | <span data-ttu-id="3e24a-209">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-209">7</span></span>   | <span data-ttu-id="3e24a-210">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-210">7</span></span>   |
| <span data-ttu-id="3e24a-211">3</span><span class="sxs-lookup"><span data-stu-id="3e24a-211">3</span></span>   | <span data-ttu-id="3e24a-212">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-212">6</span></span>   | <span data-ttu-id="3e24a-213">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-213">4</span></span>   | <span data-ttu-id="3e24a-214">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-214">6</span></span>   | <span data-ttu-id="3e24a-215">3</span><span class="sxs-lookup"><span data-stu-id="3e24a-215">3</span></span>   | <span data-ttu-id="3e24a-216">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-216">6</span></span>   | <span data-ttu-id="3e24a-217">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-217">4</span></span>   | <span data-ttu-id="3e24a-218">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-218">6</span></span>   |
| <span data-ttu-id="3e24a-219">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-219">7</span></span>   | <span data-ttu-id="3e24a-220">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-220">7</span></span>   | <span data-ttu-id="3e24a-221">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-221">7</span></span>   | <span data-ttu-id="3e24a-222">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-222">7</span></span>   | <span data-ttu-id="3e24a-223">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-223">7</span></span>   | <span data-ttu-id="3e24a-224">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-224">7</span></span>   | <span data-ttu-id="3e24a-225">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-225">7</span></span>   | <span data-ttu-id="3e24a-226">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-226">7</span></span>   |
| <span data-ttu-id="3e24a-227">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-227">5</span></span>   | <span data-ttu-id="3e24a-228">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-228">6</span></span>   | <span data-ttu-id="3e24a-229">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-229">5</span></span>   | <span data-ttu-id="3e24a-230">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-230">6</span></span>   | <span data-ttu-id="3e24a-231">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-231">5</span></span>   | <span data-ttu-id="3e24a-232">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-232">6</span></span>   | <span data-ttu-id="3e24a-233">5</span><span class="sxs-lookup"><span data-stu-id="3e24a-233">5</span></span>   | <span data-ttu-id="3e24a-234">6</span><span class="sxs-lookup"><span data-stu-id="3e24a-234">6</span></span>   |
| <span data-ttu-id="3e24a-235">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-235">7</span></span>   | <span data-ttu-id="3e24a-236">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-236">7</span></span>   | <span data-ttu-id="3e24a-237">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-237">7</span></span>   | <span data-ttu-id="3e24a-238">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-238">7</span></span>   | <span data-ttu-id="3e24a-239">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-239">7</span></span>   | <span data-ttu-id="3e24a-240">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-240">7</span></span>   | <span data-ttu-id="3e24a-241">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-241">7</span></span>   | <span data-ttu-id="3e24a-242">7</span><span class="sxs-lookup"><span data-stu-id="3e24a-242">7</span></span>   |



 

<span data-ttu-id="3e24a-243">從上表中，您可以判斷每次傳遞的解碼器都會解碼的圖元。</span><span class="sxs-lookup"><span data-stu-id="3e24a-243">From the table above, you can determine the pixels that will be decoded with each pass of the decoder.</span></span> <span data-ttu-id="3e24a-244">與 Windows 7 GIF 編解碼器不同的是，Windows 7 PNG 編解碼器會將掃描行上最左邊的可用圖元複製到空的圖元。</span><span class="sxs-lookup"><span data-stu-id="3e24a-244">Unlike the Windows 7 GIF codec, the Windows 7 PNG codec replicates the left-most available pixel on a scan line to populate empty pixels.</span></span>

<span data-ttu-id="3e24a-245">下列影像顯示三個漸進式層級的 Windows 7 PNG 漸進解碼編解碼器範例。</span><span class="sxs-lookup"><span data-stu-id="3e24a-245">The following images show an example of the Windows 7 PNG progressive decoding codec at three progressive levels.</span></span>

![png 漸進式解碼範例](graphics/PNG_Progressive_Comparison.jpg)

<span data-ttu-id="3e24a-247">左上方的影像會顯示在漸進式層級0解碼的 PNG 影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-247">The image at the top left shows a PNG image decoded at progressive level 0.</span></span> <span data-ttu-id="3e24a-248">右上方的影像會顯示在漸進式層級3解碼的相同 PNG 影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-248">The top-right image shows the same PNG image decoded at progressive level 3.</span></span> <span data-ttu-id="3e24a-249">下圖顯示在7個漸進式層級之後完整解碼的相同影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-249">The bottom image shows the same image fully decoded after 7 progressive levels.</span></span>

### <a name="gif-progressive-decoding"></a><span data-ttu-id="3e24a-250">GIF 漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-250">GIF Progressive Decoding</span></span>

<span data-ttu-id="3e24a-251">GIF 影像檔提供四個漸進式層級進行解碼，如 GIF 規格中所述。</span><span class="sxs-lookup"><span data-stu-id="3e24a-251">GIF image files provide four progressive levels for decoding, as described in the GIF specification.</span></span> <span data-ttu-id="3e24a-252">每個階段都會填入影像內的特定資料列，並在第四次通過之後產生完整的影像。</span><span class="sxs-lookup"><span data-stu-id="3e24a-252">Each pass populates certain rows within an image, producing a full image after the fourth pass.</span></span> <span data-ttu-id="3e24a-253">下列來自 GIF 規格的表格會顯示每次傳遞的解碼時，所解碼的掃描行。</span><span class="sxs-lookup"><span data-stu-id="3e24a-253">The following table from the GIF specification shows which scan lines are decoded by each pass of the decoder.</span></span> 

| <span data-ttu-id="3e24a-254">層級編號/傳遞編號</span><span class="sxs-lookup"><span data-stu-id="3e24a-254">Level number/ pass number</span></span> | <span data-ttu-id="3e24a-255">已填入掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-255">Scan lines populated</span></span>   | <span data-ttu-id="3e24a-256">啟動掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-256">Starting scan line</span></span> |
|---------------------------|------------------------|--------------------|
| <span data-ttu-id="3e24a-257">1</span><span class="sxs-lookup"><span data-stu-id="3e24a-257">1</span></span>                         | <span data-ttu-id="3e24a-258">每八個掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-258">Every eighth scan line</span></span> | <span data-ttu-id="3e24a-259">0</span><span class="sxs-lookup"><span data-stu-id="3e24a-259">0</span></span>                  |
| <span data-ttu-id="3e24a-260">2</span><span class="sxs-lookup"><span data-stu-id="3e24a-260">2</span></span>                         | <span data-ttu-id="3e24a-261">每八個掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-261">Every eighth scan line</span></span> | <span data-ttu-id="3e24a-262">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-262">4</span></span>                  |
| <span data-ttu-id="3e24a-263">3</span><span class="sxs-lookup"><span data-stu-id="3e24a-263">3</span></span>                         | <span data-ttu-id="3e24a-264">每四次掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-264">Every fourth scan line</span></span> | <span data-ttu-id="3e24a-265">2</span><span class="sxs-lookup"><span data-stu-id="3e24a-265">2</span></span>                  |
| <span data-ttu-id="3e24a-266">4</span><span class="sxs-lookup"><span data-stu-id="3e24a-266">4</span></span>                         | <span data-ttu-id="3e24a-267">每秒掃描行</span><span class="sxs-lookup"><span data-stu-id="3e24a-267">Every second scan line</span></span> | <span data-ttu-id="3e24a-268">1</span><span class="sxs-lookup"><span data-stu-id="3e24a-268">1</span></span>                  |



 

<span data-ttu-id="3e24a-269">雖然編解碼器可以在任何特定層級指定空白圖元的內容，但是 Windows GIF 編解碼器會將填入的掃描行複寫到空白掃描行上方，以填入空的掃描行。</span><span class="sxs-lookup"><span data-stu-id="3e24a-269">Although codecs can specify the content of empty pixels at any particular level, the Windows GIF codec populates empty scan lines by replicating populated scan lines above the empty scan line.</span></span>

## <a name="progressive-decoding-in-applications"></a><span data-ttu-id="3e24a-270">應用程式中的漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="3e24a-270">Progressive Decoding in Applications</span></span>

<span data-ttu-id="3e24a-271">主要漸進式解碼介面是 [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="3e24a-271">The main progressive decoding interface is the [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) interface.</span></span> <span data-ttu-id="3e24a-272">若要取得介面的參考，請查詢影像框架 ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) 以進行 **IWICProgressiveLevelControl**。</span><span class="sxs-lookup"><span data-stu-id="3e24a-272">To obtain a reference to the interface, query an image frame ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) for **IWICProgressiveLevelControl**.</span></span> <span data-ttu-id="3e24a-273">然後可以從介面存取漸進式方法。</span><span class="sxs-lookup"><span data-stu-id="3e24a-273">Progressive methods can then be accessed from the interface.</span></span>

<span data-ttu-id="3e24a-274">下列程式碼提供在應用程式中使用漸進式解碼的範例。</span><span class="sxs-lookup"><span data-stu-id="3e24a-274">The code below provides an example for using progressive decoding in applications.</span></span>


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



<span data-ttu-id="3e24a-275">上述程式碼提供在大部分的應用程式中執行漸進式解碼所需的基本功能。</span><span class="sxs-lookup"><span data-stu-id="3e24a-275">The preceding code provides the basic functionality necessary for implementing progressive decoding in most applications.</span></span> <span data-ttu-id="3e24a-276">使用程式碼時，可以在影像圖元資料變成可用時存取漸進式層級。</span><span class="sxs-lookup"><span data-stu-id="3e24a-276">Using the code, progressive levels can be accessed as image pixel data becomes available.</span></span> <span data-ttu-id="3e24a-277">[**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel)函式會封鎖執行，直到要求的層級可用為止。</span><span class="sxs-lookup"><span data-stu-id="3e24a-277">The [**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) function blocks execution until the level being requested is available.</span></span>

## <a name="custom-codec-support-for-progressive-decoding"></a><span data-ttu-id="3e24a-278">漸進式解碼的自訂編解碼器支援</span><span class="sxs-lookup"><span data-stu-id="3e24a-278">Custom Codec Support for Progressive Decoding</span></span>

<span data-ttu-id="3e24a-279">如果客戶的影像格式支援漸進式解碼，則編解碼器開發人員可能會選擇執行 [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) 。</span><span class="sxs-lookup"><span data-stu-id="3e24a-279">Codec developers may choose to implement the [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) if their image formats support progressive decoding.</span></span> <span data-ttu-id="3e24a-280">對漸進式解碼的支援不是 WIC 探索和仲裁的需求。</span><span class="sxs-lookup"><span data-stu-id="3e24a-280">Support for progressive decoding is not a requirement for discovery and arbitration by WIC.</span></span> <span data-ttu-id="3e24a-281">不過，漸進式解碼可大幅增強使用者體驗，並應盡可能考慮執行。</span><span class="sxs-lookup"><span data-stu-id="3e24a-281">However, progressive decoding greatly enhances the user experience, and implementation should be considered if possible.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e24a-282">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e24a-282">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3e24a-283">**概念**</span><span class="sxs-lookup"><span data-stu-id="3e24a-283">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e24a-284">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="3e24a-284">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

<span data-ttu-id="3e24a-285">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="3e24a-285">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3e24a-286">Continuous-Tone 的數位壓縮和編碼仍然是影像-需求和指導方針</span><span class="sxs-lookup"><span data-stu-id="3e24a-286">Digital Compression and Coding of Continuous-Tone Still Images - Requirements and Guidelines</span></span>](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[<span data-ttu-id="3e24a-287">JPEG 檔案交換格式</span><span class="sxs-lookup"><span data-stu-id="3e24a-287">JPEG File Interchange Format</span></span>](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[<span data-ttu-id="3e24a-288">GIF89a 規格</span><span class="sxs-lookup"><span data-stu-id="3e24a-288">GIF89a Specification</span></span>](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[<span data-ttu-id="3e24a-289">可移植網狀圖形 (PNG) 規格和延伸模組</span><span class="sxs-lookup"><span data-stu-id="3e24a-289">Portable Network Graphics (PNG) Specification and Extensions</span></span>](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



