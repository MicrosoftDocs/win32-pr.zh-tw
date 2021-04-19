---
description: 原生 JPEG XR 編解碼器可透過 Windows 影像處理元件 (WIC) 取得。 編解碼器支援的 JPEG XR 格式，是專為消費者和專業數位攝影所設計。
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: JPEG XR 編解碼器總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985295"
---
# <a name="jpeg-xr-codec-overview"></a><span data-ttu-id="61486-104">JPEG XR 編解碼器總覽</span><span class="sxs-lookup"><span data-stu-id="61486-104">JPEG XR Codec Overview</span></span>

<span data-ttu-id="61486-105">原生 JPEG XR 編解碼器可透過 Windows 影像處理元件 (WIC) 取得。</span><span class="sxs-lookup"><span data-stu-id="61486-105">The native JPEG XR codec is available through the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="61486-106">編解碼器支援的 JPEG XR 格式，是專為消費者和專業數位攝影所設計。</span><span class="sxs-lookup"><span data-stu-id="61486-106">The JPEG XR format, which the codec supports, is designed for consumer and professional digital photography.</span></span>

<span data-ttu-id="61486-107">JPEG XR 格式最多可達到原始 JPEG 格式的壓縮效率兩倍，並減少較不明顯的壓縮成品。</span><span class="sxs-lookup"><span data-stu-id="61486-107">The JPEG XR format can achieve up to twice the compression efficiency of the original JPEG format, with less noticeable compression artifacts.</span></span> <span data-ttu-id="61486-108">JPEG XR 的功能包括：</span><span class="sxs-lookup"><span data-stu-id="61486-108">Features of JPEG XR include:</span></span>

-   <span data-ttu-id="61486-109">支援單色、RGB、CMYK 和 n 聲道影像</span><span class="sxs-lookup"><span data-stu-id="61486-109">Support for monochrome, RGB, CMYK, and n-channel images</span></span>
-   <span data-ttu-id="61486-110">8-、16和32位的整數格式</span><span class="sxs-lookup"><span data-stu-id="61486-110">8-, 16-, and 32-bit integer formats</span></span>
-   <span data-ttu-id="61486-111">使用固定點或浮點色彩值的高動態範圍、寬範圍格式</span><span class="sxs-lookup"><span data-stu-id="61486-111">High dynamic range, wide-gamut formats, using fixed point or floating point color values</span></span>
-   <span data-ttu-id="61486-112">漸進式解碼</span><span class="sxs-lookup"><span data-stu-id="61486-112">Progressive decoding</span></span>
-   <span data-ttu-id="61486-113">使用相同壓縮演算法的失真或無損編碼</span><span class="sxs-lookup"><span data-stu-id="61486-113">Lossy or lossless encoding using the same compression algorithm</span></span>
-   <span data-ttu-id="61486-114">支援在大型影像中解碼感興趣的區域</span><span class="sxs-lookup"><span data-stu-id="61486-114">Support for decoding of regions of interest in large images</span></span>

<span data-ttu-id="61486-115">JPEG XR 格式是在下列標準檔中定義：</span><span class="sxs-lookup"><span data-stu-id="61486-115">The JPEG XR format is defined in the following standards documents:</span></span>

-   <span data-ttu-id="61486-116">ITU-T T. 832： *資訊技術– JPEG XR 影像編碼系統–影像編碼規格*</span><span class="sxs-lookup"><span data-stu-id="61486-116">ITU-T T.832: *Information technology – JPEG XR image coding system – Image coding specification*</span></span>
-   <span data-ttu-id="61486-117">ISO/IEC 29199-2:2010： *資訊技術— JPEG XR 影像編碼系統-第2部分：影像編碼規格*</span><span class="sxs-lookup"><span data-stu-id="61486-117">ISO/IEC 29199-2:2010: *Information technology — JPEG XR image coding system — Part 2: Image coding specification*</span></span>

<span data-ttu-id="61486-118">JPEG XR 標準主要是以 [HD 相片](hdphoto-format-overview.md) 格式為基礎，但是這兩種格式之間有一些差異。</span><span class="sxs-lookup"><span data-stu-id="61486-118">The JPEG XR standard is largely based on the [HD Photo](hdphoto-format-overview.md) format, but there are some differences between the two formats.</span></span> <span data-ttu-id="61486-119">在 Windows 8 中，已更新 HD 相片編解碼器以支援 JPEG XR。</span><span class="sxs-lookup"><span data-stu-id="61486-119">In Windows 8, the HD Photo codec has been updated to support JPEG XR.</span></span> <span data-ttu-id="61486-120">編碼器現在一律會輸出符合 JPEG XR 規範的位串流。</span><span class="sxs-lookup"><span data-stu-id="61486-120">The encoder now always outputs a JPEG XR–compliant bit stream.</span></span> <span data-ttu-id="61486-121">此解碼器可以解碼 JPEG XR 和 HD 相片影像。</span><span class="sxs-lookup"><span data-stu-id="61486-121">The decoder can decode both JPEG XR and HD Photo images.</span></span>

<span data-ttu-id="61486-122">我們已對 JPEG XR 編解碼器進行大幅的效能改進，相對於 HD 相片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="61486-122">Substantial performance improvements, in relation to the HD Photo codec, have been made to the JPEG XR codec.</span></span> <span data-ttu-id="61486-123">例如，子解析影像解碼（例如縮圖產生）已改善，以及低解析度影像解碼。</span><span class="sxs-lookup"><span data-stu-id="61486-123">For example, sub-resolution image decoding, such as thumbnail generation, has been improved, as well as low-resolution image decoding.</span></span> <span data-ttu-id="61486-124">建議您使用 JPEG XR 格式，而不是使用 HD 相片格式。</span><span class="sxs-lookup"><span data-stu-id="61486-124">It is recommended that you use the JPEG XR format instead of the HD Photo format.</span></span>

## <a name="codec-information"></a><span data-ttu-id="61486-125">編解碼器資訊</span><span class="sxs-lookup"><span data-stu-id="61486-125">Codec Information</span></span>



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61486-126">副檔名</span><span class="sxs-lookup"><span data-stu-id="61486-126">File name extension</span></span> | <span data-ttu-id="61486-127">"jxr" 和 "wdp"</span><span class="sxs-lookup"><span data-stu-id="61486-127">"jxr" and "wdp"</span></span>                                                         |
| <span data-ttu-id="61486-128">容器 GUID</span><span class="sxs-lookup"><span data-stu-id="61486-128">Container GUID</span></span>      | <span data-ttu-id="61486-129">**GUID \_ ContainerFormatWmp**</span><span class="sxs-lookup"><span data-stu-id="61486-129">**GUID\_ContainerFormatWmp**</span></span>                                            |
| <span data-ttu-id="61486-130">解碼器 GUID</span><span class="sxs-lookup"><span data-stu-id="61486-130">Decoder GUID</span></span>        | <span data-ttu-id="61486-131">**CLSID \_ WICWmpDecoder**</span><span class="sxs-lookup"><span data-stu-id="61486-131">**CLSID\_WICWmpDecoder**</span></span>                                                |
| <span data-ttu-id="61486-132">編碼器 GUID</span><span class="sxs-lookup"><span data-stu-id="61486-132">Encoder GUID</span></span>        | <span data-ttu-id="61486-133">**CLSID \_ WICWmpEncoder**</span><span class="sxs-lookup"><span data-stu-id="61486-133">**CLSID\_WICWmpEncoder**</span></span>                                                |
| <span data-ttu-id="61486-134">設定檔支援</span><span class="sxs-lookup"><span data-stu-id="61486-134">Profile Support</span></span>     | <span data-ttu-id="61486-135">編碼器和解碼最多可支援主要設定檔，最高可達層級128。</span><span class="sxs-lookup"><span data-stu-id="61486-135">The encoder and decoder support up to Main Profile and up to level 128.</span></span> |



 

## <a name="codec-features"></a><span data-ttu-id="61486-136">編解碼器功能</span><span class="sxs-lookup"><span data-stu-id="61486-136">Codec Features</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="61486-137">高動態範圍</span><span class="sxs-lookup"><span data-stu-id="61486-137">High Dynamic Range</span></span>

<span data-ttu-id="61486-138">JPEG XR 支援使用浮點或固定點色彩的高動態範圍影像。</span><span class="sxs-lookup"><span data-stu-id="61486-138">JPEG XR supports high-dynamic range images, using floating-point or fixed-point colors.</span></span> <span data-ttu-id="61486-139">在這些色彩格式中，圖元的數值範圍大於可見範圍，因此您可以在中繼處理階段中調整可見範圍的上方或下方的色彩。</span><span class="sxs-lookup"><span data-stu-id="61486-139">In these color formats, the numerical range of a pixel is larger than the visible range, so you can adjust colors above or below the visible range during intermediate processing stages.</span></span>

-   <span data-ttu-id="61486-140">固定點：在固定點標記法中，0代表黑色，而1.0 表示最大飽和度。</span><span class="sxs-lookup"><span data-stu-id="61486-140">Fixed-point: In a fixed-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="61486-141">JPEG XR 編解碼器支援16位和32位的固定點格式。</span><span class="sxs-lookup"><span data-stu-id="61486-141">The JPEG XR codec supports both 16-bit and 32-bit fixed-point formats.</span></span> <span data-ttu-id="61486-142">若為16位，1.0 = 0x2000h，可為可見範圍 \[ 0 ... 1 提供 13 \] 位。</span><span class="sxs-lookup"><span data-stu-id="61486-142">For 16-bit, 1.0 = 0x2000h, which gives 13 bits for the visible range \[0...1\].</span></span> <span data-ttu-id="61486-143">總範圍是–4.0 到 + 3.999，並以線性方式對應。</span><span class="sxs-lookup"><span data-stu-id="61486-143">The total range is –4.0 to +3.999, and is mapped linearly.</span></span> <span data-ttu-id="61486-144">若為32位、1.0 = 0x01000000h，可見範圍為24位，而總範圍為–128到 + 127.999。</span><span class="sxs-lookup"><span data-stu-id="61486-144">For 32-bit, 1.0 = 0x01000000h, the visible range is 24 bits, and the total range is –128 to +127.999.</span></span>
-   <span data-ttu-id="61486-145">浮點數：在浮點表示中，0代表黑色，而1.0 代表最大飽和度。</span><span class="sxs-lookup"><span data-stu-id="61486-145">Floating-point: In a floating-point representation, 0 represents black and 1.0 represents maximum saturation.</span></span> <span data-ttu-id="61486-146">JPEG XR 編解碼器支援16位和32位的浮點數格式。</span><span class="sxs-lookup"><span data-stu-id="61486-146">The JPEG XR codec supports both 16-bit and 32-bit floating-point formats.</span></span>

