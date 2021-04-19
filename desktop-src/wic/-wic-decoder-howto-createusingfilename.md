---
description: 本主題說明如何使用映射檔案名來建立點陣圖解碼器。
ms.assetid: b384861d-4e71-4e07-8b44-5c1cbcb3a70f
title: 如何使用映射檔案名建立解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 113ea82b741f2a8dab6c92d6391d65eb7d7e99c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985094"
---
# <a name="how-to-create-a-decoder-using-an-image-filename"></a><span data-ttu-id="a91e8-103">如何使用映射檔案名建立解碼器</span><span class="sxs-lookup"><span data-stu-id="a91e8-103">How to Create a Decoder Using an Image Filename</span></span>

<span data-ttu-id="a91e8-104">本主題說明如何使用映射檔案名來建立點陣圖解碼器。</span><span class="sxs-lookup"><span data-stu-id="a91e8-104">This topic describes how to create a bitmap decoder by using an image filename.</span></span>

<span data-ttu-id="a91e8-105">使用映射檔案名建立點陣圖解碼</span><span class="sxs-lookup"><span data-stu-id="a91e8-105">To create a bitmap decoder by using an image filename</span></span>

1.  <span data-ttu-id="a91e8-106">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 物件，以建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="a91e8-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="a91e8-107">使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="a91e8-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="a91e8-108">取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="a91e8-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="a91e8-109">JPEG 檔案格式只支援單一框架。</span><span class="sxs-lookup"><span data-stu-id="a91e8-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="a91e8-110">因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。</span><span class="sxs-lookup"><span data-stu-id="a91e8-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="a91e8-111">若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="a91e8-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="a91e8-112">處理影像框架。</span><span class="sxs-lookup"><span data-stu-id="a91e8-112">Process the image frame.</span></span> <span data-ttu-id="a91e8-113">如需 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="a91e8-113">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a91e8-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a91e8-114">See Also</span></span>

[<span data-ttu-id="a91e8-115">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a91e8-115">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="a91e8-116">參考</span><span class="sxs-lookup"><span data-stu-id="a91e8-116">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="a91e8-117">範例</span><span class="sxs-lookup"><span data-stu-id="a91e8-117">Samples</span></span>](-wic-samples.md)


 

 



