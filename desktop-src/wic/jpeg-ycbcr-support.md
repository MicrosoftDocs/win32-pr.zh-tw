---
description: 從 Windows 8.1 開始，Windows 影像處理元件 (WIC) JPEG 編解碼器可支援在其原生 YCbCr 表單中讀取和寫入影像資料。
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: JPEG YCbCr 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944312"
---
# <a name="jpeg-ycbcr-support"></a><span data-ttu-id="0c505-103">JPEG YCbCr 支援</span><span class="sxs-lookup"><span data-stu-id="0c505-103">JPEG YCbCr Support</span></span>

<span data-ttu-id="0c505-104">從 Windows 8.1 開始， [Windows 影像處理元件 (WIC) ](-wic-about-windows-imaging-codec.md) JPEG 編解碼器可支援在其原生 YC<sub>b</sub>C<sub>r</sub> 表單中讀取和寫入影像資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-104">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <span data-ttu-id="0c505-105">WIC YC<sub>b</sub>C<sub>r</sub> 支援可以搭配 [Direct2D](../direct2d/direct2d-portal.md) 使用，以呈現具有影像效果的 YC<sub>b</sub>C<sub>r</sub> 圖元資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-105">WIC YC<sub>b</sub>C<sub>r</sub> support can be used in conjunction with [Direct2D](../direct2d/direct2d-portal.md) to render YC<sub>b</sub>C<sub>r</sub> pixel data with an image effect.</span></span> <span data-ttu-id="0c505-106">此外，WIC JPEG 編解碼器也可以透過媒體基礎使用特定相機驅動程式所產生的 YC<sub>b</sub>C<sub>r</sub> 圖元資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-106">In addition, the WIC JPEG codec can consume YC<sub>b</sub>C<sub>r</sub> pixel data produced by certain camera drivers via Media Foundation.</span></span>

<span data-ttu-id="0c505-107">YC<sub>b</sub>C<sub>r</sub> 圖元資料耗用的記憶體明顯小於標準 BGRA 像素格式。</span><span class="sxs-lookup"><span data-stu-id="0c505-107">YC<sub>b</sub>C<sub>r</sub> pixel data consumes significantly less memory than standard BGRA pixel formats.</span></span> <span data-ttu-id="0c505-108">此外，存取 YC<sub>b</sub>C<sub>r</sub> 資料可讓您將 JPEG 解碼/編碼管線的一些階段卸載至 Direct2D，也就是 GPU 加速。</span><span class="sxs-lookup"><span data-stu-id="0c505-108">In addition, accessing YC<sub>b</sub>C<sub>r</sub> data allows you to offload some stages of the JPEG decode/encode pipeline to Direct2D which is GPU accelerated.</span></span> <span data-ttu-id="0c505-109">藉由使用 YC<sub>b</sub>C<sub>r</sub>，您的應用程式可以減少相同大小和品質影像的 JPEG 記憶體耗用量和載入時間。</span><span class="sxs-lookup"><span data-stu-id="0c505-109">By using YC<sub>b</sub>C<sub>r</sub>, your app can reduce JPEG memory consumption and load times for the same size and quality images.</span></span> <span data-ttu-id="0c505-110">或者，您的應用程式可以使用更高解析度的 JPEG 影像，而不會受到效能的影響。</span><span class="sxs-lookup"><span data-stu-id="0c505-110">Or, your app can use more, higher resolution JPEG images without suffering from performance penalties.</span></span>

<span data-ttu-id="0c505-111">本主題說明 YC<sub>b</sub>C<sub>r</sub> 資料的運作方式，以及如何在 WIC 和 Direct2D 中使用它。</span><span class="sxs-lookup"><span data-stu-id="0c505-111">This topic describes how YC<sub>b</sub>C<sub>r</sub> data works and how to use it in WIC and Direct2D.</span></span>

