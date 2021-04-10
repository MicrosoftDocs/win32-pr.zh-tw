---
title: 如何從檔案載入點陣圖
description: 顯示如何從影像檔載入 Direct2D 點陣圖。
ms.assetid: 4abfbc2b-2730-4d96-897e-1e2232383a72
ms.topic: article
ms.date: 03/09/2019
ms.openlocfilehash: c9590e799e71e92056157b75573565cf79b9236b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682757"
---
# <a name="how-to-load-a-bitmap-from-a-file"></a><span data-ttu-id="8a9f0-103">如何從檔案載入點陣圖</span><span class="sxs-lookup"><span data-stu-id="8a9f0-103">How to Load a Bitmap from a File</span></span>

<span data-ttu-id="8a9f0-104">Direct2D 使用 Windows 影像處理元件 (WIC) 載入點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-104">Direct2D uses the Windows Imaging Component (WIC) to load bitmaps.</span></span> <span data-ttu-id="8a9f0-105">若要從檔案載入點陣圖，請先使用 WIC 物件載入影像，並將它轉換成與 Direct2D 相容的格式，然後使用 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) 方法來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-105">To load a bitmap from a file, first use WIC objects to load the image and to convert it to a Direct2D-compatible format, then use the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span>

1.  <span data-ttu-id="8a9f0-106">使用 [**IWICImagingFactory：： CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)方法建立 [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-106">Create an [**IWICBitmapDecoder**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapdecoder) by using the [**IWICImagingFactory::CreateDecoderFromFileName**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

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

    

2.  <span data-ttu-id="8a9f0-107">從影像取出框架，然後將框架儲存在 [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) 物件中。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-107">Retrieve a frame from the image and store the frame in an [**IWICBitmapFrameDecode**](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

    ```C++
        if (SUCCEEDED(hr))
        {
            // Create the initial frame.
            hr = pDecoder->GetFrame(0, &pSource);
        }
    ```

    

3.  <span data-ttu-id="8a9f0-108">點陣圖必須轉換成 Direct2D 可以使用的格式，因此請將影像的像素格式轉換成32bppPBGRA。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-108">The bitmap must be converted to a format that Direct2D can use, so convert the image's pixel format to 32bppPBGRA.</span></span> <span data-ttu-id="8a9f0-109"> (如需支援格式的清單，請參閱 [像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。 ) 。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-109">(For a list of supported formats, see [Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).).</span></span> <span data-ttu-id="8a9f0-110">呼叫 [**IWICImagingFactory：： CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) 方法來建立 [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) 物件，然後呼叫 **IWICFormatConverter** 物件的 [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) 方法來執行轉換。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-110">Call the [**IWICImagingFactory::CreateFormatConverter**](/windows/win32/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method to create an [**IWICFormatConverter**](/windows/win32/api/wincodec/nn-wincodec-iwicformatconverter) object, then call the **IWICFormatConverter** object's [**Initialize**](/windows/win32/api/wincodec/nf-wincodec-iwicformatconverter-initialize) method to perform the conversion.</span></span>
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

    

4.  <span data-ttu-id="8a9f0-111">呼叫 [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) 方法來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 物件，此物件可由轉譯目標繪製並用於其他 Direct2D 物件。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-111">Call the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md) method to create an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object that can be drawn by a render target and used with other Direct2D objects.</span></span>
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

    

<span data-ttu-id="8a9f0-112">此範例中省略了某些程式碼。</span><span class="sxs-lookup"><span data-stu-id="8a9f0-112">Some code has been omitted from this example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a9f0-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a9f0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a9f0-114">**ID2D1Bitmap**</span><span class="sxs-lookup"><span data-stu-id="8a9f0-114">**ID2D1Bitmap**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[<span data-ttu-id="8a9f0-115">**CreateBitmapFromWicBitmap**</span><span class="sxs-lookup"><span data-stu-id="8a9f0-115">**CreateBitmapFromWicBitmap**</span></span>](id2d1rendertarget-createbitmapfromwicbitmap.md)
</dt> <dt>

[<span data-ttu-id="8a9f0-116">如何從資源載入點陣圖</span><span class="sxs-lookup"><span data-stu-id="8a9f0-116">How to Load a Bitmap from a Resource</span></span>](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 