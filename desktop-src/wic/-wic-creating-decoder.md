---
description: 本主題介紹點陣圖解碼（核心 Windows 影像處理元件 (WIC) 編解碼器元件，用來從資料流程解碼影像檔案。
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: 解碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320924"
---
# <a name="decoding-overview"></a><span data-ttu-id="53403-103">解碼總覽</span><span class="sxs-lookup"><span data-stu-id="53403-103">Decoding Overview</span></span>

<span data-ttu-id="53403-104">本主題介紹點陣圖解碼（核心 Windows 影像處理元件 (WIC) 編解碼器元件，用來從資料流程解碼影像檔案。</span><span class="sxs-lookup"><span data-stu-id="53403-104">The topic introduces the bitmap decoder, a core Windows Imaging Component (WIC) codec component used to decode image files from a stream.</span></span>

<span data-ttu-id="53403-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="53403-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="53403-106">簡介</span><span class="sxs-lookup"><span data-stu-id="53403-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="53403-107">原生點陣圖解碼器</span><span class="sxs-lookup"><span data-stu-id="53403-107">Native Bitmap Decoders</span></span>](#native-bitmap-decoders)
-   [<span data-ttu-id="53403-108">建立點陣圖解碼器</span><span class="sxs-lookup"><span data-stu-id="53403-108">Creating a Bitmap Decoder</span></span>](#creating-a-bitmap-decoder)
-   [<span data-ttu-id="53403-109">解碼器擴充性</span><span class="sxs-lookup"><span data-stu-id="53403-109">Decoder Extensibility</span></span>](#decoder-extensibility)
-   [<span data-ttu-id="53403-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="53403-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="53403-111">簡介</span><span class="sxs-lookup"><span data-stu-id="53403-111">Introduction</span></span>

<span data-ttu-id="53403-112">您可以將點陣圖解碼器視為數位影像的外部容器，並提供全域屬性和影像框架的存取權。</span><span class="sxs-lookup"><span data-stu-id="53403-112">Bitmap decoders can be viewed as the outer container of a digital image and provides access to global properties and image frames.</span></span> <span data-ttu-id="53403-113">某些影像格式支援全域縮圖、預覽、色彩內容或中繼資料，而有些則只在框架層級提供這些屬性。</span><span class="sxs-lookup"><span data-stu-id="53403-113">Some image formats support global thumbnails, previews, color contexts, or metadata, while others provide these properties only at the frame level.</span></span> <span data-ttu-id="53403-114">不過請注意，許多標準影像格式都不支援這些全域屬性。</span><span class="sxs-lookup"><span data-stu-id="53403-114">Note, however, many of the standard image formats do not support these global properties.</span></span> <span data-ttu-id="53403-115">因此，WIC 提供的許多原生編解碼器，都不支援這些全域屬性的大部分。</span><span class="sxs-lookup"><span data-stu-id="53403-115">As such, many of the native codec implementations provided by WIC do not support the majority of these global properties.</span></span> <span data-ttu-id="53403-116">如需全域屬性支援的相關資訊，請參閱本主題的「原生點陣圖解碼器」一節中的表格。</span><span class="sxs-lookup"><span data-stu-id="53403-116">See the table in the Native Bitmap Decoders section of this topic for information about global property support.</span></span>

<span data-ttu-id="53403-117">在 WIC 中，點陣圖解碼器會以 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面表示，並可讓您存取點陣圖的這些全域屬性，更重要的是它所包含的框架。</span><span class="sxs-lookup"><span data-stu-id="53403-117">In WIC, bitmap decoders are represented by the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and provides access to these global properties of the bitmap and, more importantly, the frames it contains.</span></span> <span data-ttu-id="53403-118">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)介面代表個別的點陣圖框架，在 [點陣圖來源總覽](-wic-bitmapsources.md)中會詳細討論。</span><span class="sxs-lookup"><span data-stu-id="53403-118">The [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface represents an individual bitmap frame and is discussed in detail in the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="native-bitmap-decoders"></a><span data-ttu-id="53403-119">原生點陣圖解碼器</span><span class="sxs-lookup"><span data-stu-id="53403-119">Native Bitmap Decoders</span></span>

<span data-ttu-id="53403-120">WIC 針對標準的 web 影像格式和高動態範圍的 HD 相片格式，提供 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面的數個原生實作為。</span><span class="sxs-lookup"><span data-stu-id="53403-120">WIC provides several native implementations of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface for the standard web image formats and the high dynamic range HD Photo format.</span></span> <span data-ttu-id="53403-121">下表列出可用的原生解碼器、類別識別碼名稱，以及全域屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="53403-121">The following table lists the available native decoders, class identifier name, and support for global properties.</span></span> <span data-ttu-id="53403-122">雖然功能可能不支援全域層級的縮圖等屬性，但影像格式可能會在個別的框架層級支援這類屬性。</span><span class="sxs-lookup"><span data-stu-id="53403-122">Though a feature may not support a property such as thumbnails at the global level, the image format may support such properties at the individual frame level.</span></span>



| <span data-ttu-id="53403-123">映像格式</span><span class="sxs-lookup"><span data-stu-id="53403-123">Image Format</span></span> | <span data-ttu-id="53403-124">CLSID 名稱</span><span class="sxs-lookup"><span data-stu-id="53403-124">CLSID Name</span></span>            | <span data-ttu-id="53403-125">縮圖</span><span class="sxs-lookup"><span data-stu-id="53403-125">Thumbnails</span></span> | <span data-ttu-id="53403-126">預覽</span><span class="sxs-lookup"><span data-stu-id="53403-126">Previews</span></span> | <span data-ttu-id="53403-127">色彩內容</span><span class="sxs-lookup"><span data-stu-id="53403-127">Color Contexts</span></span> | <span data-ttu-id="53403-128">中繼資料</span><span class="sxs-lookup"><span data-stu-id="53403-128">Metadata</span></span> |
|--------------|-----------------------|------------|----------|----------------|----------|
| <span data-ttu-id="53403-129">BMP</span><span class="sxs-lookup"><span data-stu-id="53403-129">BMP</span></span>          | <span data-ttu-id="53403-130">CLSID \_ WICBmpDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-130">CLSID\_WICBmpDecoder</span></span>  | <span data-ttu-id="53403-131">否</span><span class="sxs-lookup"><span data-stu-id="53403-131">No</span></span>         | <span data-ttu-id="53403-132">否</span><span class="sxs-lookup"><span data-stu-id="53403-132">No</span></span>       | <span data-ttu-id="53403-133">否</span><span class="sxs-lookup"><span data-stu-id="53403-133">No</span></span>             | <span data-ttu-id="53403-134">否</span><span class="sxs-lookup"><span data-stu-id="53403-134">No</span></span>       |
| <span data-ttu-id="53403-135">GIF</span><span class="sxs-lookup"><span data-stu-id="53403-135">GIF</span></span>          | <span data-ttu-id="53403-136">CLSID \_ WICGifDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-136">CLSID\_WICGifDecoder</span></span>  | <span data-ttu-id="53403-137">否</span><span class="sxs-lookup"><span data-stu-id="53403-137">No</span></span>         | <span data-ttu-id="53403-138">否</span><span class="sxs-lookup"><span data-stu-id="53403-138">No</span></span>       | <span data-ttu-id="53403-139">否</span><span class="sxs-lookup"><span data-stu-id="53403-139">No</span></span>             | <span data-ttu-id="53403-140">是</span><span class="sxs-lookup"><span data-stu-id="53403-140">Yes</span></span>      |
| <span data-ttu-id="53403-141">ICO</span><span class="sxs-lookup"><span data-stu-id="53403-141">ICO</span></span>          | <span data-ttu-id="53403-142">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-142">CLSID\_WICIcoDecoder</span></span>  | <span data-ttu-id="53403-143">否</span><span class="sxs-lookup"><span data-stu-id="53403-143">No</span></span>         | <span data-ttu-id="53403-144">否</span><span class="sxs-lookup"><span data-stu-id="53403-144">No</span></span>       | <span data-ttu-id="53403-145">否</span><span class="sxs-lookup"><span data-stu-id="53403-145">No</span></span>             | <span data-ttu-id="53403-146">否</span><span class="sxs-lookup"><span data-stu-id="53403-146">No</span></span>       |
| <span data-ttu-id="53403-147">JPEG</span><span class="sxs-lookup"><span data-stu-id="53403-147">JPEG</span></span>         | <span data-ttu-id="53403-148">CLSID \_ WICJpegDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-148">CLSID\_WICJpegDecoder</span></span> | <span data-ttu-id="53403-149">否</span><span class="sxs-lookup"><span data-stu-id="53403-149">No</span></span>         | <span data-ttu-id="53403-150">否</span><span class="sxs-lookup"><span data-stu-id="53403-150">No</span></span>       | <span data-ttu-id="53403-151">否</span><span class="sxs-lookup"><span data-stu-id="53403-151">No</span></span>             | <span data-ttu-id="53403-152">否</span><span class="sxs-lookup"><span data-stu-id="53403-152">No</span></span>       |
| <span data-ttu-id="53403-153">PNG</span><span class="sxs-lookup"><span data-stu-id="53403-153">PNG</span></span>          | <span data-ttu-id="53403-154">CLSID \_ WICPngDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-154">CLSID\_WICPngDecoder</span></span>  | <span data-ttu-id="53403-155">否</span><span class="sxs-lookup"><span data-stu-id="53403-155">No</span></span>         | <span data-ttu-id="53403-156">否</span><span class="sxs-lookup"><span data-stu-id="53403-156">No</span></span>       | <span data-ttu-id="53403-157">否</span><span class="sxs-lookup"><span data-stu-id="53403-157">No</span></span>             | <span data-ttu-id="53403-158">否</span><span class="sxs-lookup"><span data-stu-id="53403-158">No</span></span>       |
| <span data-ttu-id="53403-159">TIFF</span><span class="sxs-lookup"><span data-stu-id="53403-159">TIFF</span></span>         | <span data-ttu-id="53403-160">CLSID \_ WICTiffDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-160">CLSID\_WICTiffDecoder</span></span> | <span data-ttu-id="53403-161">否</span><span class="sxs-lookup"><span data-stu-id="53403-161">No</span></span>         | <span data-ttu-id="53403-162">否</span><span class="sxs-lookup"><span data-stu-id="53403-162">No</span></span>       | <span data-ttu-id="53403-163">否</span><span class="sxs-lookup"><span data-stu-id="53403-163">No</span></span>             | <span data-ttu-id="53403-164">否</span><span class="sxs-lookup"><span data-stu-id="53403-164">No</span></span>       |
| <span data-ttu-id="53403-165">HD 相片</span><span class="sxs-lookup"><span data-stu-id="53403-165">HD Photo</span></span>     | <span data-ttu-id="53403-166">CLSID \_ WICWmpDecoder</span><span class="sxs-lookup"><span data-stu-id="53403-166">CLSID\_WICWmpDecoder</span></span>  | <span data-ttu-id="53403-167">否</span><span class="sxs-lookup"><span data-stu-id="53403-167">No</span></span>         | <span data-ttu-id="53403-168">是</span><span class="sxs-lookup"><span data-stu-id="53403-168">Yes</span></span>      | <span data-ttu-id="53403-169">否</span><span class="sxs-lookup"><span data-stu-id="53403-169">No</span></span>             | <span data-ttu-id="53403-170">否</span><span class="sxs-lookup"><span data-stu-id="53403-170">No</span></span>       |



 

## <a name="creating-a-bitmap-decoder"></a><span data-ttu-id="53403-171">建立點陣圖解碼器</span><span class="sxs-lookup"><span data-stu-id="53403-171">Creating a Bitmap Decoder</span></span>

<span data-ttu-id="53403-172">若要使用 WIC 解碼影像，您必須先針對目標影像格式建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 的實例。</span><span class="sxs-lookup"><span data-stu-id="53403-172">To decode an image using WIC, you first need to create an instance of the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) for the targeted image format.</span></span> <span data-ttu-id="53403-173">如果支援，則可讓您存取全域屬性和中繼資料，以及影像框架。</span><span class="sxs-lookup"><span data-stu-id="53403-173">The decoder instance enables you to access the global properties and metadata, if supported, as well as the image frames.</span></span> <span data-ttu-id="53403-174">WIC 影像處理 factory [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)提供數種建立點陣圖解碼器的方法。</span><span class="sxs-lookup"><span data-stu-id="53403-174">The WIC imaging factory, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), provides several methods for creating bitmap decoders.</span></span> <span data-ttu-id="53403-175">提供下列 factory 方法來建立點陣圖解碼器。</span><span class="sxs-lookup"><span data-stu-id="53403-175">The following factory methods are provided to create bitmap decoders.</span></span>

-   [<span data-ttu-id="53403-176">**CreateDecoder**</span><span class="sxs-lookup"><span data-stu-id="53403-176">**CreateDecoder**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [<span data-ttu-id="53403-177">**CreateDecoderFromFileHandle**</span><span class="sxs-lookup"><span data-stu-id="53403-177">**CreateDecoderFromFileHandle**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [<span data-ttu-id="53403-178">**CreateDecoderFromFilename**</span><span class="sxs-lookup"><span data-stu-id="53403-178">**CreateDecoderFromFilename**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [<span data-ttu-id="53403-179">**CreateDecoderFromStream**</span><span class="sxs-lookup"><span data-stu-id="53403-179">**CreateDecoderFromStream**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

<span data-ttu-id="53403-180">下列程式碼示範如何使用映射檔案名建立點陣圖解碼器，以及抓取影像的第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="53403-180">The following code demonstrates the how to create a bitmap decoder using an image filename and retrieve the first frame of the image.</span></span>


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a><span data-ttu-id="53403-181">解碼器擴充性</span><span class="sxs-lookup"><span data-stu-id="53403-181">Decoder Extensibility</span></span>

<span data-ttu-id="53403-182">WIC 的其中一個核心功能是擴充性架構，可讓編解碼器開發人員開發自己的映射編解碼器，並取得與映射編解碼器原生執行相同的平臺支援。</span><span class="sxs-lookup"><span data-stu-id="53403-182">One of the core features of WIC is an extensibility framework that enables codec developers to develop their own image codecs and get the same platform support as the native implementations of image codecs.</span></span> <span data-ttu-id="53403-183">不論影像格式為何，都使用單一、一致的介面集來處理所有圖像。</span><span class="sxs-lookup"><span data-stu-id="53403-183">A single, consistent set of interfaces is used for all image processing, regardless of image format.</span></span> <span data-ttu-id="53403-184">任何使用 WIC 的應用程式都會在安裝編解碼器時立即取得新映射格式的自動支援。</span><span class="sxs-lookup"><span data-stu-id="53403-184">Any application using WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="53403-185">如需有關編解碼器開發的詳細資訊，請參閱 [元件開發](-wic-component-development.md)中的主題。</span><span class="sxs-lookup"><span data-stu-id="53403-185">For more information on codec development, see the topics in [Component Development](-wic-component-development.md).</span></span> <span data-ttu-id="53403-186">如需有關如何開發的詳細資訊，請參閱 [執行 WIC-Enabled 的解碼器](-wic-implementingwicdecoder.md)。</span><span class="sxs-lookup"><span data-stu-id="53403-186">For more information on decoder development, see [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53403-187">相關主題</span><span class="sxs-lookup"><span data-stu-id="53403-187">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="53403-188">**概念**</span><span class="sxs-lookup"><span data-stu-id="53403-188">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53403-189">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="53403-189">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="53403-190">編碼總覽</span><span class="sxs-lookup"><span data-stu-id="53403-190">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

[<span data-ttu-id="53403-191">元件開發</span><span class="sxs-lookup"><span data-stu-id="53403-191">Component Development</span></span>](-wic-component-development.md)
</dt> </dl>

 

 



