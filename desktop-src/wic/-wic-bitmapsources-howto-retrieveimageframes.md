---
description: 本主題示範如何將多框架影像解碼，以及抓取每個畫面格進行處理。
ms.assetid: e4f69608-7bf1-4d54-b586-b749526700c9
title: 如何從影像中取出畫面格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeeb19e0a0ac69f75673df0736fd0bd4987b3423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112861"
---
# <a name="how-to-retrieve-the-frames-from-an-image"></a><span data-ttu-id="4d539-103">如何從影像中取出畫面格</span><span class="sxs-lookup"><span data-stu-id="4d539-103">How to Retrieve the Frames from an Image</span></span>

<span data-ttu-id="4d539-104">本主題示範如何將多框架影像解碼，以及抓取每個畫面格進行處理。</span><span class="sxs-lookup"><span data-stu-id="4d539-104">This topic demonstrates how to decode a multi-frame image and retrieve each frame for processing.</span></span>

<span data-ttu-id="4d539-105">取出影像的框架</span><span class="sxs-lookup"><span data-stu-id="4d539-105">To retrieve the frames of an image</span></span>

1.  <span data-ttu-id="4d539-106">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 來建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="4d539-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="4d539-107">使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="4d539-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    UINT nFrameCount = 0;
    UINT uiWidth, uiHeight;

    // Create decoder for an image.
    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"creek.tiff",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="4d539-108">取出影像中的框架數目。</span><span class="sxs-lookup"><span data-stu-id="4d539-108">Retrieve the number of frames in the images.</span></span>

    ```C++
    // Retrieve the frame count of the image.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrameCount(&nFrameCount);
    }
    ```

    

4.  <span data-ttu-id="4d539-109">藉由為影像中的每個畫面格取得 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 來處理每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="4d539-109">Process each frame by obtaining an [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) for each frame in the image.</span></span>

    ```C++
    // Process each frame in the image.
    for (UINT i=0; i < nFrameCount; i++)
    {
       // Retrieve the next bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoder->GetFrame(i, &pIDecoderFrame);
       }

       // Retrieve the size of the bitmap frame.
       if (SUCCEEDED(hr))
       {
          hr = pIDecoderFrame->GetSize(&uiWidth, &uiHeight);
       }

       // Additional frame processing.
       // ...

       SafeRelease(&pIDecoderFrame);
    }
    ```

    

## <a name="see-also"></a><span data-ttu-id="4d539-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d539-110">See Also</span></span>

[<span data-ttu-id="4d539-111">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="4d539-111">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="4d539-112">參考</span><span class="sxs-lookup"><span data-stu-id="4d539-112">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="4d539-113">範例</span><span class="sxs-lookup"><span data-stu-id="4d539-113">Samples</span></span>](-wic-samples.md)


 

 



