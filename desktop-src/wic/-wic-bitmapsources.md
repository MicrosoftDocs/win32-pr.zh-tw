---
description: 本主題介紹點陣圖來源（核心 Windows 影像處理元件 (WIC) 元件，代表影像的點陣圖圖元。
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: 點陣圖來源總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468976"
---
# <a name="bitmap-sources-overview"></a><span data-ttu-id="67e20-103">點陣圖來源總覽</span><span class="sxs-lookup"><span data-stu-id="67e20-103">Bitmap Sources Overview</span></span>

<span data-ttu-id="67e20-104">本主題介紹點陣圖來源（核心 Windows 影像處理元件 (WIC) 元件，代表影像的點陣圖圖元。</span><span class="sxs-lookup"><span data-stu-id="67e20-104">This topic introduces bitmap sources, a core Windows Imaging Component (WIC) component that represents the bitmap pixels of an image.</span></span>

<span data-ttu-id="67e20-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="67e20-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="67e20-106">點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-106">Bitmap Sources</span></span>](#bitmap-sources-overview)
-   [<span data-ttu-id="67e20-107">點陣圖框架</span><span class="sxs-lookup"><span data-stu-id="67e20-107">Bitmap Frames</span></span>](#bitmap-frames)
-   [<span data-ttu-id="67e20-108">點陣圖</span><span class="sxs-lookup"><span data-stu-id="67e20-108">Bitmaps</span></span>](#bitmap-sources-overview)
-   [<span data-ttu-id="67e20-109">轉換點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-109">Transform Bitmap Sources</span></span>](#transform-bitmap-sources)
-   [<span data-ttu-id="67e20-110">像素格式和色彩內容轉換器</span><span class="sxs-lookup"><span data-stu-id="67e20-110">Pixel Format and Color Context Converters</span></span>](#pixel-format-and-color-context-converters)
-   [<span data-ttu-id="67e20-111">繪製點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-111">Drawing Bitmap Sources</span></span>](#drawing-bitmap-sources)
-   [<span data-ttu-id="67e20-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="67e20-112">Related topics</span></span>](#related-topics)

## <a name="bitmap-sources"></a><span data-ttu-id="67e20-113">點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-113">Bitmap Sources</span></span>

<span data-ttu-id="67e20-114">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)元件是 WIC 的基本組建區塊，代表一組圖元。</span><span class="sxs-lookup"><span data-stu-id="67e20-114">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) component is the basic building block of WIC and represents a single set of pixels.</span></span> <span data-ttu-id="67e20-115">點陣圖來源可以是 multiframe 影像的個別框架，也可以是在點陣圖來源上執行轉換的結果。</span><span class="sxs-lookup"><span data-stu-id="67e20-115">A bitmap source can be an individual frame of a multiframe image, or it can be the result of a transform performed on a bitmap source.</span></span> <span data-ttu-id="67e20-116">**IWICBitmapSource** 介面是許多主要 WIC 介面的基底，例如「解碼器框架 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)和轉換點陣圖來源，例如 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)。</span><span class="sxs-lookup"><span data-stu-id="67e20-116">The **IWICBitmapSource** interface is the base of many of the primary WIC interfaces such as the decoder frame [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and transform bitmap sources such as the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

<span data-ttu-id="67e20-117">下表描述 WIC 提供的不同點陣圖來源元件。</span><span class="sxs-lookup"><span data-stu-id="67e20-117">The following table describes the different bitmap source components provided by WIC.</span></span>



| <span data-ttu-id="67e20-118">點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-118">Bitmap Sources</span></span>                                                    | <span data-ttu-id="67e20-119">Description</span><span class="sxs-lookup"><span data-stu-id="67e20-119">Description</span></span>                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="67e20-120">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="67e20-120">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | <span data-ttu-id="67e20-121">表示解碼器圖像框架。</span><span class="sxs-lookup"><span data-stu-id="67e20-121">Represents a decoder image frame.</span></span>                                    |
| [<span data-ttu-id="67e20-122">**IWICBitmap**</span><span class="sxs-lookup"><span data-stu-id="67e20-122">**IWICBitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | <span data-ttu-id="67e20-123">提供點陣圖來源的可寫性和記憶體中標記法。</span><span class="sxs-lookup"><span data-stu-id="67e20-123">Provides writability and in-memory representation to bitmap sources.</span></span> |
| [<span data-ttu-id="67e20-124">**IWICBitmapClipper**</span><span class="sxs-lookup"><span data-stu-id="67e20-124">**IWICBitmapClipper**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | <span data-ttu-id="67e20-125">將點陣圖來源裁剪至所需的矩形。</span><span class="sxs-lookup"><span data-stu-id="67e20-125">Clips a bitmap source to a desired rectangle.</span></span>                        |
| [<span data-ttu-id="67e20-126">**IWICBitmapFlipRotator**</span><span class="sxs-lookup"><span data-stu-id="67e20-126">**IWICBitmapFlipRotator**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | <span data-ttu-id="67e20-127">翻轉和/或將點陣圖來源旋轉為所需的方向。</span><span class="sxs-lookup"><span data-stu-id="67e20-127">Flips and/or rotates a bitmap source to a desired orientation.</span></span>       |
| [<span data-ttu-id="67e20-128">**IWICBitmapScaler**</span><span class="sxs-lookup"><span data-stu-id="67e20-128">**IWICBitmapScaler**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | <span data-ttu-id="67e20-129">將點陣圖來源調整為所需的大小。</span><span class="sxs-lookup"><span data-stu-id="67e20-129">Scales a bitmap source to a desired size.</span></span>                            |
| [<span data-ttu-id="67e20-130">**IWICColorTransform**</span><span class="sxs-lookup"><span data-stu-id="67e20-130">**IWICColorTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | <span data-ttu-id="67e20-131">轉換點陣圖來源的色彩內容。</span><span class="sxs-lookup"><span data-stu-id="67e20-131">Transforms the color context of a bitmap source.</span></span>                     |
| [<span data-ttu-id="67e20-132">**IWICFormatConverter**</span><span class="sxs-lookup"><span data-stu-id="67e20-132">**IWICFormatConverter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | <span data-ttu-id="67e20-133">轉換點陣圖來源的像素格式。</span><span class="sxs-lookup"><span data-stu-id="67e20-133">Converts the pixel format of a bitmap source.</span></span>                        |



 

## <a name="bitmap-frames"></a><span data-ttu-id="67e20-134">點陣圖框架</span><span class="sxs-lookup"><span data-stu-id="67e20-134">Bitmap Frames</span></span>

<span data-ttu-id="67e20-135">最常見的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 是 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)。</span><span class="sxs-lookup"><span data-stu-id="67e20-135">The most common [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="67e20-136">這個介面是用來存取影像格式的實際點陣圖資料。</span><span class="sxs-lookup"><span data-stu-id="67e20-136">This interface is used to access the actual bitmap data of an image format.</span></span> <span data-ttu-id="67e20-137">許多影像格式只支援單一點陣圖框架，而其他格式（例如 GIF 和 TIFF）支援每個影像有多個畫面格。</span><span class="sxs-lookup"><span data-stu-id="67e20-137">Many image formats only support a single bitmap frame, while other formats such as GIF and TIFF support multiple frames per image.</span></span>

<span data-ttu-id="67e20-138">如需從影像取得點陣圖框架的範例，請參閱 [如何取出影像](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) 主題的畫面格。</span><span class="sxs-lookup"><span data-stu-id="67e20-138">For an example on obtaining bitmap frames from an image, see the [How to Retrieve the Frames of an Image](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) topic.</span></span>

## <a name="bitmaps"></a><span data-ttu-id="67e20-139">點陣圖</span><span class="sxs-lookup"><span data-stu-id="67e20-139">Bitmaps</span></span>

<span data-ttu-id="67e20-140">[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)會將可寫性和靜態記憶體內部的概念加入點陣圖來源中。</span><span class="sxs-lookup"><span data-stu-id="67e20-140">An [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) adds the concepts of writability and static in-memory to bitmap sources.</span></span> <span data-ttu-id="67e20-141">WIC 點陣圖可讓使用者直接存取點陣圖來源的圖元。</span><span class="sxs-lookup"><span data-stu-id="67e20-141">WIC bitmaps enables users to directly access the pixels of a bitmap source.</span></span> <span data-ttu-id="67e20-142">這種直接存取是由 [**鎖定**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) 方法提供，而且支援點陣圖圖元的任何讀取和/或寫入存取組合。</span><span class="sxs-lookup"><span data-stu-id="67e20-142">This direct access is provided by the [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) method and supports any combination of read and/or write access to the bitmap pixels.</span></span> <span data-ttu-id="67e20-143">**Lock** 方法會鎖定指定的點陣圖矩形，並提供 [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) 物件來存取圖元。</span><span class="sxs-lookup"><span data-stu-id="67e20-143">**Lock** method locks the specified bitmap rectangle and provides an [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object to access the pixels.</span></span>

<span data-ttu-id="67e20-144">如需使用 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) 和 [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) 物件的範例，請參閱 [如何修改點陣圖來源的圖元](-wic-bitmapsources-howto-modifypixels.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="67e20-144">For an example using [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) and [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) objects, see the [How to Modify the Pixels of a Bitmap Source](-wic-bitmapsources-howto-modifypixels.md) topic.</span></span>

## <a name="transform-bitmap-sources"></a><span data-ttu-id="67e20-145">轉換點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-145">Transform Bitmap Sources</span></span>

<span data-ttu-id="67e20-146">WIC 提供數個可轉換圖元資料的 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 介面。</span><span class="sxs-lookup"><span data-stu-id="67e20-146">WIC provides several [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interfaces that transform the pixel data.</span></span> <span data-ttu-id="67e20-147">具體而言，WIC 會提供點陣圖來源轉換來調整、裁剪、旋轉和翻轉圖元資料。</span><span class="sxs-lookup"><span data-stu-id="67e20-147">Specifically, WIC provides bitmap source transforms for scaling, clipping, rotating, and flipping pixel data.</span></span> <span data-ttu-id="67e20-148">這些點陣圖來源轉換有 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)和 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)。</span><span class="sxs-lookup"><span data-stu-id="67e20-148">These bitmap source transforms are [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), and [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span> <span data-ttu-id="67e20-149">這些點陣圖來源的每一個都有方法可初始化並建立新的轉換點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="67e20-149">Each of these bitmap sources have a method to initialize and create a new transformed bitmap source.</span></span> <span data-ttu-id="67e20-150">例如， **IWICBitmapClipper** 包括 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="67e20-150">For example, the **IWICBitmapClipper** includes the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span> <span data-ttu-id="67e20-151">這個方法會在指定的 [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)上，使用輸入點陣圖來源的裁剪圖元資料來初始化 clipper 點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="67e20-151">This method initializes the clipper bitmap source with the clipped pixel data of the input bitmap source at the given [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect).</span></span>

<span data-ttu-id="67e20-152">下列的 how to 主題示範轉換點陣圖來源的不同用途。</span><span class="sxs-lookup"><span data-stu-id="67e20-152">The following how-to topics demonstrate different uses of the transform bitmap sources.</span></span>

-   [<span data-ttu-id="67e20-153">如何調整點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-153">How to Scale a Bitmap Source</span></span>](-wic-bitmapsources-howto-scale.md)
-   [<span data-ttu-id="67e20-154">如何裁剪點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-154">How to Clip a Bitmap Source</span></span>](-wic-bitmapsources-howto-clip.md)
-   [<span data-ttu-id="67e20-155">如何翻轉和旋轉點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-155">How to Flip and Rotate a Bitmap Source</span></span>](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a><span data-ttu-id="67e20-156">像素格式和色彩內容轉換器</span><span class="sxs-lookup"><span data-stu-id="67e20-156">Pixel Format and Color Context Converters</span></span>

<span data-ttu-id="67e20-157">WIC 也提供點陣圖來源轉換點陣圖來源的像素格式和色彩內容。</span><span class="sxs-lookup"><span data-stu-id="67e20-157">WIC also provides bitmap sources converting the pixel format and color context of a bitmap source.</span></span> <span data-ttu-id="67e20-158">WIC 提供這些作業的 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 和 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) 。</span><span class="sxs-lookup"><span data-stu-id="67e20-158">WIC provides the [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) and [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) for these operations.</span></span>

<span data-ttu-id="67e20-159">[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 會將指定的點陣圖來源從一個像素格式轉換成另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="67e20-159">[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) converts a given bitmap source from one pixel format to another.</span></span>

<span data-ttu-id="67e20-160">如需使用 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)的範例，請參閱 [如何使用 Direct2D 繪製點陣圖來源](-wic-bitmapsources-howto-drawusingd2d.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="67e20-160">For an example using the [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter), see the [How to Draw a Bitmap Source Using Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) topic.</span></span>

## <a name="drawing-bitmap-sources"></a><span data-ttu-id="67e20-161">繪製點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-161">Drawing Bitmap Sources</span></span>

<span data-ttu-id="67e20-162">WIC 是靜止的影像編解碼器技術，可用來管理影像資料和中繼資料，而不是原本提供呈現影像的方式。</span><span class="sxs-lookup"><span data-stu-id="67e20-162">WIC is a still image codec technology and is used to manage image data and metadata and does not inherently provide a way to render images.</span></span> <span data-ttu-id="67e20-163">不過，您可以使用數種 Windows 圖形技術來繪製點陣圖來源，例如 Direct2D、Windows 圖形裝置介面 (GDI) 和 Windows GDI +。</span><span class="sxs-lookup"><span data-stu-id="67e20-163">However, bitmap sources can be drawn using several Windows graphics technology such as Direct2D, Windows Graphics Device Interface (GDI), and Windows GDI+.</span></span> <span data-ttu-id="67e20-164">這些技術各有不同的 WIC 互通性層級。</span><span class="sxs-lookup"><span data-stu-id="67e20-164">Each of these technologies has a different level of interoperability with WIC.</span></span> <span data-ttu-id="67e20-165">Direct2D 透過 [ID2D1Bitmap](../direct2d/render-targets-overview.md) 介面和 [ID2D1RenderTarget：： CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) 方法提供直接的互通性，而 gdi 和 gdi + 則需要使用者將點陣圖來源圖元複製到 [點陣圖](../gdi/bitmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="67e20-165">Direct2D provides direct interoperability through the [ID2D1Bitmap](../direct2d/render-targets-overview.md) interface and the [ID2D1RenderTarget::CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) method while GDI and GDI+ require users to copy the bitmap source pixels into an [Bitmaps](../gdi/bitmaps.md).</span></span>

<span data-ttu-id="67e20-166">下列範例示範如何使用 Direct2D 繪製點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="67e20-166">The following example demonstrate how to draw bitmap sources by using Direct2D.</span></span>

-   [<span data-ttu-id="67e20-167">如何使用 Direct2D 繪製點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="67e20-167">How to Draw a Bitmap Source Using Direct2D</span></span>](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a><span data-ttu-id="67e20-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="67e20-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67e20-169">**概念**</span><span class="sxs-lookup"><span data-stu-id="67e20-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67e20-170">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="67e20-170">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="67e20-171">編碼總覽</span><span class="sxs-lookup"><span data-stu-id="67e20-171">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> <dt>

<span data-ttu-id="67e20-172">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="67e20-172">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="67e20-173">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="67e20-173">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
