---
description: 本主題說明如何使用映射檔案名來建立點陣圖解碼器。
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: 如何使用映射檔案名建立解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867581e06692188913e4bb1af4956956c462c46bc189a4983f3c5d24bc38c986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811988"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a>如何使用映射檔案名建立解碼器

本主題說明如何使用映射檔案名來建立點陣圖解碼器。

使用映射檔案名建立點陣圖解碼

1.  建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)物件，以建立 Windows 影像處理元件 (WIC) 物件。

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

4.  處理影像框架。 如需 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

## <a name="see-also"></a>另請參閱

[程式設計指南](-wic-programming-guide.md)


[參考](-wic-codec-reference.md)


[範例](-wic-samples.md)


 

 



