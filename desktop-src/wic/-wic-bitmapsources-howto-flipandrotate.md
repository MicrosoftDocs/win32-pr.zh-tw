---
description: 本主題示範如何使用 IWICBitmapFlipRotator 元件來旋轉 IWICBitmapSource。
ms.assetid: 371c7759-0165-4a2a-b2ff-f9c8a31053a4
title: 如何翻轉和旋轉點陣圖來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f6a805144025f185a4f4793fc4fafb27d7695a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112864"
---
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a>如何翻轉和旋轉點陣圖來源

本主題示範如何使用 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)元件來旋轉 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。

翻轉和旋轉點陣圖來源

1.  建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 物件，以建立 WINDOWS 影像處理元件 (WIC) 物件。

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapFlipRotator *pIFlipRotator = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    JPEG 檔案格式只支援單一框架。 因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。 若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。

4.  建立用來翻轉影像的 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) 。

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  使用沿著垂直 y 軸) 垂直翻轉 (點陣圖框架的影像資料，初始化翻轉/旋轉物件。

    ```C++
    // Initialize the flip/rotator to flip the original source horizontally.
    if (SUCCEEDED(hr))
    {
       hr = pIFlipRotator->Initialize(
          pIDecoderFrame,                     // Bitmap source to flip.
          WICBitmapTransformFlipHorizontal);  // Flip the pixels along the 
                                              //  vertical y-axis.
    }
    ```

    

    如需其他的旋轉和翻轉選項，請參閱 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 。

6.  繪製或處理翻轉的點陣圖來源。

    > [!Note]  
    > [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)介面繼承自 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)介面，因此您可以在任何接受 **IWICBitmapSource** 的位置使用已初始化的翻轉/旋轉物件。

     

    下圖將示範如何沿著垂直 X 軸) 水準翻轉影像 (。

    ![顯示影像 verital X 軸) 水準翻轉 (的圖例](graphics/fliphorizontal.png)

## <a name="see-also"></a>另請參閱

[程式設計指南](-wic-programming-guide.md)


[參考](-wic-codec-reference.md)


[範例](-wic-samples.md)


 

 



