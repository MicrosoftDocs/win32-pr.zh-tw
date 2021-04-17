---
description: 本主題示範如何使用 IWICBitmapClipper 元件取得 IWICBitmapSource 的矩形部分。
ms.assetid: c9834827-8e1d-436d-be82-c1a2a2f7ca5c
title: 如何裁剪點陣圖來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43919e03d5d866d37ad4af203e741d2b10e60889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568057"
---
# <a name="how-to-clip-a-bitmap-source"></a><span data-ttu-id="57310-103">如何裁剪點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="57310-103">How to Clip a Bitmap Source</span></span>

<span data-ttu-id="57310-104">本主題示範如何使用 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)元件取得 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)的矩形部分。</span><span class="sxs-lookup"><span data-stu-id="57310-104">This topic demonstrates how to obtain a rectangular portion of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using an [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) component.</span></span>

<span data-ttu-id="57310-105">若要裁剪點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="57310-105">To clip a bitmap source</span></span>

1.  <span data-ttu-id="57310-106">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 物件，以建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="57310-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="57310-107">使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="57310-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="57310-108">取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="57310-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="57310-109">JPEG 檔案格式只支援單一框架。</span><span class="sxs-lookup"><span data-stu-id="57310-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="57310-110">因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。</span><span class="sxs-lookup"><span data-stu-id="57310-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="57310-111">若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="57310-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="57310-112">建立要用於影像裁剪的 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) 。</span><span class="sxs-lookup"><span data-stu-id="57310-112">Create the [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) to use for the image clipping.</span></span>

    ```C++
    IWICBitmapClipper *pIClipper = NULL;

    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapClipper(&pIClipper);
    }
    ```

    

5.  <span data-ttu-id="57310-113">使用點陣圖框架指定矩形內的影像資料，初始化 clipper 物件。</span><span class="sxs-lookup"><span data-stu-id="57310-113">Initialize the clipper object with the image data within the given rectangle of the bitmap frame.</span></span>

    ```C++
    // Create the clipping rectangle.
    WICRect rcClip = { 0, 0, uiWidth/2, uiHeight/2 };

    // Initialize the clipper with the given rectangle of the frame's image data.
    if (SUCCEEDED(hr))
    {
       hr = pIClipper->Initialize(pIDecoderFrame, &rcClip);
    }
    ```

    

6.  <span data-ttu-id="57310-114">繪製或處理裁剪的影像。</span><span class="sxs-lookup"><span data-stu-id="57310-114">Draw or process the clipped image.</span></span>

    <span data-ttu-id="57310-115">下圖示范影像裁剪。</span><span class="sxs-lookup"><span data-stu-id="57310-115">The following illustration demonstrates imaging clipping.</span></span> <span data-ttu-id="57310-116">左邊的原始影像是 200 x 130 圖元。</span><span class="sxs-lookup"><span data-stu-id="57310-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="57310-117">右邊的影像是裁剪成所定義之矩形的原始影像 `{20,20,100,100}` 。</span><span class="sxs-lookup"><span data-stu-id="57310-117">The image on the right is the original image clipped to a rectangle defined as `{20,20,100,100}`.</span></span>

    ![影像裁剪的圖例](graphics/cliparegion_axisalignedclip.png)

## <a name="see-also"></a><span data-ttu-id="57310-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57310-119">See Also</span></span>

[<span data-ttu-id="57310-120">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="57310-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="57310-121">參考</span><span class="sxs-lookup"><span data-stu-id="57310-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="57310-122">範例</span><span class="sxs-lookup"><span data-stu-id="57310-122">Samples</span></span>](-wic-samples.md)


 

 



