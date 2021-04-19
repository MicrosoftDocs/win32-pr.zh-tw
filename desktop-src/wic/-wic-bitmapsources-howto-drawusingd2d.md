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
# <a name="how-to-draw-a-bitmapsource-using-direct2d"></a>如何使用 Direct2D 繪製 BitmapSource

本主題將示範使用 Direct2D 繪製 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 的程式。

使用 Direct2D 繪製點陣圖來源

1.  解碼來源影像並取得點陣圖來源。 在此範例中，會使用 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 來解碼影像，並抓取第一個影像畫面格。

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

    

    若要繪製其他類型的點陣圖來源，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

2.  將點陣圖來源轉換成32bppPBGRA 像素格式。

    Direct2D 必須先轉換成32bppPBGRA 像素格式，才能使用映射。 若要轉換影像格式，請使用 [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) 方法來建立 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) 物件。 一旦建立之後，請使用 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) 方法來執行轉換。

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

    

3.  建立 [ID2D1RenderTarget](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 物件，以轉譯為視窗控制碼。

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

    

    如需呈現目標的詳細資訊，請參閱 Direct2D 轉譯 [目標總覽](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)。

4.  使用[ID2D1RenderTarget：： CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md)方法來建立[ID2D1Bitmap](../direct2d/render-targets-overview.md)物件。

    ```C++
        // D2DBitmap may have been released due to device loss. 
        // If so, re-create it from the source bitmap
        if (m_pConvertedSourceBitmap && !m_pD2DBitmap)
        {
            m_pRT->CreateBitmapFromWicBitmap(m_pConvertedSourceBitmap, NULL, &m_pD2DBitmap);
        }
    ```

    

5.  使用 D2D [](../direct2d/render-targets-overview.md) ID2D1RenderTarget 繪製 ID2D1Bitmap [：:D rawbitmap](../direct2d/id2d1rendertarget-drawbitmap.md)方法。

    ```C++
        // Draws an image and scales it to the current window size
        if (m_pD2DBitmap)
        {
            m_pRT->DrawBitmap(m_pD2DBitmap, rectangle);
        }
    ```

    

此範例中省略了程式碼。 如需完整的程式碼，請參閱 [使用 Direct2D 範例的 WIC 映射檢視器](-wic-sample-d2d-viewer.md)。

## <a name="see-also"></a>另請參閱

[程式設計指南](-wic-programming-guide.md)


[參考](-wic-codec-reference.md)


[範例](-wic-samples.md)


[Direct2D](../direct2d/direct2d-portal.md)


 

 
