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
# <a name="how-to-flip-and-rotate-a-bitmap-source"></a><span data-ttu-id="3ba9e-103">如何翻轉和旋轉點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="3ba9e-103">How to Flip and Rotate a Bitmap Source</span></span>

<span data-ttu-id="3ba9e-104">本主題示範如何使用 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)元件來旋轉 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-104">This topic demonstrates how to rotate an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) by using an [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) component.</span></span>

<span data-ttu-id="3ba9e-105">翻轉和旋轉點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="3ba9e-105">To flip and rotate a bitmap source</span></span>

1.  <span data-ttu-id="3ba9e-106">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 物件，以建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="3ba9e-107">使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

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

    

3.  <span data-ttu-id="3ba9e-108">取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="3ba9e-109">JPEG 檔案格式只支援單一框架。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="3ba9e-110">因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="3ba9e-111">若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="3ba9e-112">建立用來翻轉影像的 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-112">Create the [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) to use for flipping the image.</span></span>

    ```C++
    // Create the flip/rotator.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFlipRotator(&pIFlipRotator);
    }
    ```

    

5.  <span data-ttu-id="3ba9e-113">使用沿著垂直 y 軸) 垂直翻轉 (點陣圖框架的影像資料，初始化翻轉/旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-113">Initialize the flip/rotator object with the image data of the bitmap frame flipped horizontally (along the vertical y-axis).</span></span>

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

    

    <span data-ttu-id="3ba9e-114">如需其他的旋轉和翻轉選項，請參閱 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-114">See [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) for additional rotations and flipping options.</span></span>

6.  <span data-ttu-id="3ba9e-115">繪製或處理翻轉的點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-115">Draw or process the flipped bitmap source.</span></span>

    > [!Note]  
    > <span data-ttu-id="3ba9e-116">[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)介面繼承自 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)介面，因此您可以在任何接受 **IWICBitmapSource** 的位置使用已初始化的翻轉/旋轉物件。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-116">The [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) interface inherits from the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, so you can use the initialized flip/rotator object anywhere that accepts a **IWICBitmapSource**.</span></span>

     

    <span data-ttu-id="3ba9e-117">下圖將示範如何沿著垂直 X 軸) 水準翻轉影像 (。</span><span class="sxs-lookup"><span data-stu-id="3ba9e-117">The following illustration demonstrates flipping an imaging horizontally (along the vertical x-axis).</span></span>

    ![顯示影像 verital X 軸) 水準翻轉 (的圖例](graphics/fliphorizontal.png)

## <a name="see-also"></a><span data-ttu-id="3ba9e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ba9e-119">See Also</span></span>

[<span data-ttu-id="3ba9e-120">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="3ba9e-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="3ba9e-121">參考</span><span class="sxs-lookup"><span data-stu-id="3ba9e-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="3ba9e-122">範例</span><span class="sxs-lookup"><span data-stu-id="3ba9e-122">Samples</span></span>](-wic-samples.md)


 

 