### <a name="tiles"></a><span data-ttu-id="61486-147">磚</span><span class="sxs-lookup"><span data-stu-id="61486-147">Tiles</span></span>

<span data-ttu-id="61486-148">框架可以分割成矩形子領域加寬，稱為 *磚*。</span><span class="sxs-lookup"><span data-stu-id="61486-148">A frame can be partitioned into rectangular subregions called *tiles*.</span></span> <span data-ttu-id="61486-149">磚是包含巨大區塊矩形陣列的影像區域。</span><span class="sxs-lookup"><span data-stu-id="61486-149">A tile is an area of a image that contains rectangular arrays of macroblocks.</span></span> <span data-ttu-id="61486-150">磚可讓影像的區域進行解碼，而不需要處理整個影像。</span><span class="sxs-lookup"><span data-stu-id="61486-150">Tiles enable regions of the image to be decoded without processing the entire image.</span></span>

<span data-ttu-id="61486-151">在編碼期間，藉由設定 **HorizontalTileSlices** 和 **VerticalTileSlices** 屬性來選取圖格數目。</span><span class="sxs-lookup"><span data-stu-id="61486-151">During encoding, select the number of tiles by setting the **HorizontalTileSlices** and **VerticalTileSlices** properties.</span></span> <span data-ttu-id="61486-152">磚大小下限為16×16圖元。</span><span class="sxs-lookup"><span data-stu-id="61486-152">The minimum tile size is 16 × 16 pixels.</span></span> <span data-ttu-id="61486-153">編碼器會調整磚數目以維持這項限制。</span><span class="sxs-lookup"><span data-stu-id="61486-153">The encoder adjusts the number of tiles to maintain this restriction.</span></span> <span data-ttu-id="61486-154">每個磚都有相關聯的儲存和處理額外負荷，因此您應該考慮特定案例所需的磚數目。</span><span class="sxs-lookup"><span data-stu-id="61486-154">There is storage and processing overhead associated with each tile, so you should consider the number of tiles that are needed for particular scenarios.</span></span>

### <a name="image-stream-output"></a><span data-ttu-id="61486-155">影像資料流程輸出</span><span class="sxs-lookup"><span data-stu-id="61486-155">Image Stream Output</span></span>

<span data-ttu-id="61486-156">JPEG XR 標準定義了 JPEG XR 檔案的兩個部分：</span><span class="sxs-lookup"><span data-stu-id="61486-156">The JPEG-XR standard defines two parts of a JPEG-XR file:</span></span>

-   <span data-ttu-id="61486-157">影像位資料流程，定義于標準的主體中。</span><span class="sxs-lookup"><span data-stu-id="61486-157">The image bit stream, defined in the body of the standard.</span></span>
-   <span data-ttu-id="61486-158">映射容器。</span><span class="sxs-lookup"><span data-stu-id="61486-158">The image container.</span></span> <span data-ttu-id="61486-159">檔案包含了 Exif 和 XMP 中繼資料，並定義于標準的附錄 A 中。</span><span class="sxs-lookup"><span data-stu-id="61486-159">The file contains Exif and XMP metadata, and is defined in Annex A of the standard.</span></span>

<span data-ttu-id="61486-160">標準可將影像串流內嵌在另一種類型的檔案容器內，因此可能會被允許。</span><span class="sxs-lookup"><span data-stu-id="61486-160">It is possible, and allowed by the standard, to embed the image stream inside another type of file container.</span></span> <span data-ttu-id="61486-161">編碼器支援僅限資料流程模式，會輸出沒有映射容器的原始影像位串流。</span><span class="sxs-lookup"><span data-stu-id="61486-161">The encoder supports a stream-only mode, which outputs the raw image bit stream with no image container.</span></span> <span data-ttu-id="61486-162">應用程式可以將位資料流程儲存為一些其他的容器格式。</span><span class="sxs-lookup"><span data-stu-id="61486-162">An application can store the bit stream in some other container format.</span></span>

<span data-ttu-id="61486-163">若要啟用僅限資料流程模式，請設定 **StreamOnly** 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-163">To enable stream-only mode, set the **StreamOnly** property.</span></span>

### <a name="image-quality-settings"></a><span data-ttu-id="61486-164">影像品質設定</span><span class="sxs-lookup"><span data-stu-id="61486-164">Image Quality Settings</span></span>

<span data-ttu-id="61486-165">數個編解碼器屬性會控制編碼器的輸出影像品質。</span><span class="sxs-lookup"><span data-stu-id="61486-165">Several codec properties control the quality of the output image from the encoder.</span></span>

