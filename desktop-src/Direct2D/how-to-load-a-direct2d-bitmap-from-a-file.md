---
title: 如何從檔案載入點陣圖
description: 顯示如何從影像檔載入 Direct2D 點陣圖。
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: a330f0e32ee4abf62eb7df1c1d6a00b3f217e6f04502cebae6c489aa01eaaa9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824558"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a>如何從檔案載入點陣圖

Direct2D 使用 Windows 影像處理元件 (WIC) 載入點陣圖。 若要從檔案載入點陣圖，請先使用 WIC 物件載入影像，並將它轉換成與 Direct2D 相容的格式，然後使用 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) 方法來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)。

1.  使用 [**IWICImagingFactory：： CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)方法建立 [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) 。

    ```C++
    HRESULT DemoApp::LoadBitmapFromFile(
        ID2D1RenderTarget *pRenderTarget,
        IWICImagingFactory *pIWICFactory,
        PCWSTR uri,
        UINT destinationWidth,
        UINT destinationHeight,
        ID2D1Bitmap **ppBitmap
        )
    {
        IWICBitmapDecoder *pDecoder = NULL;
        IWICBitmapFrameDecode *pSource = NULL;
        IWICStream *pStream = NULL;
        IWICFormatConverter *pConverter = NULL;
        IWICBitmapScaler *pScaler = NULL;

        HRESULT hr = pIWICFactory->CreateDecoderFromFilename(
            uri,
            NULL,
            GENERIC_READ,
            WICDecodeMetadataCacheOnLoad,
            &pDecoder
            );
            
    ```

    

2.  從影像取出框架，然後將框架儲存在 [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) 物件中。

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  點陣圖必須轉換成 Direct2D 可以使用的格式，因此請將影像的像素格式轉換成32bppPBGRA。  (如需支援格式的清單，請參閱 [像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。 ) 。 呼叫 [**IWICImagingFactory：： CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) 方法來建立 [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) 物件，然後呼叫 **IWICFormatConverter** 物件的 [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) 方法來執行轉換。
    ```C++
        if (SUCCEEDED(hr))
        {

            // Convert the image format to 32bppPBGRA
            // (DXGI_FORMAT_B8G8R8A8_UNORM + D2D1_ALPHA_MODE_PREMULTIPLIED).
            hr = pIWICFactory->CreateFormatConverter(&pConverter);

        }
     
     
        if (SUCCEEDED(hr))
        {
            hr = pConverter->Initialize(
                pSource,
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                NULL,
                0.f,
                WICBitmapPaletteTypeMedianCut
                );
    ```

    

4.  呼叫 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) 方法來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 物件，此物件可由轉譯目標繪製並用於其他 Direct2D 物件。
    ```C++
        if (SUCCEEDED(hr))
        {
        
            // Create a Direct2D bitmap from the WIC bitmap.
            hr = pRenderTarget->CreateBitmapFromWicBitmap(
                pConverter,
                NULL,
                ppBitmap
                );
        }

        SafeRelease(&pDecoder);
        SafeRelease(&pSource);
        SafeRelease(&pStream);
        SafeRelease(&pConverter);
        SafeRelease(&pScaler);

        return hr;
    }
    ```

    

此範例中省略了某些程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 