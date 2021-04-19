---
description: 本主題說明如何使用資料流程建立點陣圖解碼器。
ms.assetid: 982d2110-ff2f-43e0-a931-cb2b8146ad0a
title: 如何使用資料流程建立解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a76badec0e2587f9136cfa6bc3ff041b76592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982089"
---
# <a name="how-to-create-a-decoder-using-a-stream"></a>如何使用資料流程建立解碼器

本主題說明如何使用資料流程建立點陣圖解碼器。

使用資料流程建立點陣圖解碼

1.  將影像檔載入資料流程中。 在此範例中，會建立應用程式資源的資料流程。

    在應用程式資源定義 ( .rc) 檔案中，定義資源。 下列範例會定義 `Image` 名為的資源 `IDR_SAMPLE_IMAGE` 。

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    建立應用程式時，會將資源新增至應用程式的資源。

2.  從應用程式載入資源。

    ```C++
    HRESULT hr = S_OK;

    // WIC interface pointers.
    IWICStream *pIWICStream = NULL;
    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame = NULL;

    // Resource management.
    HRSRC imageResHandle = NULL;
    HGLOBAL imageResDataHandle = NULL;
    void *pImageFile = NULL;
    DWORD imageFileSize = 0;

    // Locate the resource in the application's executable.
    imageResHandle = FindResource(
       NULL,             // This component.
       L"SampleImage",   // Resource name.
       L"Image");        // Resource type.

    hr = (imageResHandle ? S_OK : E_FAIL);

    // Load the resource to the HGLOBAL.
    if (SUCCEEDED(hr)){
       imageResDataHandle = LoadResource(NULL, imageResHandle);
       hr = (imageResDataHandle ? S_OK : E_FAIL);
    }
    
    ```

    

3.  鎖定資源並取得大小。

    ```C++
    // Lock the resource to retrieve memory pointer.
    if (SUCCEEDED(hr)){
       pImageFile = LockResource(imageResDataHandle);
       hr = (pImageFile ? S_OK : E_FAIL);
    }

    // Calculate the size.
    if (SUCCEEDED(hr)){
       imageFileSize = SizeofResource(NULL, imageResHandle);
       hr = (imageFileSize ? S_OK : E_FAIL);
    }
    
    ```

    

4.  建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 來建立 WINDOWS 影像處理元件 (WIC) 物件。

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  使用 [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) 方法來建立 [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) 物件，並使用映射記憶體指標將它初始化。

    ```C++
    // Create a WIC stream to map onto the memory.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateStream(&pIWICStream);
    }

    // Initialize the stream with the memory pointer and size.
    if (SUCCEEDED(hr)){
       hr = pIWICStream->InitializeFromMemory(
             reinterpret_cast<BYTE*>(pImageFile),
             imageFileSize);
    }
    ```

    

6.  使用 [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法，從新的資料流程物件建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。

    ```C++
    // Create a decoder for the stream.
    if (SUCCEEDED(hr)){
       hr = m_pIWICFactory->CreateDecoderFromStream(
          pIWICStream,                   // The stream to use to create the decoder
          NULL,                          // Do not prefer a particular vendor
          WICDecodeMetadataCacheOnLoad,  // Cache metadata when needed
          &pIDecoder);                   // Pointer to the decoder
    }
    ```

    

7.  取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    JPEG 檔案格式只支援單一框架。 因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。 若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。

8.  處理影像框架。 如需 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。

## <a name="see-also"></a>另請參閱

[程式設計指南](-wic-programming-guide.md)


[參考](-wic-codec-reference.md)


[範例](-wic-samples.md)


 

 