-   <span data-ttu-id="61486-166">[ImageQuality](#imagequality) 是在 WIC 編解碼器之間的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-166">[ImageQuality](#imagequality) is a property common across WIC codecs.</span></span> <span data-ttu-id="61486-167">它會將影像品質指定為0.0 –1.0 的單一浮點值，</span><span class="sxs-lookup"><span data-stu-id="61486-167">It specifies image quality as a single floating-point value from 0.0–1.0,</span></span>
-   <span data-ttu-id="61486-168">[ [品質](#image-quality-settings)]、[重 [迭](#overlap)] 和 [ [取樣](#subsampling) ] 屬性能讓您更充分掌控品質設定。</span><span class="sxs-lookup"><span data-stu-id="61486-168">The [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties give more control over the quality settings.</span></span>

<span data-ttu-id="61486-169">若要使用「 [品質](#image-quality-settings)」、「重 [迭](#overlap)」和「 [取樣](#subsampling) 」屬性，請將 [UseCodecOptions](#usecodecoptions) 屬性設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="61486-169">To use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties, set the [UseCodecOptions](#usecodecoptions) property to **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="61486-170">如果 [UseCodecOptions](#usecodecoptions) 是 **Variant \_ false** (**Variant \_ false** 是) 編碼器使用 [ImageQuality](#imagequality) 屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="61486-170">If [UseCodecOptions](#usecodecoptions) is **VARIANT\_FALSE** (**VARIANT\_FALSE** is the default) the encoder uses the [ImageQuality](#imagequality) property.</span></span> <span data-ttu-id="61486-171">編碼器會透過查閱資料表，將 ImageQuality 的值對應到 [品質](#image-quality-settings)、重 [迭](#overlap)和次 [取樣](#subsampling) 。</span><span class="sxs-lookup"><span data-stu-id="61486-171">The encoder maps the value of ImageQuality to [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) through a lookup table.</span></span>

<span data-ttu-id="61486-172">編碼器不支援 **CompressionQuality** 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-172">The encoder does not support the **CompressionQuality** property.</span></span>

### <a name="compressed-domain-transcode"></a><span data-ttu-id="61486-173">壓縮的網域轉碼</span><span class="sxs-lookup"><span data-stu-id="61486-173">Compressed Domain Transcode</span></span>

<span data-ttu-id="61486-174">JPEG XR 編解碼器可以執行某些影像轉換，而不需要實際解碼壓縮的資料並重新編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-174">The JPEG XR codec can perform certain image transformations without actually decoding the compressed data and re-encoding it.</span></span> <span data-ttu-id="61486-175">壓縮的網域作業非常有效率，而且可避免在您將損及重新編碼已壓縮的影像時，通常會發生的任何額外品質損失。</span><span class="sxs-lookup"><span data-stu-id="61486-175">Compressed domain operations are very efficient and avoid any additional quality loss that is typical when you decode and re-encode a lossy-compressed image.</span></span>

<span data-ttu-id="61486-176">以下是支援的壓縮網域作業：</span><span class="sxs-lookup"><span data-stu-id="61486-176">The following compressed domain operations are supported:</span></span>

-   <span data-ttu-id="61486-177">裁剪影像的區域。</span><span class="sxs-lookup"><span data-stu-id="61486-177">Crop a region of the image.</span></span>
-   <span data-ttu-id="61486-178">旋轉或翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="61486-178">Rotate or flip the image.</span></span>
-   <span data-ttu-id="61486-179">捨棄頻率資料來建立較小的影像檔案。</span><span class="sxs-lookup"><span data-stu-id="61486-179">Discard frequency data to create a smaller image file.</span></span>
-   <span data-ttu-id="61486-180">重新組織空間與頻率順序之間的影像。</span><span class="sxs-lookup"><span data-stu-id="61486-180">Reorganize the image between spatial and frequency order.</span></span>

<span data-ttu-id="61486-181">如果來源影像是 JPEG XR 影像，JPEG XR 編碼器會使用壓縮的網域轉碼（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="61486-181">The JPEG XR encoder uses compressed domain transcoding, if possible, when the source image is a JPEG XR image.</span></span> <span data-ttu-id="61486-182">當編碼器執行壓縮的網域作業時，它會忽略下列編解碼器屬性： [AlphaQuality](#alphaquality)、 [ImageQuality](#imagequality)、InterleavedAlpha [、不](#lossless)失真重[迭](#overlap)和[品質](#image-quality-settings)。 [](#interleavedalpha)</span><span class="sxs-lookup"><span data-stu-id="61486-182">When the encoder performs a compressed domain operation, it ignores the following codec properties: [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), [Lossless](#lossless)[Overlap](#overlap), and [Quality](#image-quality-settings).</span></span> <span data-ttu-id="61486-183">如果 [HorizontalTileSlices](/windows) 和 [VerticalTileSlices](/windows) 屬性存在，您必須將它們設定為零。</span><span class="sxs-lookup"><span data-stu-id="61486-183">If the [HorizontalTileSlices](/windows) and [VerticalTileSlices](/windows) properties are present, you must set them to zero.</span></span> <span data-ttu-id="61486-184">您無法在壓縮的網域轉碼中變更影像的磚大小。</span><span class="sxs-lookup"><span data-stu-id="61486-184">You cannot change the tile size of an image as part of a compressed domain transcode.</span></span>

<span data-ttu-id="61486-185">下列清單說明如何執行影像轉換。</span><span class="sxs-lookup"><span data-stu-id="61486-185">The follow list describes how to perform the image transformations.</span></span>

-   <span data-ttu-id="61486-186">若要裁剪影像，請在 **WriteSource** 方法的 [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)參數中設定所需的區域。</span><span class="sxs-lookup"><span data-stu-id="61486-186">To crop the image, set the desired region in the [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) parameter of the **WriteSource** method.</span></span>
-   <span data-ttu-id="61486-187">若要旋轉或翻轉影像，請設定 [BitmapTransform](#bitmaptransform) 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-187">To rotate or flip the image, set the [BitmapTransform](#bitmaptransform) property.</span></span>
-   <span data-ttu-id="61486-188">若要捨棄映射中的頻率資料，請設定 [ImageDataDiscard](#imagedatadiscard) 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-188">To discard frequency data in the image, set the [ImageDataDiscard](#imagedatadiscard) property.</span></span> <span data-ttu-id="61486-189">若要捨棄 Alpha 通道中的頻率資料，請設定 [AlphaDataDiscard](#alphadatadiscard) 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-189">To discard frequency data in the alpha channel, set the [AlphaDataDiscard](#alphadatadiscard) property.</span></span> <span data-ttu-id="61486-190">捨棄頻率資料可減少編碼的檔案大小，並可減少解析度。</span><span class="sxs-lookup"><span data-stu-id="61486-190">Discarding frequency data reduces the encoded file size and can reduce the resolution.</span></span>
-   <span data-ttu-id="61486-191">若要在頻率和空間排序之間變更影像組織，請設定 [FrequencyOrdering](/windows) 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-191">To change the image organization between frequency and spatial ordering, set the [FrequencyOrdering](/windows) property.</span></span>

<span data-ttu-id="61486-192">若要停用壓縮的網域轉碼，並強制編碼器重新編碼影像，請將 [UseCodecOptions](#usecodecoptions) 設定為 **variant \_ TRUE** ，並將 [CompressedDomainTranscode](#compresseddomaintranscode) 設定為 **variant \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="61486-192">To disable compressed domain transcode and force the encoder to re-encode the image, set the [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE** and set [CompressedDomainTranscode](#compresseddomaintranscode) to **VARIANT\_FALSE**.</span></span>

## <a name="encoder-options"></a><span data-ttu-id="61486-193">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="61486-193">Encoder Options</span></span>

<span data-ttu-id="61486-194">若要設定編碼屬性，請使用 [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="61486-194">To set encoding properties, use the [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) interface.</span></span> <span data-ttu-id="61486-195">如需詳細資訊，請參閱 [編碼總覽](-wic-creating-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="61486-195">For more information, see the [Encoding Overview](-wic-creating-encoder.md).</span></span>

<span data-ttu-id="61486-196">下列清單指定編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="61486-196">The following list specifies the encoder options.</span></span>

-   [<span data-ttu-id="61486-197">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61486-197">AlphaDataDiscard</span></span>](#alphadatadiscard)
-   [<span data-ttu-id="61486-198">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="61486-198">AlphaQuality</span></span>](#alphaquality)
-   [<span data-ttu-id="61486-199">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="61486-199">BitmapTransform</span></span>](#bitmaptransform)
-   [<span data-ttu-id="61486-200">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="61486-200">CompressedDomainTranscode</span></span>](#compresseddomaintranscode)
-   [<span data-ttu-id="61486-201">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="61486-201">FrequencyOrder</span></span>](#frequencyorder)
-   [<span data-ttu-id="61486-202">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61486-202">HorizontalTileSlices</span></span>](#horizontaltileslices)
-   [<span data-ttu-id="61486-203">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="61486-203">IgnoreOverlap</span></span>](#ignoreoverlap)
-   [<span data-ttu-id="61486-204">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61486-204">ImageDataDiscard</span></span>](#imagedatadiscard)
-   [<span data-ttu-id="61486-205">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="61486-205">ImageQuality</span></span>](#imagequality)
-   [<span data-ttu-id="61486-206">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-206">InterleavedAlpha</span></span>](#interleavedalpha)
-   [<span data-ttu-id="61486-207">Lossless</span><span class="sxs-lookup"><span data-stu-id="61486-207">Lossless</span></span>](#lossless)
-   [<span data-ttu-id="61486-208">重疊</span><span class="sxs-lookup"><span data-stu-id="61486-208">Overlap</span></span>](#overlap)
-   [<span data-ttu-id="61486-209">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="61486-209">ProgressiveMode</span></span>](#progressivemode)
-   [<span data-ttu-id="61486-210">品質</span><span class="sxs-lookup"><span data-stu-id="61486-210">Quality</span></span>](#image-quality-settings)
-   [<span data-ttu-id="61486-211">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="61486-211">StreamOnly</span></span>](#streamonly)
-   [<span data-ttu-id="61486-212">圖元</span><span class="sxs-lookup"><span data-stu-id="61486-212">Subsampling</span></span>](#subsampling)
-   [<span data-ttu-id="61486-213">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="61486-213">UseCodecOptions</span></span>](#usecodecoptions)
-   [<span data-ttu-id="61486-214">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61486-214">VerticalTileSlices</span></span>](#verticaltileslices)

### <a name="alphadatadiscard"></a><span data-ttu-id="61486-215">AlphaDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61486-215">AlphaDataDiscard</span></span>

<span data-ttu-id="61486-216">設定壓縮的網域轉碼期間要捨棄的 Alpha 頻率資料量。</span><span class="sxs-lookup"><span data-stu-id="61486-216">Sets the amount of alpha frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="61486-217">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-217">Data type</span></span> | <span data-ttu-id="61486-218">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-218">VARTYPE</span></span>     | <span data-ttu-id="61486-219">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-219">Range</span></span> | <span data-ttu-id="61486-220">預設</span><span class="sxs-lookup"><span data-stu-id="61486-220">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61486-221">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-221">**UCHAR**</span></span> | <span data-ttu-id="61486-222">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-222">**VT\_UI1**</span></span> | <span data-ttu-id="61486-223">0–4</span><span class="sxs-lookup"><span data-stu-id="61486-223">0–4</span></span>   | <span data-ttu-id="61486-224">無</span><span class="sxs-lookup"><span data-stu-id="61486-224">None</span></span>    |



 

<span data-ttu-id="61486-225">只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** ，且影像包含平面 Alpha 色板或交錯 Alpha 色板時，才會套用這個屬性; 否則會忽略此屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-225">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and the image contains either a planar alpha channel or interleaved alpha channel; otherwise it is ignored.</span></span>

<span data-ttu-id="61486-226">針對包含平面 Alpha 色板的影像，下列值是有效的。</span><span class="sxs-lookup"><span data-stu-id="61486-226">For images that contain a planar alpha channel, the following values are valid.</span></span>



| <span data-ttu-id="61486-227">值</span><span class="sxs-lookup"><span data-stu-id="61486-227">Value</span></span> | <span data-ttu-id="61486-228">描述</span><span class="sxs-lookup"><span data-stu-id="61486-228">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61486-229">0</span><span class="sxs-lookup"><span data-stu-id="61486-229">0</span></span>     | <span data-ttu-id="61486-230">不捨棄影像頻率資料。</span><span class="sxs-lookup"><span data-stu-id="61486-230">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="61486-231">1</span><span class="sxs-lookup"><span data-stu-id="61486-231">1</span></span>     | <span data-ttu-id="61486-232">Flexbits 會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="61486-232">The flexbits are discarded.</span></span> <span data-ttu-id="61486-233">這可任意減少轉碼影像的平面 Alpha 通道品質。</span><span class="sxs-lookup"><span data-stu-id="61486-233">This arbitrarily reduces the quality of the planar alpha channel for the transcoded image.</span></span> <span data-ttu-id="61486-234">，而不會變更有效的解決方式。</span><span class="sxs-lookup"><span data-stu-id="61486-234">, without a change in the effective resolution.</span></span> <span data-ttu-id="61486-235">檔案大小和品質的確切縮減取決於許多因素，而且無法完全指定。</span><span class="sxs-lookup"><span data-stu-id="61486-235">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="61486-236">2</span><span class="sxs-lookup"><span data-stu-id="61486-236">2</span></span>     | <span data-ttu-id="61486-237">會捨棄高通過頻率的資料區，包括 flexbits。</span><span class="sxs-lookup"><span data-stu-id="61486-237">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="61486-238">這可有效地將平面 Alpha 通道的解析度減少為兩個維度的4倍。</span><span class="sxs-lookup"><span data-stu-id="61486-238">This effectively reduces the resolution of the planar alpha channel by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="61486-239">轉碼影像的實際維度會維持不變，但影像會遺失 Alpha 通道圖元每個4x4 區塊中的所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61486-239">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of alpha-channel pixels.</span></span> <span data-ttu-id="61486-240">一般來說，只有當 [ImageDataDiscard](#imagedatadiscard) 屬性具有相同的值時，才應該設定這個值。</span><span class="sxs-lookup"><span data-stu-id="61486-240">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span>                            |
| <span data-ttu-id="61486-241">3</span><span class="sxs-lookup"><span data-stu-id="61486-241">3</span></span>     | <span data-ttu-id="61486-242">系統會捨棄「高階」和「低通路」頻率資料格（包括 flexbits）。</span><span class="sxs-lookup"><span data-stu-id="61486-242">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="61486-243">這項 ffectively 可減少平面 Alpha 通道的解析度，因為這兩個維度的因數都是16。</span><span class="sxs-lookup"><span data-stu-id="61486-243">This ffectively reduces the resolution of the planar alpha channel by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="61486-244">轉碼影像的實際維度會維持不變，但影像會在每16x16 巨大區塊的 Alpha 通道圖元中遺失所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61486-244">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of alpha-channel pixels.</span></span> <span data-ttu-id="61486-245">一般來說，只有當 [ImageDataDiscard](#imagedatadiscard) 屬性具有相同的值時，才應該設定這個值。</span><span class="sxs-lookup"><span data-stu-id="61486-245">Typically, you should set this value only when the [ImageDataDiscard](#imagedatadiscard) property has the same value.</span></span> |
| <span data-ttu-id="61486-246">4</span><span class="sxs-lookup"><span data-stu-id="61486-246">4</span></span>     | <span data-ttu-id="61486-247">完全捨棄 Alpha 色頻 (Alpha Channel)。</span><span class="sxs-lookup"><span data-stu-id="61486-247">The alpha channel is completely discarded.</span></span> <span data-ttu-id="61486-248">轉碼影像的像素格式會變更，以反映 Alpha 色板的移除。</span><span class="sxs-lookup"><span data-stu-id="61486-248">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="61486-249">針對包含交錯 Alpha 色板的影像，下列值有效。</span><span class="sxs-lookup"><span data-stu-id="61486-249">For images that contain an interleaved alpha channel, the following value is valid.</span></span>



| <span data-ttu-id="61486-250">值</span><span class="sxs-lookup"><span data-stu-id="61486-250">Value</span></span> | <span data-ttu-id="61486-251">描述</span><span class="sxs-lookup"><span data-stu-id="61486-251">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61486-252">4</span><span class="sxs-lookup"><span data-stu-id="61486-252">4</span></span>     | <span data-ttu-id="61486-253">完全捨棄 Alpha 色頻 (Alpha Channel)。</span><span class="sxs-lookup"><span data-stu-id="61486-253">The alpha channel is completely discarded.</span></span> <span data-ttu-id="61486-254">轉碼影像的像素格式會變更，以反映 Alpha 色板的移除。</span><span class="sxs-lookup"><span data-stu-id="61486-254">The pixel format of the transcoded image is changed to reflect the removal of the alpha channel.</span></span> |



 

<span data-ttu-id="61486-255">針對交錯 Alpha，除非這個屬性設定為4，否則 Alpha 通道會根據 [ImageDataDiscard](#imagedatadiscard) 屬性的值，處理與影像資料相同的處理。</span><span class="sxs-lookup"><span data-stu-id="61486-255">For interleaved alpha, unless this property is set to 4, the alpha channel is processed the same as the image data, according to the value of the [ImageDataDiscard](#imagedatadiscard) property.</span></span>

### <a name="alphaquality"></a><span data-ttu-id="61486-256">AlphaQuality</span><span class="sxs-lookup"><span data-stu-id="61486-256">AlphaQuality</span></span>

<span data-ttu-id="61486-257">設定平面 Alpha 通道影像的壓縮品質。</span><span class="sxs-lookup"><span data-stu-id="61486-257">Sets the compression quality for the planar alpha channel image.</span></span>



| <span data-ttu-id="61486-258">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-258">Data type</span></span> | <span data-ttu-id="61486-259">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-259">VARTYPE</span></span>     | <span data-ttu-id="61486-260">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-260">Range</span></span> | <span data-ttu-id="61486-261">預設</span><span class="sxs-lookup"><span data-stu-id="61486-261">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61486-262">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-262">**UCHAR**</span></span> | <span data-ttu-id="61486-263">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-263">**VT\_UI1**</span></span> | <span data-ttu-id="61486-264">1–255</span><span class="sxs-lookup"><span data-stu-id="61486-264">1–255</span></span> | <span data-ttu-id="61486-265">1</span><span class="sxs-lookup"><span data-stu-id="61486-265">1</span></span>       |



 

<span data-ttu-id="61486-266">當影像具有 Alpha 色板，且 [InterleavedAlpha](#interleavedalpha) 屬性為 **VARIANT \_ FALSE** 時，就會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-266">This property applies when the image has an alpha channel and the [InterleavedAlpha](#interleavedalpha) property is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="61486-267">值1表示無失真模式。</span><span class="sxs-lookup"><span data-stu-id="61486-267">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="61486-268">增加值會產生較高的壓縮比例和較低的影像品質。</span><span class="sxs-lookup"><span data-stu-id="61486-268">Increasing values result in higher compression ratios and lower image quality.</span></span>

### <a name="bitmaptransform"></a><span data-ttu-id="61486-269">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="61486-269">BitmapTransform</span></span>

<span data-ttu-id="61486-270">指定是否在解碼時旋轉或翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="61486-270">Specifies whether the image is rotated or flipped when decoded.</span></span>



| <span data-ttu-id="61486-271">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-271">Data type</span></span> | <span data-ttu-id="61486-272">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-272">VARTYPE</span></span>     | <span data-ttu-id="61486-273">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-273">Range</span></span>                                                                     | <span data-ttu-id="61486-274">預設</span><span class="sxs-lookup"><span data-stu-id="61486-274">Default</span></span>                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="61486-275">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-275">**UCHAR**</span></span> | <span data-ttu-id="61486-276">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-276">**VT\_UI1**</span></span> | [<span data-ttu-id="61486-277">**WICBitmapTransformOptions**</span><span class="sxs-lookup"><span data-stu-id="61486-277">**WICBitmapTransformOptions**</span></span>](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | <span data-ttu-id="61486-278">**WICBitmapTransformRotate0**</span><span class="sxs-lookup"><span data-stu-id="61486-278">**WICBitmapTransformRotate0**</span></span> |



 

### <a name="compresseddomaintranscode"></a><span data-ttu-id="61486-279">CompressedDomainTranscode</span><span class="sxs-lookup"><span data-stu-id="61486-279">CompressedDomainTranscode</span></span>

<span data-ttu-id="61486-280">啟用或停用壓縮的網域轉碼。</span><span class="sxs-lookup"><span data-stu-id="61486-280">Enables or disables compressed domain transcoding.</span></span>



| <span data-ttu-id="61486-281">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-281">Data type</span></span>         | <span data-ttu-id="61486-282">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-282">VARTYPE</span></span>      | <span data-ttu-id="61486-283">預設</span><span class="sxs-lookup"><span data-stu-id="61486-283">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="61486-284">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-284">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-285">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-285">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-286">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61486-286">**VARIANT\_TRUE**</span></span> |



 

<span data-ttu-id="61486-287">若要停用壓縮的網域作業，請將此屬性設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="61486-287">To disable compressed domain operations, set this property to **VARIANT\_FALSE**.</span></span>

### <a name="frequencyorder"></a><span data-ttu-id="61486-288">FrequencyOrder</span><span class="sxs-lookup"><span data-stu-id="61486-288">FrequencyOrder</span></span>

<span data-ttu-id="61486-289">依頻率順序啟用編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-289">Enables encoding in frequency order.</span></span> <span data-ttu-id="61486-290">JPEG XR 編碼器的裝置執行可依空間順序組織檔案，以減少編碼期間所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="61486-290">Device implementations of JPEG XR encoders can organize a file in spatial order to reduce the memory required during encoding.</span></span>



| <span data-ttu-id="61486-291">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-291">Data type</span></span>         | <span data-ttu-id="61486-292">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-292">VARTYPE</span></span>      | <span data-ttu-id="61486-293">預設</span><span class="sxs-lookup"><span data-stu-id="61486-293">Default</span></span>           |
|-------------------|--------------|-------------------|
| <span data-ttu-id="61486-294">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-294">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-295">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-295">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-296">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61486-296">**VARIANT\_TRUE**</span></span> |



 

-   <span data-ttu-id="61486-297">**變異 \_TRUE**：頻率順序。</span><span class="sxs-lookup"><span data-stu-id="61486-297">**VARIANT\_TRUE**: Frequency order.</span></span> <span data-ttu-id="61486-298">頻率最低的資料會先出現在檔案中，而影像內容會依其頻率（而非其空間方向）來分組。</span><span class="sxs-lookup"><span data-stu-id="61486-298">The lowest frequency data appears first in the file, and image content is grouped by its frequency rather than its spatial orientation.</span></span> <span data-ttu-id="61486-299">依頻率順序組織檔案，可為任何以頻率為基礎的解碼提供最佳效能。</span><span class="sxs-lookup"><span data-stu-id="61486-299">Organizing a file by frequency order provides the best performance for any frequency-based decoding.</span></span>
-   <span data-ttu-id="61486-300">**變異 \_FALSE**：空間順序。</span><span class="sxs-lookup"><span data-stu-id="61486-300">**VARIANT\_FALSE**: Spatial order.</span></span> <span data-ttu-id="61486-301">空間順序可減少編碼期間所需的記憶體</span><span class="sxs-lookup"><span data-stu-id="61486-301">Spatial order reduces the memory required during encoding</span></span>

<span data-ttu-id="61486-302">除非您有使用空間順序的效能或應用程式特定的原因，否則建議使用頻率順序。</span><span class="sxs-lookup"><span data-stu-id="61486-302">Frequency order is recommended unless you have performance or application-specific reasons to use spatial order.</span></span>

### <a name="horizontaltileslices"></a><span data-ttu-id="61486-303">HorizontalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61486-303">HorizontalTileSlices</span></span>

<span data-ttu-id="61486-304">設定水準磚的數目。</span><span class="sxs-lookup"><span data-stu-id="61486-304">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="61486-305">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-305">Data type</span></span>  | <span data-ttu-id="61486-306">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-306">VARTYPE</span></span>     | <span data-ttu-id="61486-307">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-307">Range</span></span>  | <span data-ttu-id="61486-308">預設</span><span class="sxs-lookup"><span data-stu-id="61486-308">Default</span></span>                      |
|------------|-------------|--------|------------------------------|
| <span data-ttu-id="61486-309">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="61486-309">**USHORT**</span></span> | <span data-ttu-id="61486-310">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="61486-310">**VT\_UI2**</span></span> | <span data-ttu-id="61486-311">0–4095</span><span class="sxs-lookup"><span data-stu-id="61486-311">0–4095</span></span> | <span data-ttu-id="61486-312"> (影像寬度– 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="61486-312">(image width – 1) >> 8</span></span> |



 

<span data-ttu-id="61486-313">值是水準細分的數目;亦即水準磚的數目–1。</span><span class="sxs-lookup"><span data-stu-id="61486-313">The value is the number of horizontal subdivisions; that is, the number of horizontal tiles – 1.</span></span>

### <a name="ignoreoverlap"></a><span data-ttu-id="61486-314">IgnoreOverlap</span><span class="sxs-lookup"><span data-stu-id="61486-314">IgnoreOverlap</span></span>

<span data-ttu-id="61486-315">指定編碼器在壓縮的網域轉碼期間處理磚邊界的方式。</span><span class="sxs-lookup"><span data-stu-id="61486-315">Specifies how the encoder handles tile boundaries during a compressed domain transcode.</span></span>



| <span data-ttu-id="61486-316">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-316">Data type</span></span>         | <span data-ttu-id="61486-317">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-317">VARTYPE</span></span>      | <span data-ttu-id="61486-318">預設</span><span class="sxs-lookup"><span data-stu-id="61486-318">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61486-319">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-319">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-320">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-320">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-321">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-321">**VARIANT\_FALSE**</span></span> |



 

<span data-ttu-id="61486-322">只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** ，而且只執行一或多個磚的子領域轉碼時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-322">This property is applied only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE** and a sub-region transcode of exactly one or more tiles is performed.</span></span>

<span data-ttu-id="61486-323">區域轉碼的預設作業是擴充要求的區域，以包含重迭區域邊緣所需的周圍圖元。</span><span class="sxs-lookup"><span data-stu-id="61486-323">The default operation for a region transcode is to expand the requested region to include the surrounding pixels that are required for overlap decoding of the region edges.</span></span> <span data-ttu-id="61486-324">如果這個屬性設定為 **VARIANT \_ TRUE**，則編解碼器會忽略周圍的圖元，而只會解壓縮選取的磚或磚。</span><span class="sxs-lookup"><span data-stu-id="61486-324">If this property is set to **VARIANT\_TRUE**, the codec ignores the surrounding pixels, and only the selected tile or tiles are extracted.</span></span> <span data-ttu-id="61486-325">如果來源影像未並排顯示或要求的區域包含部分磚，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="61486-325">If the source image is not tiled or if the requested region includes partial tiles, this parameter is ignored.</span></span>

### <a name="imagedatadiscard"></a><span data-ttu-id="61486-326">ImageDataDiscard</span><span class="sxs-lookup"><span data-stu-id="61486-326">ImageDataDiscard</span></span>

<span data-ttu-id="61486-327">設定壓縮的網域轉碼期間要捨棄的映射頻率資料量。</span><span class="sxs-lookup"><span data-stu-id="61486-327">Sets the amount of image frequency data to discard during a compressed domain transcode.</span></span>



| <span data-ttu-id="61486-328">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-328">Data type</span></span> | <span data-ttu-id="61486-329">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-329">VARTYPE</span></span>     | <span data-ttu-id="61486-330">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-330">Range</span></span> | <span data-ttu-id="61486-331">預設</span><span class="sxs-lookup"><span data-stu-id="61486-331">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61486-332">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-332">**UCHAR**</span></span> | <span data-ttu-id="61486-333">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-333">**VT\_UI1**</span></span> | <span data-ttu-id="61486-334">0–3</span><span class="sxs-lookup"><span data-stu-id="61486-334">0–3</span></span>   | <span data-ttu-id="61486-335">0</span><span class="sxs-lookup"><span data-stu-id="61486-335">0</span></span>       |



 

<span data-ttu-id="61486-336">只有當 [CompressedDomainTranscode](#compresseddomaintranscode) 屬性設定為 **VARIANT \_ TRUE** 時，才會套用這個屬性; 否則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="61486-336">This property applies only if the [CompressedDomainTranscode](#compresseddomaintranscode) property is set to **VARIANT\_TRUE**; otherwise it is ignored.</span></span>



| <span data-ttu-id="61486-337">值</span><span class="sxs-lookup"><span data-stu-id="61486-337">Value</span></span> | <span data-ttu-id="61486-338">描述</span><span class="sxs-lookup"><span data-stu-id="61486-338">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61486-339">0</span><span class="sxs-lookup"><span data-stu-id="61486-339">0</span></span>     | <span data-ttu-id="61486-340">不捨棄影像頻率資料。</span><span class="sxs-lookup"><span data-stu-id="61486-340">No image frequency data is discarded.</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="61486-341">1</span><span class="sxs-lookup"><span data-stu-id="61486-341">1</span></span>     | <span data-ttu-id="61486-342">Flexbits 會被捨棄。</span><span class="sxs-lookup"><span data-stu-id="61486-342">The flexbits are discarded.</span></span> <span data-ttu-id="61486-343">這可任意減少轉碼影像的品質，而不會變更影像的有效解析度。</span><span class="sxs-lookup"><span data-stu-id="61486-343">This arbitrarily reduces the quality of the transcoded image without changing the effective resolution of the image.</span></span> <span data-ttu-id="61486-344">檔案大小和品質的確切縮減取決於許多因素，而且無法完全指定。</span><span class="sxs-lookup"><span data-stu-id="61486-344">The exact reduction in file size and quality depends on numerous factors and cannot be exactly specified.</span></span> <span data-ttu-id="61486-345">這個值會傳回針對交錯 Alpha 色板指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="61486-345">This value returns an error specified for an interleaved alpha channel.</span></span>                                                                                |
| <span data-ttu-id="61486-346">2</span><span class="sxs-lookup"><span data-stu-id="61486-346">2</span></span>     | <span data-ttu-id="61486-347">會捨棄高通過頻率的資料區，包括 flexbits。</span><span class="sxs-lookup"><span data-stu-id="61486-347">The high-pass frequency data band is discarded, including the flexbits.</span></span> <span data-ttu-id="61486-348">這可減少轉碼影像的解析度，因為這兩個維度的因數為4。</span><span class="sxs-lookup"><span data-stu-id="61486-348">This reduces the resolution of the transcoded image by a factor of 4 in both dimensions.</span></span> <span data-ttu-id="61486-349">轉碼影像的實際維度會維持不變，但影像會遺失每個4x4 圖元區塊中的所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61486-349">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 4x4 block of pixels.</span></span> <span data-ttu-id="61486-350">因此，每次解碼轉碼映射時，應據以 >downsampled。</span><span class="sxs-lookup"><span data-stu-id="61486-350">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span>                             |
| <span data-ttu-id="61486-351">3</span><span class="sxs-lookup"><span data-stu-id="61486-351">3</span></span>     | <span data-ttu-id="61486-352">系統會捨棄「高階」和「低通路」頻率資料格（包括 flexbits）。</span><span class="sxs-lookup"><span data-stu-id="61486-352">Both the high-pass and low-pass frequency data bands are discarded, including the flexbits.</span></span> <span data-ttu-id="61486-353">這可減少轉碼影像的解析度，因為這兩個維度的因數都是16。</span><span class="sxs-lookup"><span data-stu-id="61486-353">This reduces the resolution of the transcoded image by a factor of 16 in both dimensions.</span></span> <span data-ttu-id="61486-354">轉碼影像的實際維度會維持不變，但影像會在每16x16 巨大區塊的圖元中失去所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="61486-354">The actual dimensions of the transcoded image remain the same, but the image loses all detail in each 16x16 macroblock of pixels.</span></span> <span data-ttu-id="61486-355">因此，每次解碼轉碼映射時，應據以 >downsampled。</span><span class="sxs-lookup"><span data-stu-id="61486-355">Therefore, the transcoded image should be downsampled accordingly whenever it is decoded.</span></span> |



 

<span data-ttu-id="61486-356">如果影像包含交錯的 Alpha 色板，除非[AlphaDataDiscard](#alphadatadiscard)屬性設定為4，否則會將[ImageDataDiscard](#imagedatadiscard)的值套用至 Alpha 色板，在此情況下會捨棄 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="61486-356">If the image contains an interleaved alpha channel, the value of [ImageDataDiscard](#imagedatadiscard) is applied to the alpha channel unless the [AlphaDataDiscard](#alphadatadiscard) property is set to 4, in which case the alpha channel is discarded.</span></span>

<span data-ttu-id="61486-357">若是平面 Alpha，捨棄的頻率資料是由 [AlphaDataDiscard](#alphadatadiscard) 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="61486-357">For planar alpha, the frequency data that is discarded is controlled by the [AlphaDataDiscard](#alphadatadiscard) property.</span></span>

### <a name="imagequality"></a><span data-ttu-id="61486-358">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="61486-358">ImageQuality</span></span>

<span data-ttu-id="61486-359">設定影像品質。</span><span class="sxs-lookup"><span data-stu-id="61486-359">Sets the image quality.</span></span>



| <span data-ttu-id="61486-360">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-360">Data type</span></span> | <span data-ttu-id="61486-361">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-361">VARTYPE</span></span>    | <span data-ttu-id="61486-362">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-362">Range</span></span> | <span data-ttu-id="61486-363">預設</span><span class="sxs-lookup"><span data-stu-id="61486-363">Default</span></span> |
|-----------|------------|-------|---------|
| <span data-ttu-id="61486-364">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="61486-364">**FLOAT**</span></span> | <span data-ttu-id="61486-365">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="61486-365">**VT\_R4**</span></span> | <span data-ttu-id="61486-366">0–1。0</span><span class="sxs-lookup"><span data-stu-id="61486-366">0–1.0</span></span> | <span data-ttu-id="61486-367">0.9</span><span class="sxs-lookup"><span data-stu-id="61486-367">0.9</span></span>     |



 

<span data-ttu-id="61486-368">層級1.0 提供數學無損的壓縮。</span><span class="sxs-lookup"><span data-stu-id="61486-368">Level 1.0 gives mathematically lossless compression.</span></span>

<span data-ttu-id="61486-369">層級0.0 是最低品質設定。</span><span class="sxs-lookup"><span data-stu-id="61486-369">Level 0.0 is the lowest quality setting.</span></span>

### <a name="interleavedalpha"></a><span data-ttu-id="61486-370">InterleavedAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-370">InterleavedAlpha</span></span>

<span data-ttu-id="61486-371">指定是否要編碼交錯的 Alpha 或平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-371">Specifies whether to encode interleaved alpha or planar alpha.</span></span>



| <span data-ttu-id="61486-372">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-372">Data type</span></span>         | <span data-ttu-id="61486-373">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-373">VARTYPE</span></span>      | <span data-ttu-id="61486-374">預設</span><span class="sxs-lookup"><span data-stu-id="61486-374">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61486-375">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-375">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-376">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-376">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-377">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-377">**VARIANT\_FALSE**</span></span> |



 

-   <span data-ttu-id="61486-378">**變異 \_TRUE**：交錯的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-378">**VARIANT\_TRUE**: Interleaved alpha.</span></span> <span data-ttu-id="61486-379">Alpha 色板資訊會編碼為額外的交錯通道，而且沒有與影像內容通道的相互關聯。</span><span class="sxs-lookup"><span data-stu-id="61486-379">Alpha channel information is encoded as an additional interleaved channel, with no correlation to the image content channels.</span></span> <span data-ttu-id="61486-380">當影像正在串流時，此模式非常適合用來在影像中同時解碼 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-380">This mode is useful for decoding alpha simultaneously with the image when the image is streaming.</span></span>
-   <span data-ttu-id="61486-381">VARIANT \_ FALSE：平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-381">VARIANT\_FALSE: Planar alpha.</span></span> <span data-ttu-id="61486-382">平面 Alpha 通道會編碼為個別的影像。</span><span class="sxs-lookup"><span data-stu-id="61486-382">A planar alpha channel is encoded as a separate image.</span></span> <span data-ttu-id="61486-383">影像資料和 Alpha 通道會獨立解碼。</span><span class="sxs-lookup"><span data-stu-id="61486-383">The image data and the alpha channel are decoded independently.</span></span> <span data-ttu-id="61486-384">（選擇性）您可以藉由設定 [AlphaQuality](#alphaquality) 屬性來設定 Alpha 色板的品質等級。</span><span class="sxs-lookup"><span data-stu-id="61486-384">Optionally, you can set the quality level of the alpha channel by setting the [AlphaQuality](#alphaquality) property.</span></span>

<span data-ttu-id="61486-385">只有某些 RGB 像素格式支援交錯 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-385">Interleaved alpha is supported only for certain RGB pixel formats.</span></span> <span data-ttu-id="61486-386">任何定義 Alpha 色板的影像格式都支援平面 Alpha。</span><span class="sxs-lookup"><span data-stu-id="61486-386">Planar alpha is supported for any image format that defines an alpha channel.</span></span>

### <a name="lossless"></a><span data-ttu-id="61486-387">Lossless</span><span class="sxs-lookup"><span data-stu-id="61486-387">Lossless</span></span>

<span data-ttu-id="61486-388">啟用遺失壓縮。</span><span class="sxs-lookup"><span data-stu-id="61486-388">Enables losses compression.</span></span>



| <span data-ttu-id="61486-389">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-389">Data type</span></span>         | <span data-ttu-id="61486-390">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-390">VARTYPE</span></span>      | <span data-ttu-id="61486-391">預設</span><span class="sxs-lookup"><span data-stu-id="61486-391">Default</span></span>        |
|-------------------|--------------|----------------|
| <span data-ttu-id="61486-392">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-392">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-393">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-393">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-394">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="61486-394">VARIANT\_FALSE</span></span> |



 

<span data-ttu-id="61486-395">如果值為 **VARIANT \_ TRUE**，編碼器會使用不失真壓縮。</span><span class="sxs-lookup"><span data-stu-id="61486-395">If the value is **VARIANT\_TRUE**, the encoder uses lossless compression.</span></span> <span data-ttu-id="61486-396">當設定為 **VARIANT \_ TRUE** 時，此屬性會覆寫 [ImageQuality](#imagequality) 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-396">When set to **VARIANT\_TRUE**, this property overrides the [ImageQuality](#imagequality) property.</span></span>

### <a name="overlap"></a><span data-ttu-id="61486-397">重疊</span><span class="sxs-lookup"><span data-stu-id="61486-397">Overlap</span></span>

<span data-ttu-id="61486-398">設定重迭篩選的層級。</span><span class="sxs-lookup"><span data-stu-id="61486-398">Sets the level of overlap filtering.</span></span> <span data-ttu-id="61486-399">使用重迭篩選時，會跨區塊和巨大區塊界限套用轉換係數。</span><span class="sxs-lookup"><span data-stu-id="61486-399">With overlap filtering, transform coefficients are applied across block and macroblock boundaries.</span></span> <span data-ttu-id="61486-400">這可以減少封鎖構件。</span><span class="sxs-lookup"><span data-stu-id="61486-400">This can reduce blocking artifacts.</span></span>



| <span data-ttu-id="61486-401">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-401">Data type</span></span> | <span data-ttu-id="61486-402">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-402">VARTYPE</span></span>     | <span data-ttu-id="61486-403">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-403">Range</span></span> | <span data-ttu-id="61486-404">預設</span><span class="sxs-lookup"><span data-stu-id="61486-404">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61486-405">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-405">**UCHAR**</span></span> | <span data-ttu-id="61486-406">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-406">**VT\_UI1**</span></span> | <span data-ttu-id="61486-407">0–4</span><span class="sxs-lookup"><span data-stu-id="61486-407">0–4</span></span>   | <span data-ttu-id="61486-408">1</span><span class="sxs-lookup"><span data-stu-id="61486-408">1</span></span>       |



 



| <span data-ttu-id="61486-409">值</span><span class="sxs-lookup"><span data-stu-id="61486-409">Value</span></span> | <span data-ttu-id="61486-410">描述</span><span class="sxs-lookup"><span data-stu-id="61486-410">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="61486-411">0</span><span class="sxs-lookup"><span data-stu-id="61486-411">0</span></span>     | <span data-ttu-id="61486-412">無重迭。</span><span class="sxs-lookup"><span data-stu-id="61486-412">No overlap.</span></span>                                   |
| <span data-ttu-id="61486-413">1</span><span class="sxs-lookup"><span data-stu-id="61486-413">1</span></span>     | <span data-ttu-id="61486-414">一個重迭層級，軟平並排。</span><span class="sxs-lookup"><span data-stu-id="61486-414">One level of overlap, soft tiling.</span></span> <span data-ttu-id="61486-415">(預設值。)</span><span class="sxs-lookup"><span data-stu-id="61486-415">(Default.)</span></span> |
| <span data-ttu-id="61486-416">2</span><span class="sxs-lookup"><span data-stu-id="61486-416">2</span></span>     | <span data-ttu-id="61486-417">兩個重迭層級，軟平並排。</span><span class="sxs-lookup"><span data-stu-id="61486-417">Two levels of overlap, soft tiling.</span></span>           |
| <span data-ttu-id="61486-418">3</span><span class="sxs-lookup"><span data-stu-id="61486-418">3</span></span>     | <span data-ttu-id="61486-419">一個重迭層級，硬平圖</span><span class="sxs-lookup"><span data-stu-id="61486-419">One level of overlap, hard tiling</span></span>             |
| <span data-ttu-id="61486-420">4</span><span class="sxs-lookup"><span data-stu-id="61486-420">4</span></span>     | <span data-ttu-id="61486-421">重迭的兩個層級，硬平圖。</span><span class="sxs-lookup"><span data-stu-id="61486-421">Two levels of overlap, hard tiling.</span></span>           |



 

<span data-ttu-id="61486-422">定義：</span><span class="sxs-lookup"><span data-stu-id="61486-422">Definitions:</span></span>

-   <span data-ttu-id="61486-423">一個重迭層級：會根據連續的區塊來修改4x4 區塊的編碼值。</span><span class="sxs-lookup"><span data-stu-id="61486-423">One level of overlap: The encoded values of 4x4 blocks are modified based on neighboring blocks.</span></span>
-   <span data-ttu-id="61486-424">重迭的兩個層級：套用第一個重迭層級。</span><span class="sxs-lookup"><span data-stu-id="61486-424">Two levels of overlap: The first level of overlap is applied.</span></span> <span data-ttu-id="61486-425">此外，會根據鄰近的巨大區塊修改16x16 巨大區塊的編碼值。</span><span class="sxs-lookup"><span data-stu-id="61486-425">In addition, the encoded values of 16x16 macroblocks are modified based on the neighboring macroblocks.</span></span>
-   <span data-ttu-id="61486-426">軟圖格：重迭篩選會套用到磚邊界。</span><span class="sxs-lookup"><span data-stu-id="61486-426">Soft tiling: Overlap filtering is applied across tile boundaries.</span></span>
-   <span data-ttu-id="61486-427">硬磚：重迭篩選不會套用到磚邊界。</span><span class="sxs-lookup"><span data-stu-id="61486-427">Hard tiling: Overlap filtering is not applied across tile boundaries.</span></span> <span data-ttu-id="61486-428">硬圖格可以沿著磚邊界引進一些視覺構件。</span><span class="sxs-lookup"><span data-stu-id="61486-428">Hard tiles can introduce some visual artifacts along tile boundaries.</span></span>

<span data-ttu-id="61486-429">如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="61486-429">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="progressivemode"></a><span data-ttu-id="61486-430">ProgressiveMode</span><span class="sxs-lookup"><span data-stu-id="61486-430">ProgressiveMode</span></span>

<span data-ttu-id="61486-431">啟用或停用漸進式編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-431">Enables or disables progressive encoding.</span></span>



| <span data-ttu-id="61486-432">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-432">Data type</span></span>         | <span data-ttu-id="61486-433">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-433">VARTYPE</span></span>      | <span data-ttu-id="61486-434">預設</span><span class="sxs-lookup"><span data-stu-id="61486-434">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61486-435">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-435">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-436">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-436">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-437">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-437">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="61486-438">值</span><span class="sxs-lookup"><span data-stu-id="61486-438">Value</span></span>              | <span data-ttu-id="61486-439">描述</span><span class="sxs-lookup"><span data-stu-id="61486-439">Description</span></span>                |
|--------------------|----------------------------|
| <span data-ttu-id="61486-440">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61486-440">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="61486-441">順序模式 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="61486-441">Sequential mode (default).</span></span> |
| <span data-ttu-id="61486-442">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-442">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="61486-443">漸進模式。</span><span class="sxs-lookup"><span data-stu-id="61486-443">Progressive mode.</span></span>          |



 

### <a name="quality"></a><span data-ttu-id="61486-444">品質</span><span class="sxs-lookup"><span data-stu-id="61486-444">Quality</span></span>

<span data-ttu-id="61486-445">設定壓縮品質。</span><span class="sxs-lookup"><span data-stu-id="61486-445">Sets the compression quality.</span></span>



| <span data-ttu-id="61486-446">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-446">Data type</span></span> | <span data-ttu-id="61486-447">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-447">VARTYPE</span></span>     | <span data-ttu-id="61486-448">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-448">Range</span></span> | <span data-ttu-id="61486-449">預設</span><span class="sxs-lookup"><span data-stu-id="61486-449">Default</span></span> |
|-----------|-------------|-------|---------|
| <span data-ttu-id="61486-450">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-450">**UCHAR**</span></span> | <span data-ttu-id="61486-451">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-451">**VT\_UI1**</span></span> | <span data-ttu-id="61486-452">1–255</span><span class="sxs-lookup"><span data-stu-id="61486-452">1–255</span></span> | <span data-ttu-id="61486-453">1</span><span class="sxs-lookup"><span data-stu-id="61486-453">1</span></span>       |



 

<span data-ttu-id="61486-454">值1表示無失真模式。</span><span class="sxs-lookup"><span data-stu-id="61486-454">The value 1 indicates lossless mode.</span></span> <span data-ttu-id="61486-455">增加值會產生較高的壓縮比例和較低的影像品質。</span><span class="sxs-lookup"><span data-stu-id="61486-455">Increasing values result in higher compression ratios and lower image quality.</span></span>

<span data-ttu-id="61486-456">如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="61486-456">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="streamonly"></a><span data-ttu-id="61486-457">StreamOnly</span><span class="sxs-lookup"><span data-stu-id="61486-457">StreamOnly</span></span>

<span data-ttu-id="61486-458">啟用或停用僅限資料流程模式。</span><span class="sxs-lookup"><span data-stu-id="61486-458">Enables or disables stream-only mode.</span></span>



| <span data-ttu-id="61486-459">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-459">Data type</span></span>         | <span data-ttu-id="61486-460">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-460">VARTYPE</span></span>      | <span data-ttu-id="61486-461">預設</span><span class="sxs-lookup"><span data-stu-id="61486-461">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61486-462">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-462">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-463">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-463">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-464">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-464">**VARIANT\_FALSE**</span></span> |



 



| <span data-ttu-id="61486-465">值</span><span class="sxs-lookup"><span data-stu-id="61486-465">Value</span></span>              | <span data-ttu-id="61486-466">描述</span><span class="sxs-lookup"><span data-stu-id="61486-466">Description</span></span>                                                            |
|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="61486-467">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="61486-467">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="61486-468">編碼器會輸出未經處理中繼資料的原始影像資料流程。</span><span class="sxs-lookup"><span data-stu-id="61486-468">The encoder outputs the raw image stream without metadata.</span></span>             |
| <span data-ttu-id="61486-469">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-469">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="61486-470">編碼器會輸出容器格式 (影像串流以及中繼資料) 。</span><span class="sxs-lookup"><span data-stu-id="61486-470">The encoder outputs the container format (image stream plus metadata).</span></span> |



 

### <a name="subsampling"></a><span data-ttu-id="61486-471">圖元</span><span class="sxs-lookup"><span data-stu-id="61486-471">Subsampling</span></span>

<span data-ttu-id="61486-472">設定色度的取樣。</span><span class="sxs-lookup"><span data-stu-id="61486-472">Sets the chroma subsampling.</span></span> <span data-ttu-id="61486-473">這個屬性只適用于 RGB 影像。</span><span class="sxs-lookup"><span data-stu-id="61486-473">This property applies only to RGB images.</span></span>



| <span data-ttu-id="61486-474">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-474">Data type</span></span> | <span data-ttu-id="61486-475">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-475">VARTYPE</span></span>     | <span data-ttu-id="61486-476">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-476">Range</span></span> | <span data-ttu-id="61486-477">預設</span><span class="sxs-lookup"><span data-stu-id="61486-477">Default</span></span>                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| <span data-ttu-id="61486-478">**UCHAR**</span><span class="sxs-lookup"><span data-stu-id="61486-478">**UCHAR**</span></span> | <span data-ttu-id="61486-479">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="61486-479">**VT\_UI1**</span></span> | <span data-ttu-id="61486-480">0–3</span><span class="sxs-lookup"><span data-stu-id="61486-480">0–3</span></span>   | <span data-ttu-id="61486-481">3如果 [ImageQuality](#imagequality) > 0.8;否則為1</span><span class="sxs-lookup"><span data-stu-id="61486-481">3 if [ImageQuality](#imagequality) > 0.8; otherwise 1</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61486-482">值</span><span class="sxs-lookup"><span data-stu-id="61486-482">Value</span></span></th>
<th><span data-ttu-id="61486-483">描述</span><span class="sxs-lookup"><span data-stu-id="61486-483">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61486-484">3</span><span class="sxs-lookup"><span data-stu-id="61486-484">3</span></span></td>
<td><span data-ttu-id="61486-485">4:4:4 編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-485">4:4:4 encoding.</span></span> <span data-ttu-id="61486-486">保留完整的色度解析度。</span><span class="sxs-lookup"><span data-stu-id="61486-486">Preserves full chroma resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61486-487">2</span><span class="sxs-lookup"><span data-stu-id="61486-487">2</span></span></td>
<td><span data-ttu-id="61486-488">4:2:2 編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-488">4:2:2 encoding.</span></span> <span data-ttu-id="61486-489">色度解析度是1/2 的亮度解析度。</span><span class="sxs-lookup"><span data-stu-id="61486-489">Chroma resolution is ½ of luminance resolution.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61486-490">1</span><span class="sxs-lookup"><span data-stu-id="61486-490">1</span></span></td>
<td><span data-ttu-id="61486-491">4:2:0 編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-491">4:2:0 encoding.</span></span> <span data-ttu-id="61486-492">色度解析度是1/4 的亮度解析度。</span><span class="sxs-lookup"><span data-stu-id="61486-492">Chroma resolution is ¼ of luminance resolution.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61486-493">0</span><span class="sxs-lookup"><span data-stu-id="61486-493">0</span></span></td>
<td><span data-ttu-id="61486-494">4:0:0 編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-494">4:0:0 encoding.</span></span> <span data-ttu-id="61486-495">捨棄所有的色度值，並只保留亮度。</span><span class="sxs-lookup"><span data-stu-id="61486-495">Discards all chroma values and preserves luminance only.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61486-496">不建議使用此模式，因為編解碼器會使用稍微修改的亮度定義來改善效能。</span><span class="sxs-lookup"><span data-stu-id="61486-496">This mode is not recommended, because the codec uses a slightly modified definition of luminance to improve performance.</span></span> <span data-ttu-id="61486-497">相反地，最好先將影像轉換成單色再進行編碼。</span><span class="sxs-lookup"><span data-stu-id="61486-497">Instead, it is better to convert the image to monochrome before encoding.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61486-498">4:2:2 和4:2:0 會保留亮度詳細資料，同時保有色彩詳細資料的費用。</span><span class="sxs-lookup"><span data-stu-id="61486-498">4:2:2 and 4:2:0 preserve luminance detail at the expense of color detail.</span></span>

<span data-ttu-id="61486-499">如果設定此屬性，也請將 [UseCodecOptions](#usecodecoptions) 設定為 **VARIANT \_ TRUE**。</span><span class="sxs-lookup"><span data-stu-id="61486-499">If you set this property, also set [UseCodecOptions](#usecodecoptions) to **VARIANT\_TRUE**.</span></span>

### <a name="usecodecoptions"></a><span data-ttu-id="61486-500">UseCodecOptions</span><span class="sxs-lookup"><span data-stu-id="61486-500">UseCodecOptions</span></span>

<span data-ttu-id="61486-501">指定是否使用 [ [品質](#image-quality-settings)]、[重 [迭](#overlap)] 和 [ [取樣](#subsampling) ] 屬性，而非 [一般 [ImageQuality](#imagequality) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="61486-501">Specifies whether to use the [Quality](#image-quality-settings), [Overlap](#overlap), and [Subsampling](#subsampling) properties instead of the generic [ImageQuality](#imagequality) property.</span></span>



| <span data-ttu-id="61486-502">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-502">Data type</span></span>         | <span data-ttu-id="61486-503">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-503">VARTYPE</span></span>      | <span data-ttu-id="61486-504">預設</span><span class="sxs-lookup"><span data-stu-id="61486-504">Default</span></span>            |
|-------------------|--------------|--------------------|
| <span data-ttu-id="61486-505">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-505">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="61486-506">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="61486-506">**VT\_BOOL**</span></span> | <span data-ttu-id="61486-507">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="61486-507">**VARIANT\_FALSE**</span></span> |



 

### <a name="verticaltileslices"></a><span data-ttu-id="61486-508">VerticalTileSlices</span><span class="sxs-lookup"><span data-stu-id="61486-508">VerticalTileSlices</span></span>

<span data-ttu-id="61486-509">設定水準磚的數目。</span><span class="sxs-lookup"><span data-stu-id="61486-509">Sets the number of horizontal tiles.</span></span>



| <span data-ttu-id="61486-510">資料類型</span><span class="sxs-lookup"><span data-stu-id="61486-510">Data type</span></span>  | <span data-ttu-id="61486-511">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="61486-511">VARTYPE</span></span>     | <span data-ttu-id="61486-512">範圍</span><span class="sxs-lookup"><span data-stu-id="61486-512">Range</span></span>  | <span data-ttu-id="61486-513">預設</span><span class="sxs-lookup"><span data-stu-id="61486-513">Default</span></span>                       |
|------------|-------------|--------|-------------------------------|
| <span data-ttu-id="61486-514">**USHORT**</span><span class="sxs-lookup"><span data-stu-id="61486-514">**USHORT**</span></span> | <span data-ttu-id="61486-515">**VT \_ UI2**</span><span class="sxs-lookup"><span data-stu-id="61486-515">**VT\_UI2**</span></span> | <span data-ttu-id="61486-516">0–4095</span><span class="sxs-lookup"><span data-stu-id="61486-516">0–4095</span></span> | <span data-ttu-id="61486-517"> (影像高度– 1)  >> 8</span><span class="sxs-lookup"><span data-stu-id="61486-517">(image height – 1) >> 8</span></span> |



 

<span data-ttu-id="61486-518">值是垂直細分的數目;也就是垂直磚的數目–1。</span><span class="sxs-lookup"><span data-stu-id="61486-518">The value is the number of vertical subdivisions; that is, the number of vertical tiles – 1.</span></span>

## <a name="supported-color-formats"></a><span data-ttu-id="61486-519">支援的色彩格式</span><span class="sxs-lookup"><span data-stu-id="61486-519">Supported Color Formats</span></span>

<span data-ttu-id="61486-520">如需這些格式的詳細資訊，請參閱 [原生像素格式](-wic-codec-native-pixel-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="61486-520">For more information about these formats, see [Native Pixel Formats](-wic-codec-native-pixel-formats.md).</span></span>

-   <span data-ttu-id="61486-521">**整數 RGB 格式**</span><span class="sxs-lookup"><span data-stu-id="61486-521">**Integer RGB formats**</span></span>
    -   <span data-ttu-id="61486-522">GUID \_ WICPixelFormat24bppRGB</span><span class="sxs-lookup"><span data-stu-id="61486-522">GUID\_WICPixelFormat24bppRGB</span></span>
    -   <span data-ttu-id="61486-523">GUID \_ WICPixelFormat24bppBGR</span><span class="sxs-lookup"><span data-stu-id="61486-523">GUID\_WICPixelFormat24bppBGR</span></span>
    -   <span data-ttu-id="61486-524">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="61486-524">GUID\_WICPixelFormat32bppBGR</span></span>
    -   <span data-ttu-id="61486-525">GUID \_ WICPixelFormat48bppRGB</span><span class="sxs-lookup"><span data-stu-id="61486-525">GUID\_WICPixelFormat48bppRGB</span></span>
    -   <span data-ttu-id="61486-526">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="61486-526">GUID\_WICPixelFormat32bppBGRA</span></span>
    -   <span data-ttu-id="61486-527">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="61486-527">GUID\_WICPixelFormat64bppRGBA</span></span>
    -   <span data-ttu-id="61486-528">GUID \_ WICPixelFormat32bppPBGRA</span><span class="sxs-lookup"><span data-stu-id="61486-528">GUID\_WICPixelFormat32bppPBGRA</span></span>
    -   <span data-ttu-id="61486-529">GUID \_ WICPixelFormat64bppPRGBA</span><span class="sxs-lookup"><span data-stu-id="61486-529">GUID\_WICPixelFormat64bppPRGBA</span></span>
-   <span data-ttu-id="61486-530">**固定點 RGB 格式**</span><span class="sxs-lookup"><span data-stu-id="61486-530">**Fixed-point RGB formats**</span></span>
    -   <span data-ttu-id="61486-531">GUID \_ WICPixelFormat48bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-531">GUID\_WICPixelFormat48bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61486-532">GUID \_ WICPixelFormat64bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-532">GUID\_WICPixelFormat64bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61486-533">GUID \_ WICPixelFormat96bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-533">GUID\_WICPixelFormat96bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61486-534">GUID \_ WICPixelFormat128bppRGBFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-534">GUID\_WICPixelFormat128bppRGBFixedPoint</span></span>
    -   <span data-ttu-id="61486-535">GUID \_ WICPixelFormat128bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-535">GUID\_WICPixelFormat128bppRGBAFixedPoint</span></span>
-   <span data-ttu-id="61486-536">**浮點數 RGB 格式**</span><span class="sxs-lookup"><span data-stu-id="61486-536">**Floating-point RGB formats**</span></span>
    -   <span data-ttu-id="61486-537">GUID \_ WICPixelFormat48bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="61486-537">GUID\_WICPixelFormat48bppRGBHalf</span></span>
    -   <span data-ttu-id="61486-538">GUID \_ WICPixelFormat64bppRGBHalf</span><span class="sxs-lookup"><span data-stu-id="61486-538">GUID\_WICPixelFormat64bppRGBHalf</span></span>
    -   <span data-ttu-id="61486-539">GUID \_ WICPixelFormat128bppRGBFloat</span><span class="sxs-lookup"><span data-stu-id="61486-539">GUID\_WICPixelFormat128bppRGBFloat</span></span>
    -   <span data-ttu-id="61486-540">GUID \_ WICPixelFormat64bppRGBAFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-540">GUID\_WICPixelFormat64bppRGBAFixedPoint</span></span>
    -   <span data-ttu-id="61486-541">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="61486-541">GUID\_WICPixelFormat64bppRGBAHalf</span></span>
    -   <span data-ttu-id="61486-542">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="61486-542">GUID\_WICPixelFormat128bppRGBAFloat</span></span>
    -   <span data-ttu-id="61486-543">GUID \_ WICPixelFormat128bppPRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="61486-543">GUID\_WICPixelFormat128bppPRGBAFloat</span></span>
-   <span data-ttu-id="61486-544">**灰階格式**</span><span class="sxs-lookup"><span data-stu-id="61486-544">**Grayscale formats**</span></span>
    -   <span data-ttu-id="61486-545">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="61486-545">GUID\_WICPixelFormat8bppGray</span></span>
    -   <span data-ttu-id="61486-546">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="61486-546">GUID\_WICPixelFormat16bppGray</span></span>
    -   <span data-ttu-id="61486-547">GUID \_ WICPixelFormat16bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-547">GUID\_WICPixelFormat16bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="61486-548">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="61486-548">GUID\_WICPixelFormat16bppGrayHalf</span></span>
    -   <span data-ttu-id="61486-549">GUID \_ WICPixelFormat32bppGrayFixedPoint</span><span class="sxs-lookup"><span data-stu-id="61486-549">GUID\_WICPixelFormat32bppGrayFixedPoint</span></span>
    -   <span data-ttu-id="61486-550">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="61486-550">GUID\_WICPixelFormat32bppGrayFloat</span></span>
-   <span data-ttu-id="61486-551">**壓縮格式**</span><span class="sxs-lookup"><span data-stu-id="61486-551">**Packed formats**</span></span>
    -   <span data-ttu-id="61486-552">GUID \_ WICPixelFormat16bppBGR555</span><span class="sxs-lookup"><span data-stu-id="61486-552">GUID\_WICPixelFormat16bppBGR555</span></span>
    -   <span data-ttu-id="61486-553">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="61486-553">GUID\_WICPixelFormat16bppBGR565</span></span>
    -   <span data-ttu-id="61486-554">GUID \_ WICPixelFormat32bppBGR101010</span><span class="sxs-lookup"><span data-stu-id="61486-554">GUID\_WICPixelFormat32bppBGR101010</span></span>
    -   <span data-ttu-id="61486-555">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="61486-555">GUID\_WICPixelFormat32bppRGBE</span></span>
-   <span data-ttu-id="61486-556">**CMYK 格式**</span><span class="sxs-lookup"><span data-stu-id="61486-556">**CMYK formats**</span></span>
    -   <span data-ttu-id="61486-557">GUID \_ WICPixelFormat40bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-557">GUID\_WICPixelFormat40bppCMYKAlpha</span></span>
    -   <span data-ttu-id="61486-558">GUID \_ WICPixelFormat64bppCMYK</span><span class="sxs-lookup"><span data-stu-id="61486-558">GUID\_WICPixelFormat64bppCMYK</span></span>
    -   <span data-ttu-id="61486-559">GUID \_ WICPixelFormat80bppCMYKAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-559">GUID\_WICPixelFormat80bppCMYKAlpha</span></span>
-   <span data-ttu-id="61486-560">**N 通道格式**</span><span class="sxs-lookup"><span data-stu-id="61486-560">**N-channel formats**</span></span>
    -   <span data-ttu-id="61486-561">GUID \_ WICPixelFormat32bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="61486-561">GUID\_WICPixelFormat32bpp4Channels</span></span>
    -   <span data-ttu-id="61486-562">GUID \_ WICPixelFormat40bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="61486-562">GUID\_WICPixelFormat40bpp5Channels</span></span>
    -   <span data-ttu-id="61486-563">GUID \_ WICPixelFormat48bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="61486-563">GUID\_WICPixelFormat48bpp6Channels</span></span>
    -   <span data-ttu-id="61486-564">GUID \_ WICPixelFormat56bpp7Channels</span><span class="sxs-lookup"><span data-stu-id="61486-564">GUID\_WICPixelFormat56bpp7Channels</span></span>
    -   <span data-ttu-id="61486-565">GUID \_ WICPixelFormat64bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="61486-565">GUID\_WICPixelFormat64bpp8Channels</span></span>
    -   <span data-ttu-id="61486-566">GUID \_ WICPixelFormat32bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-566">GUID\_WICPixelFormat32bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-567">GUID \_ WICPixelFormat40bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-567">GUID\_WICPixelFormat40bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-568">GUID \_ WICPixelFormat48bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-568">GUID\_WICPixelFormat48bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-569">GUID \_ WICPixelFormat56bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-569">GUID\_WICPixelFormat56bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-570">GUID \_ WICPixelFormat64bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-570">GUID\_WICPixelFormat64bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-571">GUID \_ WICPixelFormat72bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-571">GUID\_WICPixelFormat72bpp8ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-572">GUID \_ WICPixelFormat48bpp3Channels</span><span class="sxs-lookup"><span data-stu-id="61486-572">GUID\_WICPixelFormat48bpp3Channels</span></span>
    -   <span data-ttu-id="61486-573">GUID \_ WICPixelFormat64bpp4Channels</span><span class="sxs-lookup"><span data-stu-id="61486-573">GUID\_WICPixelFormat64bpp4Channels</span></span>
    -   <span data-ttu-id="61486-574">GUID \_ WICPixelFormat80bpp5Channels</span><span class="sxs-lookup"><span data-stu-id="61486-574">GUID\_WICPixelFormat80bpp5Channels</span></span>
    -   <span data-ttu-id="61486-575">GUID \_ WICPixelFormat96bpp6Channels</span><span class="sxs-lookup"><span data-stu-id="61486-575">GUID\_WICPixelFormat96bpp6Channels</span></span>
    -   <span data-ttu-id="61486-576">GUID \_ WICPixelFormat128bpp8Channels</span><span class="sxs-lookup"><span data-stu-id="61486-576">GUID\_WICPixelFormat128bpp8Channels</span></span>
    -   <span data-ttu-id="61486-577">GUID \_ WICPixelFormat64bpp3ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-577">GUID\_WICPixelFormat64bpp3ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-578">GUID \_ WICPixelFormat80bpp4ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-578">GUID\_WICPixelFormat80bpp4ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-579">GUID \_ WICPixelFormat96bpp5ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-579">GUID\_WICPixelFormat96bpp5ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-580">GUID \_ WICPixelFormat112bpp6ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-580">GUID\_WICPixelFormat112bpp6ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-581">GUID \_ WICPixelFormat128bpp7ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-581">GUID\_WICPixelFormat128bpp7ChannelsAlpha</span></span>
    -   <span data-ttu-id="61486-582">GUID \_ WICPixelFormat144bpp8ChannelsAlpha</span><span class="sxs-lookup"><span data-stu-id="61486-582">GUID\_WICPixelFormat144bpp8ChannelsAlpha</span></span>

 

 
