---
description: 本主題將示範使用 Direct2D 繪製 IWICBitmapSource 的程式。
ms.assetid: 11d38c9a-775d-41f7-a193-37b702b29a96
title: 如何使用 Direct2D 繪製 BitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6dfdddb7cd6f7ab7341eb3c13a9fe40b797f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974458"
---
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a><span data-ttu-id="e28b7-103">如何使用 Direct2D 繪製 BitmapSource</span><span class="sxs-lookup"><span data-stu-id="e28b7-103">How to Draw a BitmapSource Using Direct2D</span></span>

<span data-ttu-id="e28b7-104">本主題將示範使用 Direct2D 繪製 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 的程式。</span><span class="sxs-lookup"><span data-stu-id="e28b7-104">This topic demonstrates the process for drawing an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using Direct2D.</span></span>

<span data-ttu-id="e28b7-105">使用 Direct2D 繪製點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="e28b7-105">To draw a bitmap source by using Direct2D</span></span>

1.  <span data-ttu-id="e28b7-106">解碼來源影像並取得點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="e28b7-106">Decode a source image and obtain a bitmap source.</span></span> <span data-ttu-id="e28b7-107">在此範例中，會使用 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 來解碼影像，並抓取第一個影像畫面格。</span><span class="sxs-lookup"><span data-stu-id="e28b7-107">In this example, an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) is used to decode the image and the first image frame is retrieved.</span></span>

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

    

    <span data-ttu-id="e28b7-108">若要繪製其他類型的點陣圖來源，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="e28b7-108">For additional types of bitmap sources to draw, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

2.  <span data-ttu-id="e28b7-109">將點陣圖來源轉換成32bppPBGRA 像素格式。</span><span class="sxs-lookup"><span data-stu-id="e28b7-109">Convert the bitmap source to an 32bppPBGRA pixel format.</span></span>

    <span data-ttu-id="e28b7-110">Direct2D 必須先轉換成32bppPBGRA 像素格式，才能使用映射。</span><span class="sxs-lookup"><span data-stu-id="e28b7-110">Before Direct2D can use an image, it must be converted to the 32bppPBGRA pixel format.</span></span> <span data-ttu-id="e28b7-111">若要轉換影像格式，請使用 [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) 方法來建立 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 物件。</span><span class="sxs-lookup"><span data-stu-id="e28b7-111">To convert the image format, use the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span> <span data-ttu-id="e28b7-112">一旦建立之後，請使用 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) 方法來執行轉換。</span><span class="sxs-lookup"><span data-stu-id="e28b7-112">Once created, use the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>

    ```C++
       // Format convert the frame to 32bppPBGRA
       if (SUCCEEDED(hr))
       {
           SafeRelease(&m_pConvertedSourceBitmap);
           hr = m_pIWICFactory->CreateFormatConverter(&m_pConvertedSourceBitmap);
       }

       if (SUCCEEDED(hr))
       {
           hr = m_pConvertedSourceBitmap->Initialize(
               pFrame,                          // Input bitmap to convert
               GUID_WICPixelFormat32bppPBGRA,   // Destination pixel format
               WICBitmapDitherTypeNone,         // Specified dither pattern
               NULL,                            // Specify a particular palette 
               0.f,                             // Alpha threshold
               WICBitmapPaletteTypeCustom       // Palette translation type
               );
       }
    ```

    

3.  <span data-ttu-id="e28b7-113">建立 [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 物件，以轉譯為視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="e28b7-113">Create an [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) object for rendering to a window handle.</span></span>

    ```C++
       // Create a D2D render target properties
       D2D1_RENDER_TARGET_PROPERTIES renderTargetProperties = D2D1::RenderTargetProperties();

       // Set the DPI to be the default system DPI to allow direct mapping
       // between image pixels and desktop pixels in different system DPI settings
       renderTargetProperties.dpiX = DEFAULT_DPI;
       renderTargetProperties.dpiY = DEFAULT_DPI;

       // Create a D2D render target
       D2D1_SIZE_U size = D2D1::SizeU(rc.right - rc.left, rc.bottom - rc.top);

       hr = m_pD2DFactory->CreateHwndRenderTarget(
           renderTargetProperties,
           D2D1::HwndRenderTargetProperties(hWnd, size),
           &m_pRT
           );
    ```

    

    <span data-ttu-id="e28b7-114">如需呈現目標的詳細資訊，請參閱 Direct2D 轉譯 [目標總覽](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)。</span><span class="sxs-lookup"><span data-stu-id="e28b7-114">For more information render targets, see the Direct2D [Render Targets Overview](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget).</span></span>

4.  <span data-ttu-id="e28b7-115">使用[ID2D1RenderTarget：： CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md)方法來建立[ID2D1Bitmap](../direct2d/render-targets-overview.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e28b7-115">Create an [ID2D1Bitmap](../direct2d/render-targets-overview.md) object using the [ID2D1RenderTarget::CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) method.</span></span>

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  <span data-ttu-id="e28b7-116">使用 D2D [](../direct2d/render-targets-overview.md) ID2D1RenderTarget 繪製 ID2D1Bitmap [：:D rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md)方法。</span><span class="sxs-lookup"><span data-stu-id="e28b7-116">Draw the [ID2D1Bitmap](../direct2d/render-targets-overview.md) using D2D [ID2D1RenderTarget::DrawBitmap](../direct2d/id2d1rendertarget-drawbitmap.md) method.</span></span>

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

<span data-ttu-id="e28b7-117">此範例中省略了程式碼。</span><span class="sxs-lookup"><span data-stu-id="e28b7-117">Code has been omitted from this example.</span></span> <span data-ttu-id="e28b7-118">如需完整的程式碼，請參閱 [使用 Direct2D 範例的 WIC 映射檢視器](-wic-sample-d2d-viewer.md)。</span><span class="sxs-lookup"><span data-stu-id="e28b7-118">For the complete code, see the [WIC Image Viewer Using Direct2D Sample](-wic-sample-d2d-viewer.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e28b7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e28b7-119">See Also</span></span>

[<span data-ttu-id="e28b7-120">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e28b7-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="e28b7-121">參考</span><span class="sxs-lookup"><span data-stu-id="e28b7-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="e28b7-122">範例</span><span class="sxs-lookup"><span data-stu-id="e28b7-122">Samples</span></span>](-wic-samples.md)


[<span data-ttu-id="e28b7-123">Direct2D</span><span class="sxs-lookup"><span data-stu-id="e28b7-123">Direct2D</span></span>](../direct2d/direct2d-portal.md)


 

 