-   [<span data-ttu-id="0c505-112">關於 JPEG YC<sub>b</sub>C<sub>r</sub> 資料</span><span class="sxs-lookup"><span data-stu-id="0c505-112">About JPEG YC<sub>b</sub>C<sub>r</sub> Data</span></span>](#about-jpeg-ycbcr-data)
    -   [<span data-ttu-id="0c505-113">YC<sub>b</sub>C<sub>r</sub> 色彩模型</span><span class="sxs-lookup"><span data-stu-id="0c505-113">YC<sub>b</sub>C<sub>r</sub> Color Model</span></span>](#ycbcr-color-model)
    -   [<span data-ttu-id="0c505-114">平面與交錯記憶體版面配置</span><span class="sxs-lookup"><span data-stu-id="0c505-114">Planar Versus Interleaved Memory Layouts</span></span>](#planar-versus-interleaved-memory-layouts)
    -   [<span data-ttu-id="0c505-115">色度次取樣</span><span class="sxs-lookup"><span data-stu-id="0c505-115">Chroma Subsampling</span></span>](#chroma-subsampling)
    -   [<span data-ttu-id="0c505-116">YC<sub>b</sub>C<sub>r</sub>的 JPEG 用法</span><span class="sxs-lookup"><span data-stu-id="0c505-116">JPEG Usage of YC<sub>b</sub>C<sub>r</sub></span></span>](#jpeg-usage-of-ycbcr)
-   [<span data-ttu-id="0c505-117">使用 JPEG YC<sub>b</sub>C<sub>r</sub> 資料</span><span class="sxs-lookup"><span data-stu-id="0c505-117">Using JPEG YC<sub>b</sub>C<sub>r</sub> Data</span></span>](#using-jpeg-ycbcr-data)
    -   [<span data-ttu-id="0c505-118">使用 YC<sub>b</sub>C<sub>r</sub> JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="0c505-118">Using YC<sub>b</sub>C<sub>r</sub> JPEG images</span></span>](#using-ycbcr-jpeg-images)
    -   [<span data-ttu-id="0c505-119">Windows 影像處理元件 Api</span><span class="sxs-lookup"><span data-stu-id="0c505-119">Windows Imaging Component APIs</span></span>](#windows-imaging-component-apis)
    -   [<span data-ttu-id="0c505-120">Direct2D Api</span><span class="sxs-lookup"><span data-stu-id="0c505-120">Direct2D APIs</span></span>](#direct2d-apis)
    -   [<span data-ttu-id="0c505-121">判斷是否支援 YC<sub>b</sub>C<sub>r</sub> 設定</span><span class="sxs-lookup"><span data-stu-id="0c505-121">Determining if the YC<sub>b</sub>C<sub>r</sub> Configuration is Supported</span></span>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [<span data-ttu-id="0c505-122">解碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-122">Decoding YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>](#decoding-ycbcr-pixel-data)
    -   [<span data-ttu-id="0c505-123">轉換 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-123">Transforming YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>](#transforming-ycbcr-pixel-data)
    -   [<span data-ttu-id="0c505-124">編碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-124">Encoding YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>](#encoding-ycbcr-pixel-data)
    -   [<span data-ttu-id="0c505-125">解碼 Windows 10 中的 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-125">Decoding YC<sub>b</sub>C<sub>r</sub> pixel data in Windows 10</span></span>](#decoding-ycbcr-pixel-data-in-windows-10)
-   [<span data-ttu-id="0c505-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c505-126">Related topics</span></span>](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a><span data-ttu-id="0c505-127">關於 JPEG YC<sub>b</sub>C<sub>r</sub> 資料</span><span class="sxs-lookup"><span data-stu-id="0c505-127">About JPEG YC<sub>b</sub>C<sub>r</sub> Data</span></span>

<span data-ttu-id="0c505-128">本節將說明一些重要概念，以瞭解 WIC 中的 YC<sub>b</sub>C<sub>r</sub> 支援如何運作及其主要優點。</span><span class="sxs-lookup"><span data-stu-id="0c505-128">This section explains some key concepts necessary to understand how YC<sub>b</sub>C<sub>r</sub> support in WIC works and its key benefits.</span></span>

### <a name="ycsubbsubcsubrsub-color-model"></a><span data-ttu-id="0c505-129">YC<sub>b</sub>C<sub>r</sub> 色彩模型</span><span class="sxs-lookup"><span data-stu-id="0c505-129">YC<sub>b</sub>C<sub>r</sub> Color Model</span></span>

<span data-ttu-id="0c505-130">Windows 8 和較早版本中的 WIC 支援四種不同的 [色彩模型](-wic-codec-native-pixel-formats.md)，最常見的是 RGB/BGR。</span><span class="sxs-lookup"><span data-stu-id="0c505-130">WIC in Windows 8 and earlier supports four different [color models](-wic-codec-native-pixel-formats.md), the most common of which is RGB/BGR.</span></span> <span data-ttu-id="0c505-131">此色彩模型使用紅色、綠色和藍色元件定義色彩資料;也可以使用第四個 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="0c505-131">This color model defines color data using red, green and blue components; a fourth alpha component may also be used.</span></span>

<span data-ttu-id="0c505-132">以下是分解成紅色、綠色和藍色元件的影像。</span><span class="sxs-lookup"><span data-stu-id="0c505-132">Here is an image decomposed into its red, green and blue components.</span></span>

![分解成紅色、綠色和藍色元件的影像。](graphics/ycbcr1.png)

<span data-ttu-id="0c505-134">YC<sub>b</sub>C<sub>r</sub> 是一種替代色彩模型，會使用亮度元件定義色彩資料 (Y) 和兩個色度元件 (c<sub>b</sub> 和 c<sub>r</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="0c505-134">YC<sub>b</sub>C<sub>r</sub> is an alternate color model that defines color data using a luminance component (Y) and two chrominance components (C<sub>b</sub> and C<sub>r</sub>).</span></span> <span data-ttu-id="0c505-135">它通常用於數位影像處理和影片案例中。</span><span class="sxs-lookup"><span data-stu-id="0c505-135">It is commonly used in digital imaging and video scenarios.</span></span> <span data-ttu-id="0c505-136">YC<sub>b</sub>C<sub>r</sub> 的詞彙通常會與 YUV 交替使用，雖然這兩個技術在技術上不同。</span><span class="sxs-lookup"><span data-stu-id="0c505-136">The term YC<sub>b</sub>C<sub>r</sub> is often used interchangeably with YUV, although the two are technically distinct.</span></span>

<span data-ttu-id="0c505-137">YC<sub>b</sub>C<sub>r</sub> 有幾種變化，不同之處在于色彩空間和動態範圍定義– WIC 特別支援 JPEG JFIF YC<sub>b</sub>C<sub>r</sub> 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-137">There are several variations of YC<sub>b</sub>C<sub>r</sub> which differ in color space and dynamic range definitions – WIC specifically supports JPEG JFIF YC<sub>b</sub>C<sub>r</sub> data.</span></span> <span data-ttu-id="0c505-138">如需詳細資訊，請參閱 [JPEG Itu-t T81 規格](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)。</span><span class="sxs-lookup"><span data-stu-id="0c505-138">For more information, refer to the [JPEG ITU-T81 specification](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).</span></span>

<span data-ttu-id="0c505-139">以下是在其 Y、C<sub>b</sub>和 c<sub>r</sub> 元件中分解的影像。</span><span class="sxs-lookup"><span data-stu-id="0c505-139">Here is an image decomposed into its Y, C<sub>b</sub>, and C<sub>r</sub> components.</span></span>

![分解為其 y、cb 和 cr 元件的影像。](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a><span data-ttu-id="0c505-141">平面與交錯記憶體版面配置</span><span class="sxs-lookup"><span data-stu-id="0c505-141">Planar Versus Interleaved Memory Layouts</span></span>

<span data-ttu-id="0c505-142">本節說明在記憶體中存取和儲存 RGB 圖元資料與 YC<sub>b</sub>C<sub>r</sub> 資料之間的一些差異。</span><span class="sxs-lookup"><span data-stu-id="0c505-142">This section describes some differences between accessing and storing RGB pixel data in memory versus YC<sub>b</sub>C<sub>r</sub> data.</span></span>

<span data-ttu-id="0c505-143">RGB 圖元資料通常是使用交錯記憶體配置儲存。</span><span class="sxs-lookup"><span data-stu-id="0c505-143">RGB pixel data is typically stored using an interleaved memory layout.</span></span> <span data-ttu-id="0c505-144">這表示單一色彩元件的資料會在圖元之間交錯，且每個圖元會連續儲存在記憶體中。</span><span class="sxs-lookup"><span data-stu-id="0c505-144">This means that data for a single color component is interleaved between pixels, and each pixel is stored contiguously in memory.</span></span>

<span data-ttu-id="0c505-145">以下圖顯示以交錯式記憶體配置儲存的 RGBA 圖元資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-145">Here is a figure showing RGBA pixel data stored in an interleaved memory layout.</span></span>

![此圖顯示以交錯式記憶體配置儲存的 rgba 圖元資料。](graphics/ycbcr3.png)

<span data-ttu-id="0c505-147">YC<sub>b</sub>C<sub>r</sub> 資料通常會使用平面記憶體配置儲存。</span><span class="sxs-lookup"><span data-stu-id="0c505-147">YC<sub>b</sub>C<sub>r</sub> data is typically stored using a planar memory layout.</span></span> <span data-ttu-id="0c505-148">這表示每個色彩元件會分別儲存在其本身的連續平面中，總共三個平面。</span><span class="sxs-lookup"><span data-stu-id="0c505-148">This means that each color component is stored separately in its own contiguous plane, for a total of three planes.</span></span> <span data-ttu-id="0c505-149">在另一個常見的設定中，C<sub>b</sub> 和 c<sub>r</sub> 元件會交錯並儲存在一起，而 Y 元件會保留在自己的平面中，總共兩個平面。</span><span class="sxs-lookup"><span data-stu-id="0c505-149">In another common configuration, the C<sub>b</sub> and C<sub>r</sub> components are interleaved and stored together, while the Y component remains in its own plane, for a total of two planes.</span></span>

<span data-ttu-id="0c505-150">以下顯示平面 Y 和交錯<sub>式 c</sub><sub>r</sub>圖元資料的圖表，這是常見的 YC<sub>b</sub>c<sub>r</sub>記憶體配置。</span><span class="sxs-lookup"><span data-stu-id="0c505-150">Here is a figure showing planar Y and interleaved C<sub>b</sub>C<sub>r</sub> pixel data, a common YC<sub>b</sub>C<sub>r</sub> memory layout.</span></span>

![顯示平面 y 和交錯 cbcr 圖元資料的圖表，這是常見的 ycbcr 記憶體配置。](graphics/ycbcr4.png)

<span data-ttu-id="0c505-152">在 WIC 和 Direct2D 中，會將每個色彩平面視為其本身的相異物件 ([IWICBitmapSource](-wic-imp-iwicbitmapsource.md) 或 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)) ，而且這些平面會形成 YC <sub>b</sub>C <sub>r</sub> 影像的支援資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-152">In both WIC and Direct2D, each color plane is treated as its own distinct object (either an [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) or [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)), and collectively these planes form the backing data for a YC<sub>b</sub>C<sub>r</sub> image.</span></span>

<span data-ttu-id="0c505-153">雖然 WIC 支援在2和3平面設定中存取 YC<sub>b</sub>C<sub>r</sub> 資料，但 Direct2D 只支援先前的 (Y 和 c<sub>b</sub>c<sub>r</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="0c505-153">While WIC supports accessing YC<sub>b</sub>C<sub>r</sub> data in both the 2 and 3 plane configurations, Direct2D only supports the former (Y and C<sub>b</sub>C<sub>r</sub>).</span></span> <span data-ttu-id="0c505-154">因此，當搭配使用 WIC 和 Direct2D 時，您應該一律使用2個平面 YC<sub>b</sub>C<sub>r</sub> 設定。</span><span class="sxs-lookup"><span data-stu-id="0c505-154">Therefore, when using WIC and Direct2D together you should always use the 2 plane YC<sub>b</sub>C<sub>r</sub> configuration.</span></span>

### <a name="chroma-subsampling"></a><span data-ttu-id="0c505-155">色度次取樣</span><span class="sxs-lookup"><span data-stu-id="0c505-155">Chroma Subsampling</span></span>

<span data-ttu-id="0c505-156">YC<sub>b</sub>C<sub>r</sub> 色彩模型非常適合數位影像案例，因為它可以利用人類視覺系統的特定層面。</span><span class="sxs-lookup"><span data-stu-id="0c505-156">The YC<sub>b</sub>C<sub>r</sub> color model is well suited for digital imaging scenarios because it can take advantage of certain aspects of the human visual system.</span></span> <span data-ttu-id="0c505-157">尤其是，人類對影像的亮度 (亮度) 的變化更敏感，且色度 (色彩) 較不敏感。</span><span class="sxs-lookup"><span data-stu-id="0c505-157">In particular, humans are more sensitive to changes in the luminance (brightness) of an image and less sensitive to chrominance (color).</span></span> <span data-ttu-id="0c505-158">藉由將色彩資料分割成不同的亮度和色度元件，我們可以選擇性地壓縮色度元件，以在品質降到最短的情況下節省空間。</span><span class="sxs-lookup"><span data-stu-id="0c505-158">By splitting the color data into separate luminance and chrominance components, we can selectively compress just the chrominance components to achieve space savings with a minimal loss in quality.</span></span>

<span data-ttu-id="0c505-159">執行這項操作的其中一種技術稱為「色度次取樣」。</span><span class="sxs-lookup"><span data-stu-id="0c505-159">One technique for doing this is called chroma subsampling.</span></span> <span data-ttu-id="0c505-160">C<sub>b</sub> 和 c<sub>r</sub> 平面是在一或兩個水準和垂直維度中 subsampled (downscaled) 。</span><span class="sxs-lookup"><span data-stu-id="0c505-160">The C<sub>b</sub> and C<sub>r</sub> planes are subsampled (downscaled) in one or both of the horizontal and vertical dimensions.</span></span> <span data-ttu-id="0c505-161">基於歷史原因，每個色度的取樣模式通常是使用三個部分 J:a： b 的比率。</span><span class="sxs-lookup"><span data-stu-id="0c505-161">For historical reasons, each chroma subsampling mode is commonly referred to using a three part J:a:b ratio.</span></span>



| <span data-ttu-id="0c505-162">次取樣模式</span><span class="sxs-lookup"><span data-stu-id="0c505-162">Subsampling mode</span></span> | <span data-ttu-id="0c505-163">水準縮小</span><span class="sxs-lookup"><span data-stu-id="0c505-163">Horizontal downscale</span></span> | <span data-ttu-id="0c505-164">垂直縮小</span><span class="sxs-lookup"><span data-stu-id="0c505-164">Vertical downscale</span></span> | <span data-ttu-id="0c505-165">每圖元的位數\*</span><span class="sxs-lookup"><span data-stu-id="0c505-165">Bits per pixel\*</span></span> |
|------------------|----------------------|--------------------|------------------|
| <span data-ttu-id="0c505-166">4:4:4</span><span class="sxs-lookup"><span data-stu-id="0c505-166">4:4:4</span></span>            | <span data-ttu-id="0c505-167">1 倍</span><span class="sxs-lookup"><span data-stu-id="0c505-167">1x</span></span>                   | <span data-ttu-id="0c505-168">1 倍</span><span class="sxs-lookup"><span data-stu-id="0c505-168">1x</span></span>                 | <span data-ttu-id="0c505-169">24</span><span class="sxs-lookup"><span data-stu-id="0c505-169">24</span></span>               |
| <span data-ttu-id="0c505-170">4:2:2</span><span class="sxs-lookup"><span data-stu-id="0c505-170">4:2:2</span></span>            | <span data-ttu-id="0c505-171">2x</span><span class="sxs-lookup"><span data-stu-id="0c505-171">2x</span></span>                   | <span data-ttu-id="0c505-172">1 倍</span><span class="sxs-lookup"><span data-stu-id="0c505-172">1x</span></span>                 | <span data-ttu-id="0c505-173">16</span><span class="sxs-lookup"><span data-stu-id="0c505-173">16</span></span>               |
| <span data-ttu-id="0c505-174">4:4:0</span><span class="sxs-lookup"><span data-stu-id="0c505-174">4:4:0</span></span>            | <span data-ttu-id="0c505-175">1 倍</span><span class="sxs-lookup"><span data-stu-id="0c505-175">1x</span></span>                   | <span data-ttu-id="0c505-176">2x</span><span class="sxs-lookup"><span data-stu-id="0c505-176">2x</span></span>                 | <span data-ttu-id="0c505-177">16</span><span class="sxs-lookup"><span data-stu-id="0c505-177">16</span></span>               |
| <span data-ttu-id="0c505-178">4:2:0</span><span class="sxs-lookup"><span data-stu-id="0c505-178">4:2:0</span></span>            | <span data-ttu-id="0c505-179">2x</span><span class="sxs-lookup"><span data-stu-id="0c505-179">2x</span></span>                   | <span data-ttu-id="0c505-180">2x</span><span class="sxs-lookup"><span data-stu-id="0c505-180">2x</span></span>                 | <span data-ttu-id="0c505-181">12</span><span class="sxs-lookup"><span data-stu-id="0c505-181">12</span></span>               |



 

<span data-ttu-id="0c505-182">\* 包含 Y 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-182">\* Includes Y data.</span></span>

<span data-ttu-id="0c505-183">從上表中，如果您使用 YC<sub>b</sub>C<sub>r</sub> 來儲存未壓縮的影像資料，您可以將記憶體節省25% 到62.5%，而每圖元 RGBA 資料可節省25% 到32位，視使用的色度次取樣模式而定。</span><span class="sxs-lookup"><span data-stu-id="0c505-183">From the above table, if you use YC<sub>b</sub>C<sub>r</sub> to store uncompressed image data you can achieve a memory savings of 25% to 62.5% versus 32 bit per pixel RGBA data, depending on which chroma subsampling mode is used.</span></span>

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a><span data-ttu-id="0c505-184">YC<sub>b</sub>C<sub>r</sub>的 JPEG 用法</span><span class="sxs-lookup"><span data-stu-id="0c505-184">JPEG Usage of YC<sub>b</sub>C<sub>r</sub></span></span>

<span data-ttu-id="0c505-185">概括而言，JPEG 解壓縮管線包含下列階段：</span><span class="sxs-lookup"><span data-stu-id="0c505-185">At a high level, the JPEG decompression pipeline consists of the following stages:</span></span>

1.  <span data-ttu-id="0c505-186">執行熵 (例如 Huffman) 解壓縮</span><span class="sxs-lookup"><span data-stu-id="0c505-186">Perform entropy (e.g. Huffman) decompression</span></span>
2.  <span data-ttu-id="0c505-187">執行 dequantization</span><span class="sxs-lookup"><span data-stu-id="0c505-187">Perform dequantization</span></span>
3.  <span data-ttu-id="0c505-188">執行反向離散余弦轉換</span><span class="sxs-lookup"><span data-stu-id="0c505-188">Perform inverse discrete cosine transform</span></span>
4.  <span data-ttu-id="0c505-189">在 C<sub>b</sub>c<sub>r</sub> 資料上執行色度 upsampling</span><span class="sxs-lookup"><span data-stu-id="0c505-189">Perform chroma upsampling on C<sub>b</sub>C<sub>r</sub> data</span></span>
5.  <span data-ttu-id="0c505-190">視需要將 YC<sub>b</sub>C<sub>r</sub> 資料轉換成 RGBA () </span><span class="sxs-lookup"><span data-stu-id="0c505-190">Convert YC<sub>b</sub>C<sub>r</sub> data to RGBA (if needed)</span></span>

<span data-ttu-id="0c505-191">藉由讓 JPEG 編解碼器產生 YC<sub>b</sub>C<sub>r</sub> 資料，我們可以避免解碼程式的最後兩個步驟，或將它們延遲到 GPU。</span><span class="sxs-lookup"><span data-stu-id="0c505-191">By having the JPEG codec produce YC<sub>b</sub>C<sub>r</sub> data, we can avoid the final two steps of the decode process, or defer them to the GPU.</span></span> <span data-ttu-id="0c505-192">除了上一節所列的記憶體節省之外，這可大幅減少將映射解碼所需的整體時間。</span><span class="sxs-lookup"><span data-stu-id="0c505-192">In addition to the memory savings listed in the previous section, this significantly reduces overall time needed to decode the image.</span></span> <span data-ttu-id="0c505-193">在編碼 YC<sub>b</sub>C<sub>r</sub> 資料時也適用相同的節省量。</span><span class="sxs-lookup"><span data-stu-id="0c505-193">The same savings apply when encoding YC<sub>b</sub>C<sub>r</sub> data.</span></span>

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a><span data-ttu-id="0c505-194">使用 JPEG YC<sub>b</sub>C<sub>r</sub> 資料</span><span class="sxs-lookup"><span data-stu-id="0c505-194">Using JPEG YC<sub>b</sub>C<sub>r</sub> Data</span></span>

<span data-ttu-id="0c505-195">本節說明如何使用 WIC 和 Direct2D 來操作 YC<sub>b</sub>C<sub>r</sub> 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-195">This section explains how to use WIC and Direct2D to operate on YC<sub>b</sub>C<sub>r</sub> data.</span></span>

<span data-ttu-id="0c505-196">若要查看實務中所使用之檔的指導方針，請參閱 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) ，其中示範在 Direct2D 應用程式中解碼和轉譯 YC<sub>b</sub>C<sub>r</sub> 內容所需的所有步驟。</span><span class="sxs-lookup"><span data-stu-id="0c505-196">To see the guidance from this document used in practice, see the [JPEG YCbCr optimizations in Direct2D and WIC sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) which demonstrates all of the steps needed to decode and render YC<sub>b</sub>C<sub>r</sub> content in a Direct2D app.</span></span>

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a><span data-ttu-id="0c505-197">使用 YC<sub>b</sub>C<sub>r</sub> JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="0c505-197">Using YC<sub>b</sub>C<sub>r</sub> JPEG images</span></span>

<span data-ttu-id="0c505-198">大部分的 JPEG 影像都會儲存為 YC<sub>b</sub>C<sub>r</sub>。</span><span class="sxs-lookup"><span data-stu-id="0c505-198">The vast majority of JPEG images are stored as YC<sub>b</sub>C<sub>r</sub>.</span></span> <span data-ttu-id="0c505-199">某些 Jpeg 包含 CMYK 或灰階資料，而且不會使用 YC<sub>b</sub>C<sub>r</sub>。</span><span class="sxs-lookup"><span data-stu-id="0c505-199">Some JPEGs contain CMYK or grayscale data and do not use YC<sub>b</sub>C<sub>r</sub>.</span></span> <span data-ttu-id="0c505-200">這表示您通常（但不一定）可以直接使用既有的 JPEG 內容，而不需要任何修改。</span><span class="sxs-lookup"><span data-stu-id="0c505-200">This means that you typically, but not always, can directly use pre-existing JPEG content without any modifications.</span></span>

<span data-ttu-id="0c505-201">WIC 和 Direct2D 不支援每個可能的 YC<sub>b</sub>C<sub>r</sub> 設定，而 Direct2D 中的 YC<sub>b</sub>c<sub>r</sub> 支援取決於基礎圖形硬體和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0c505-201">WIC and Direct2D do not support every possible YC<sub>b</sub>C<sub>r</sub> configuration, and YC<sub>b</sub>C<sub>r</sub> support in Direct2D is dependent upon the underlying graphics hardware and driver.</span></span> <span data-ttu-id="0c505-202">基於這個原因，一般用途的影像處理管線必須健全于未使用 YC<sub>b</sub>c<sub>r</sub> (包括其他常見的影像格式，例如 PNG 或 BMP) ，或無法使用 YC<sub>b</sub>C<sub>r</sub> 支援的情況。</span><span class="sxs-lookup"><span data-stu-id="0c505-202">Because of this, a general purpose imaging pipeline needs to be robust to images that do not use YC<sub>b</sub>C<sub>r</sub> (including other common image formats such as PNG or BMP) or to cases where YC<sub>b</sub>C<sub>r</sub> support is not available.</span></span> <span data-ttu-id="0c505-203">建議您保留現有的 BGRA 型映射管線，並啟用 YC<sub>b</sub>C<sub>r</sub> 作為效能優化（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0c505-203">We recommend that you keep your existing BGRA based imaging pipeline and enable YC<sub>b</sub>C<sub>r</sub> as a performance optimization when available.</span></span>

### <a name="windows-imaging-component-apis"></a><span data-ttu-id="0c505-204">Windows 影像處理元件 Api</span><span class="sxs-lookup"><span data-stu-id="0c505-204">Windows Imaging Component APIs</span></span>

<span data-ttu-id="0c505-205">Windows 8.1 中的 WIC 會新增三個新介面，以提供對 JPEG YC<sub>b</sub>C<sub>r</sub> 資料的存取。</span><span class="sxs-lookup"><span data-stu-id="0c505-205">WIC in Windows 8.1 adds three new interfaces to provide access to JPEG YC<sub>b</sub>C<sub>r</sub> data.</span></span>

### <a name="iwicplanarbitmapsourcetransform"></a><span data-ttu-id="0c505-206">IWICPlanarBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="0c505-206">IWICPlanarBitmapSourceTransform</span></span>

<span data-ttu-id="0c505-207">[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)，不同之處在于它會在平面設定中產生圖元，包括 YC <sub>b</sub>C <sub>r</sub> 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-207">[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) is analogous to [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), except that it produces pixels in a planar configuration, including YC<sub>b</sub>C<sub>r</sub> data.</span></span> <span data-ttu-id="0c505-208">您可以藉由在支援平面存取的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 執行上呼叫 QueryInterface 來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="0c505-208">You can obtain this interface by calling QueryInterface on an implementation of [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) that supports planar access.</span></span> <span data-ttu-id="0c505-209">這包括 JPEG 編解碼器對 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 以及 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)的實作為。</span><span class="sxs-lookup"><span data-stu-id="0c505-209">This includes the JPEG codec’s implementation of [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) as well as [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).</span></span>

### <a name="iwicplanarbitmapframeencode"></a><span data-ttu-id="0c505-210">IWICPlanarBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="0c505-210">IWICPlanarBitmapFrameEncode</span></span>

<span data-ttu-id="0c505-211">[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) 提供編碼平面圖元資料的功能，包括 YC <sub>b</sub>C <sub>r</sub> 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-211">[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) provides the ability to encode planar pixel data, including YC<sub>b</sub>C<sub>r</sub> data.</span></span> <span data-ttu-id="0c505-212">您可以藉由呼叫 [**IWICBITMAPFRAMEENCODE**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)JPEG 編解碼器的 QueryInterface 來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="0c505-212">You can obtain this interface by calling QueryInterface on the JPEG codec’s implementation of [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

### <a name="iwicplanarformatconverter"></a><span data-ttu-id="0c505-213">IWICPlanarFormatConverter</span><span class="sxs-lookup"><span data-stu-id="0c505-213">IWICPlanarFormatConverter</span></span>

<span data-ttu-id="0c505-214">[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) 可讓 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 取用平面圖元資料（包括 YC <sub>b</sub>C <sub>r</sub>），並將它轉換成交錯的像素格式。</span><span class="sxs-lookup"><span data-stu-id="0c505-214">[**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) allows [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) to consume planar pixel data, including YC<sub>b</sub>C<sub>r</sub>, and convert it to an interleaved pixel format.</span></span> <span data-ttu-id="0c505-215">它不會公開將交錯圖元資料轉換成平面格式的能力。</span><span class="sxs-lookup"><span data-stu-id="0c505-215">It does not expose the ability to convert interleaved pixel data to a planar format.</span></span> <span data-ttu-id="0c505-216">您可以在 Windows 提供的 **IWICFormatConverter** 執行上呼叫 QueryInterface 來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="0c505-216">You can obtain this interface by calling QueryInterface on the Windows provided implementation of **IWICFormatConverter**.</span></span>

### <a name="direct2d-apis"></a><span data-ttu-id="0c505-217">Direct2D Api</span><span class="sxs-lookup"><span data-stu-id="0c505-217">Direct2D APIs</span></span>

<span data-ttu-id="0c505-218">Windows 8.1 中的 Direct2D 支援 YC<sub>b</sub>c<sub>r</sub> 平面圖元資料（具有新的 YC<sub>b</sub>c<sub>r</sub> 影像效果）。</span><span class="sxs-lookup"><span data-stu-id="0c505-218">Direct2D in Windows 8.1 supports YC<sub>b</sub>C<sub>r</sub> planar pixel data with the new YC<sub>b</sub>C<sub>r</sub> image effect .</span></span> <span data-ttu-id="0c505-219">此效果提供轉譯 YC<sub>b</sub>C<sub>r</sub> 資料的能力。</span><span class="sxs-lookup"><span data-stu-id="0c505-219">This effect provides the ability to render YC<sub>b</sub>C<sub>r</sub> data.</span></span> <span data-ttu-id="0c505-220">效果會採用輸入兩個 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 介面：一個是以 dxgi 格式 R8 UNORM 格式來包含平面 Y 資料 \_ \_ \_ ，另一個則包含 dxgi \_ 格式 \_ R8G8 UNORM 格式的交錯 CbCr 資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0c505-220">The effect takes as input two [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) interfaces: one containing planar Y data in the DXGI\_FORMAT\_R8\_UNORM format, and one containing interleaved CbCr data in the DXGI\_FORMAT\_R8G8\_UNORM format.</span></span> <span data-ttu-id="0c505-221">您通常會使用此效果來取代可能包含 BGRA 圖元資料的 **ID2D1Bitmap** 。</span><span class="sxs-lookup"><span data-stu-id="0c505-221">You typically use this effect in place of the **ID2D1Bitmap** that would have contained BGRA pixel data.</span></span>

<span data-ttu-id="0c505-222">YC<sub>b</sub>c<sub>r</sub>影像效果的目的是要搭配可提供 YC<sub>b</sub>c<sub>r</sub>資料的 WIC YC<sub>b</sub>c<sub>r</sub> api 一起使用。</span><span class="sxs-lookup"><span data-stu-id="0c505-222">The YC<sub>b</sub>C<sub>r</sub> image effect is intended to be used in conjunction with the WIC YC<sub>b</sub>C<sub>r</sub> APIs which provide the YC<sub>b</sub>C<sub>r</sub> data.</span></span> <span data-ttu-id="0c505-223">這可有效地將部分解碼工作從 CPU 卸載至 GPU，以便更快速且平行處理。</span><span class="sxs-lookup"><span data-stu-id="0c505-223">This effectively acts to offload some of the decode work from the CPU to the GPU, where it can be processed much quicker and in parallel.</span></span>

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a><span data-ttu-id="0c505-224">判斷是否支援 YC<sub>b</sub>C<sub>r</sub> 設定</span><span class="sxs-lookup"><span data-stu-id="0c505-224">Determining if the YC<sub>b</sub>C<sub>r</sub> Configuration is Supported</span></span>

<span data-ttu-id="0c505-225">如先前所述，您的應用程式應該很健全，以 YC<sub>b</sub>C<sub>r</sub> 支援無法使用的情況。</span><span class="sxs-lookup"><span data-stu-id="0c505-225">As noted before, your app should be robust to cases where YC<sub>b</sub>C<sub>r</sub> support is not available.</span></span> <span data-ttu-id="0c505-226">本節討論您的應用程式應該檢查的條件。</span><span class="sxs-lookup"><span data-stu-id="0c505-226">This section discusses the conditions that your app should check for.</span></span> <span data-ttu-id="0c505-227">如果下列任何一項檢查失敗，您的應用程式應該會切換回標準的 BGRA 型管線。</span><span class="sxs-lookup"><span data-stu-id="0c505-227">If any of the following checks fail, your app should fall back to a standard BGRA-based pipeline.</span></span>

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a><span data-ttu-id="0c505-228">WIC 元件是否支援 YC<sub>b</sub>C<sub>r</sub> 資料存取？</span><span class="sxs-lookup"><span data-stu-id="0c505-228">Does the WIC component support YC<sub>b</sub>C<sub>r</sub> data access?</span></span>

<span data-ttu-id="0c505-229">只有 Windows 提供的 JPEG 編解碼器和某些 WIC 轉換支援 YC<sub>b</sub>C<sub>r</sub> 資料存取。</span><span class="sxs-lookup"><span data-stu-id="0c505-229">Only the Windows provided JPEG codec and certain WIC transforms support YC<sub>b</sub>C<sub>r</sub> data access.</span></span> <span data-ttu-id="0c505-230">如需完整清單，請參閱 [Windows 影像處理元件 api](#windows-imaging-component-apis) 一節。</span><span class="sxs-lookup"><span data-stu-id="0c505-230">For a complete list, refer to the [Windows Imaging Component APIs](#windows-imaging-component-apis) section.</span></span>

<span data-ttu-id="0c505-231">若要取得其中一個平面 YC<sub>b</sub>C<sub>r</sub> 介面，請呼叫原始介面上的 QueryInterface。</span><span class="sxs-lookup"><span data-stu-id="0c505-231">To obtain one of the planar YC<sub>b</sub>C<sub>r</sub> interfaces, call QueryInterface on the original interface.</span></span> <span data-ttu-id="0c505-232">如果元件不支援 YC<sub>b</sub>C<sub>r</sub> 資料存取，這將會失敗。</span><span class="sxs-lookup"><span data-stu-id="0c505-232">This will fail if the component does not support YC<sub>b</sub>C<sub>r</sub> data access.</span></span>

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a><span data-ttu-id="0c505-233">要求的 WIC 轉換是否支援 YC<sub>b</sub>C<sub>r</sub>？</span><span class="sxs-lookup"><span data-stu-id="0c505-233">Is the requested WIC transform supported for YC<sub>b</sub>C<sub>r</sub>?</span></span>

<span data-ttu-id="0c505-234">取得 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)之後，您應該先呼叫 [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform)。</span><span class="sxs-lookup"><span data-stu-id="0c505-234">After obtaining an [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform), you should first call [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform).</span></span> <span data-ttu-id="0c505-235">這個方法會將您想要套用至平面 YC<sub>b</sub>C<sub>r</sub> 資料的一組完整轉換做為輸入參數，並傳回指出支援的布林值，以及最接近可傳回之要求大小的維度。</span><span class="sxs-lookup"><span data-stu-id="0c505-235">This method takes as input parameters the complete set of transforms that you want to be applied to the planar YC<sub>b</sub>C<sub>r</sub> data, and returns a Boolean indicating support, as well as the closest dimensions to the requested size that can be returned.</span></span> <span data-ttu-id="0c505-236">使用 [**IWICPlanarBitmapSourceTransform：： CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)存取圖元資料之前，您應該先檢查這三個值。</span><span class="sxs-lookup"><span data-stu-id="0c505-236">You should check all three values before accessing the pixel data with [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).</span></span>

<span data-ttu-id="0c505-237">此模式類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="0c505-237">This pattern is similar to how [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is used.</span></span>

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a><span data-ttu-id="0c505-238">圖形驅動程式是否支援搭配 Direct2D 使用 YC<sub>b</sub>C<sub>r</sub> 所需的功能？</span><span class="sxs-lookup"><span data-stu-id="0c505-238">Does the graphics driver support the features necessary to use YC<sub>b</sub>C<sub>r</sub> with Direct2D?</span></span>

<span data-ttu-id="0c505-239">只有當您使用 Direct2D YC<sub>b</sub>c<sub>r</sub> 效果轉譯 YC<sub>b</sub>c<sub>r</sub> 內容時，才需要進行這項檢查。</span><span class="sxs-lookup"><span data-stu-id="0c505-239">This check is only necessary if you are using the Direct2D YC<sub>b</sub>C<sub>r</sub> effect to render YC<sub>b</sub>C<sub>r</sub> content.</span></span> <span data-ttu-id="0c505-240">Direct2D 會使用<sub></sub>dxgi<sub> </sub> \_ 格式 \_ R8 \_ UNORM 和 dxgi \_ 格式 \_ R8G8 \_ UNORM 像素格式（無法從所有圖形驅動程式使用）儲存 YC b C r 資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-240">Direct2D stores YC<sub>b</sub>C<sub>r</sub> data using the DXGI\_FORMAT\_R8\_UNORM and DXGI\_FORMAT\_R8G8\_UNORM pixel formats, which are not available from all graphics drivers.</span></span>

<span data-ttu-id="0c505-241">使用 YC <sub>b</sub>C <sub>r</sub> 映射效果之前，您應該呼叫 [**ID2D1DeviceCoNtext：： IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) ，以確定驅動程式支援兩種格式。</span><span class="sxs-lookup"><span data-stu-id="0c505-241">Before using the YC <sub>b</sub>C <sub>r</sub> image effect, you should call [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) to ensure that both formats are supported by the driver.</span></span>

### <a name="sample-code"></a><span data-ttu-id="0c505-242">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="0c505-242">Sample code</span></span>

<span data-ttu-id="0c505-243">以下是示範建議的檢查的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="0c505-243">Below is a code example demonstrating the recommended checks.</span></span> <span data-ttu-id="0c505-244">此範例取自 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)。</span><span class="sxs-lookup"><span data-stu-id="0c505-244">This example was taken from the [JPEG YCbCr optimizations in Direct2D and WIC sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).</span></span>


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a><span data-ttu-id="0c505-245">解碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-245">Decoding YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>

<span data-ttu-id="0c505-246">如果您想要取得 YC <sub>b</sub>C <sub>r</sub> 圖元資料，您應該呼叫 [**IWICPlanarBitmapSourceTransform：： CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels)。</span><span class="sxs-lookup"><span data-stu-id="0c505-246">If you want to obtain YC <sub>b</sub>C <sub>r</sub> pixel data you should call [**IWICPlanarBitmapSourceTransform::CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels).</span></span> <span data-ttu-id="0c505-247">這個方法會將圖元資料複製到已填滿 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) 結構的陣列中，您想要 (例如 Y 和 c <sub>b</sub>c <sub>r</sub>) 的每個資料平面都有一個。</span><span class="sxs-lookup"><span data-stu-id="0c505-247">This method copies pixel data into an array of filled-out [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) structures, one for each plane of data you want (for example, Y and C<sub>b</sub>C<sub>r</sub>).</span></span> <span data-ttu-id="0c505-248">**WICBitmapPlane** 包含圖元資料的相關資訊，並指向將接收資料的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0c505-248">A **WICBitmapPlane** contains info about the pixel data and points to the memory buffer that will receive the data.</span></span>

<span data-ttu-id="0c505-249">如果您想要使用 YC <sub>b</sub>C <sub>r</sub>圖元資料搭配其他 WIC api，您應該建立適當設定的 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)、呼叫 [**鎖定**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock)以取得基礎記憶體緩衝區，並將緩衝區與用來接收 YC <sub>b</sub>C <sub>r</sub>圖元資料的 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane)產生關聯。</span><span class="sxs-lookup"><span data-stu-id="0c505-249">If you want to use the YC <sub>b</sub>C <sub>r</sub> pixel data with other WIC APIs you should create an appropriately configured [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), call [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) to obtain the underlying memory buffer, and associate the buffer with the [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) used to receive the YC<sub>b</sub>C<sub>r</sub> pixel data.</span></span> <span data-ttu-id="0c505-250">然後，您就可以正常使用 [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) 。</span><span class="sxs-lookup"><span data-stu-id="0c505-250">You can then use the [IWICBitmap](-wic-imp-iwicbitmapdecoder.md) normally.</span></span>

<span data-ttu-id="0c505-251">最後，如果您想要在 Direct2D 中轉譯 YC <sub>b</sub>c <sub>r</sub>資料，您應該從每個 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)建立 [**ID2D1BITMAP**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ，並使用它們做為 YC <sub>b</sub>C <sub>r</sub>影像效果的來源。</span><span class="sxs-lookup"><span data-stu-id="0c505-251">Finally, if you want to render the YC <sub>b</sub>C <sub>r</sub> data in Direct2D, you should create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) from each [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and use them as source for the YC<sub>b</sub>C<sub>r</sub> image effect.</span></span> <span data-ttu-id="0c505-252">WIC 可讓您要求多個平面設定。</span><span class="sxs-lookup"><span data-stu-id="0c505-252">WIC allows you to request multiple planar configurations.</span></span> <span data-ttu-id="0c505-253">與 Direct2D 交互操作時，您應該要求兩個平面，一個使用 GUID WICPixelFormat8bppY，另一個使用 \_ guid \_ WICPixelFormat16bppCbCr，因為這是 Direct2D 所預期的設定。</span><span class="sxs-lookup"><span data-stu-id="0c505-253">When interoperating with Direct2D you should request two planes, one using GUID\_WICPixelFormat8bppY and the other using GUID\_WICPixelFormat16bppCbCr, as this is the configuration expected by Direct2D.</span></span>

### <a name="code-sample"></a><span data-ttu-id="0c505-254">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0c505-254">Code Sample</span></span>

<span data-ttu-id="0c505-255">以下程式碼範例示範在 Direct2D 中解碼和轉譯 YC<sub>b</sub>C<sub>r</sub> 資料的步驟。</span><span class="sxs-lookup"><span data-stu-id="0c505-255">Below is a code example demonstrating the steps to decode and render YC<sub>b</sub>C<sub>r</sub> data in Direct2D.</span></span> <span data-ttu-id="0c505-256">此範例取自 [Direct2D 和 WIC 範例中的 JPEG YCbCr 優化](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)。</span><span class="sxs-lookup"><span data-stu-id="0c505-256">This example was taken from the [JPEG YCbCr optimizations in Direct2D and WIC sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).</span></span>


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a><span data-ttu-id="0c505-257">轉換 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-257">Transforming YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>

<span data-ttu-id="0c505-258">轉換 YC <sub>b</sub>C <sub>r</sub> 資料與解碼幾乎完全相同，因為兩者都牽涉到 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)。</span><span class="sxs-lookup"><span data-stu-id="0c505-258">Transforming YC <sub>b</sub>C <sub>r</sub> data is nearly identical to decoding, as both involve [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform).</span></span> <span data-ttu-id="0c505-259">唯一的差別是您取得介面的 WIC 物件。</span><span class="sxs-lookup"><span data-stu-id="0c505-259">The only difference is which WIC object you obtained the interface from.</span></span> <span data-ttu-id="0c505-260">Windows 提供的 scaler、翻轉旋轉旋轉和色彩轉換全都支援 YC<sub>b</sub>C<sub>r</sub> 存取。</span><span class="sxs-lookup"><span data-stu-id="0c505-260">The Windows provided scaler, flip rotator and color transform all support YC<sub>b</sub>C<sub>r</sub> access.</span></span>

### <a name="chaining-transforms-together"></a><span data-ttu-id="0c505-261">將轉換連結在一起</span><span class="sxs-lookup"><span data-stu-id="0c505-261">Chaining Transforms Together</span></span>

<span data-ttu-id="0c505-262">WIC 支援將多個轉換連結在一起的概念。</span><span class="sxs-lookup"><span data-stu-id="0c505-262">WIC supports the notion of chaining together multiple transforms.</span></span> <span data-ttu-id="0c505-263">例如，您可以建立下列 WIC 管線：</span><span class="sxs-lookup"><span data-stu-id="0c505-263">For example, you can create the following WIC pipeline:</span></span>

![從 jpeg 解碼器開始的 wic 管線圖表。](graphics/ycbcr5.png)

<span data-ttu-id="0c505-265">然後，您可以在 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) 上呼叫 QueryInterface 來取得 [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)。</span><span class="sxs-lookup"><span data-stu-id="0c505-265">You can then call QueryInterface on the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) to obtain [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform).</span></span> <span data-ttu-id="0c505-266">色彩轉換可以與上述轉換進行通訊，而且可以公開管線中每個階段的匯總功能。</span><span class="sxs-lookup"><span data-stu-id="0c505-266">The color transform can communicate with the preceding transforms and can expose the aggregate capabilities of every stage in the pipeline.</span></span> <span data-ttu-id="0c505-267">WIC 可確保 YC<sub>b</sub>C<sub>r</sub> 資料會透過整個進程保留。</span><span class="sxs-lookup"><span data-stu-id="0c505-267">WIC ensures that the YC<sub>b</sub>C<sub>r</sub> data is preserved through the entire process.</span></span> <span data-ttu-id="0c505-268">此連結僅適用于使用支援 YC<sub>b</sub>C<sub>r</sub> 存取的元件時。</span><span class="sxs-lookup"><span data-stu-id="0c505-268">This chaining only works when using components that support YC<sub>b</sub>C<sub>r</sub> access.</span></span>

### <a name="jpeg-codec-optimizations"></a><span data-ttu-id="0c505-269">JPEG 編解碼器優化</span><span class="sxs-lookup"><span data-stu-id="0c505-269">JPEG Codec Optimizations</span></span>

<span data-ttu-id="0c505-270">類似于 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)的 jpeg 框架解碼執行， [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) 的 jpeg 框架解碼會支援原生 JPEG DCT 網域調整和旋轉。</span><span class="sxs-lookup"><span data-stu-id="0c505-270">Similar to the JPEG frame decode implementation of [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), the JPEG frame decode implementation of [**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) supports native JPEG DCT domain scaling and rotation.</span></span> <span data-ttu-id="0c505-271">您可以直接從 JPEG 解碼器要求兩個縮小的電源或旋轉。</span><span class="sxs-lookup"><span data-stu-id="0c505-271">You can request a power of two downscale or a rotation directly from the JPEG decoder.</span></span> <span data-ttu-id="0c505-272">這通常會比使用離散轉換產生更高的品質和效能。</span><span class="sxs-lookup"><span data-stu-id="0c505-272">This typically results in higher quality and performance than using the discrete transforms.</span></span>

<span data-ttu-id="0c505-273">此外，當您將一或多個 WIC 轉換轉換成 JPEG 解碼器之後，它可以利用原生 JPEG 調整和旋轉來滿足匯總要求的作業。</span><span class="sxs-lookup"><span data-stu-id="0c505-273">In addition, when you chain one or more WIC transforms after the JPEG decoder, it can leverage native JPEG scaling and rotation to satisfy the aggregate requested operation.</span></span>

### <a name="format-conversions"></a><span data-ttu-id="0c505-274">格式轉換</span><span class="sxs-lookup"><span data-stu-id="0c505-274">Format Conversions</span></span>

<span data-ttu-id="0c505-275">使用 [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) 將平面 YC <sub>b</sub>C <sub>r</sub> 圖元資料轉換成交錯的像素格式，例如 GUID \_ WICPixelFormat32bppPBGRA。</span><span class="sxs-lookup"><span data-stu-id="0c505-275">Use [**IWICPlanarFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) to convert planar YC<sub>b</sub>C<sub>r</sub> pixel data to an interleaved pixel format such as GUID\_WICPixelFormat32bppPBGRA.</span></span> <span data-ttu-id="0c505-276">Windows 8.1 中的 WIC 不提供轉換成平面 YC<sub>b</sub>C<sub>r</sub> 像素格式的能力。</span><span class="sxs-lookup"><span data-stu-id="0c505-276">WIC in Windows 8.1 does not provide the ability to convert to a planar YC<sub>b</sub>C<sub>r</sub> pixel format.</span></span>

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a><span data-ttu-id="0c505-277">編碼 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-277">Encoding YC<sub>b</sub>C<sub>r</sub> Pixel Data</span></span>

<span data-ttu-id="0c505-278">使用 [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) 將 YC <sub>b</sub>C <sub>r</sub> 圖元資料編碼成 JPEG 編碼器。</span><span class="sxs-lookup"><span data-stu-id="0c505-278">Use [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) to encode YC<sub>b</sub>C<sub>r</sub> pixel data to the JPEG encoder.</span></span> <span data-ttu-id="0c505-279">編碼 YC <sub>b</sub>C <sub>r</sub> 資料 **IWICPlanarBitmapFrameEncode** 類似，但不同于使用 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)編碼交錯資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-279">Encoding YC <sub>b</sub>C <sub>r</sub> data **IWICPlanarBitmapFrameEncode** is similar but not identical to encoding interleaved data using [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="0c505-280">平面介面只會公開撰寫平面框架影像資料的功能，您應該繼續使用畫面格編碼介面來設定中繼資料或縮圖，並在作業結束時認可。</span><span class="sxs-lookup"><span data-stu-id="0c505-280">The planar interface only exposes the ability to write planar frame image data, and you should continue to use the frame encode interface to set metadata or a thumbnail and to commit at the end of the operation.</span></span>

<span data-ttu-id="0c505-281">在一般情況下，您應該遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0c505-281">For the typical case, you should follow these steps:</span></span>

1.  <span data-ttu-id="0c505-282">正常取得 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 。</span><span class="sxs-lookup"><span data-stu-id="0c505-282">Obtain the [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) as normal.</span></span> <span data-ttu-id="0c505-283">如果您想要設定色度次取樣，請在建立框架時設定 [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) 編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="0c505-283">If you want to configure chroma subsampling, set the [**JpegYCrCbSubsampling**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) encoder option when creating the frame.</span></span>
2.  <span data-ttu-id="0c505-284">如果您需要設定中繼資料或縮圖，請使用 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 正常進行。</span><span class="sxs-lookup"><span data-stu-id="0c505-284">If you need to set metadata or a thumbnail, do this using [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) as normal.</span></span>
3.  <span data-ttu-id="0c505-285">[**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)的 QueryInterface。</span><span class="sxs-lookup"><span data-stu-id="0c505-285">QueryInterface for the [**IWICPlanarBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).</span></span>
4.  <span data-ttu-id="0c505-286">使用 [**IWICPlanarBitmapFrameEncode：： WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource)或 [**IWICPlanarBitmapFrameEncode：： WRITEPIXELS**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels)來設定 YC <sub>b</sub>C <sub>r</sub>圖元資料。</span><span class="sxs-lookup"><span data-stu-id="0c505-286">Set the YC <sub>b</sub>C <sub>r</sub> pixel data using [**IWICPlanarBitmapFrameEncode::WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) or [**IWICPlanarBitmapFrameEncode::WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels).</span></span> <span data-ttu-id="0c505-287">與其 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 對應專案不同，您會以 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 或 [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) 陣列提供這些方法，其中包含 YC <sub>b</sub>C <sub>r</sub> 圖元平面。</span><span class="sxs-lookup"><span data-stu-id="0c505-287">Unlike with their [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) counterparts, you provide these methods with an array of [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) or [**WICBitmapPlane**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) which contain the YC<sub>b</sub>C<sub>r</sub> pixel planes.</span></span>
5.  <span data-ttu-id="0c505-288">當您完成時，請呼叫 [**IWICBitmapFrameEncode：： Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)。</span><span class="sxs-lookup"><span data-stu-id="0c505-288">When you are finished, call [**IWICBitmapFrameEncode::Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span>

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a><span data-ttu-id="0c505-289">解碼 Windows 10 中的 YC<sub>b</sub>C<sub>r</sub> 圖元資料</span><span class="sxs-lookup"><span data-stu-id="0c505-289">Decoding YC<sub>b</sub>C<sub>r</sub> pixel data in Windows 10</span></span>

<span data-ttu-id="0c505-290">從 Windows 10 組建1507開始，Direct2D 提供 [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)，這是一個比較簡單的方式，可將 jpeg 解碼成 Direct2D，同時利用 YC <sub>b</sub>C <sub>r</sub> 優化。</span><span class="sxs-lookup"><span data-stu-id="0c505-290">Starting in Windows 10 build 1507, Direct2D provides [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), a simpler way to decode JPEGs into Direct2D while leveraging YC<sub>b</sub>C<sub>r</sub> optimizations.</span></span> <span data-ttu-id="0c505-291">**ID2D1ImageSourceFromWic** 會自動為您執行所有必要的 YC <sub>b</sub>C <sub>r</sub> 功能檢查;如果可能的話，它會使用優化的代碼路徑，否則會使用 fallback。</span><span class="sxs-lookup"><span data-stu-id="0c505-291">**ID2D1ImageSourceFromWic** automatically performs all of the necessary YC<sub>b</sub>C<sub>r</sub> capability checks for you; it uses the optimized codepath when possible, and uses a fallback otherwise.</span></span> <span data-ttu-id="0c505-292">它也會啟用新的優化，例如僅快取所需的映射子領域加寬。</span><span class="sxs-lookup"><span data-stu-id="0c505-292">It also enables new optimizations such as only caching subregions of the image that are needed at a time.</span></span>

<span data-ttu-id="0c505-293">如需有關使用 [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)的詳細資訊，請參閱 Direct2D 相片調整 SDK [範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)。</span><span class="sxs-lookup"><span data-stu-id="0c505-293">For more information about using [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), refer to the Direct2D Photo Adjustment SDK [sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c505-294">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c505-294">Related topics</span></span>

* [<span data-ttu-id="0c505-295">Direct2D 和 WIC 範例中的 JPEG YCbCr 優化</span><span class="sxs-lookup"><span data-stu-id="0c505-295">JPEG YCbCr optimizations in Direct2D and WIC sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
