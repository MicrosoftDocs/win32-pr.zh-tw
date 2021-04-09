---
description: 本主題示範如何從應用程式資源載入 IWICBitmapFrameDecode。
ms.assetid: 2260ad3a-44d4-4fe2-aa8c-608ffc11fbfb
title: 如何從資源 (Windows 影像處理元件) 載入點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb33ad57b3b9dac1cb5d98719c681adb38c11de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849692"
---
# <a name="how-to-load-a-bitmap-from-a-resource-windows-imaging-component"></a>如何從資源 (Windows 影像處理元件) 載入點陣圖

本主題示範如何從應用程式資源載入 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。

1.  在應用程式資源定義 ( .rc) 檔案中，定義資源。 下列範例會定義 `Image` 名為的資源 `IDR_SAMPLE_IMAGE` 。

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

    

4.  使用 [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) 方法來建立 [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) 物件，並使用映射記憶體指標將它初始化。

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

    

5.  使用 [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法，從新的資料流程物件建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。

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

    

6.  從已解碼的影像取出 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。

    ```C++
    // Retrieve the initial frame.
    if (SUCCEEDED(hr)){
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    此程式碼只會抓取影像的第一個 (`0`) 畫面格。 若為多框架影像，請使用 [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) 來判斷影像中的框架數目。

## <a name="see-also"></a>另請參閱

[程式設計指南](-wic-programming-guide.md)


[參考](-wic-codec-reference.md)


[範例](-wic-samples.md)


 

 



