---
description: 本主題示範如何使用 IWICBitmapScaler 元件來調整 IWICBitmapSource。
ms.assetid: d2c65c9b-6f52-46f7-935d-0c582ca83867
title: 如何調整點陣圖來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737f72014929065bc63ec9c6021b05e38799d06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112860"
---
# <a name="how-to-scale-a-bitmap-source"></a><span data-ttu-id="ce9c2-103">如何調整點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="ce9c2-103">How to Scale a Bitmap Source</span></span>

<span data-ttu-id="ce9c2-104">本主題示範如何使用 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)元件來調整 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-104">This topic demonstrates how to scale an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) using the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) component.</span></span>

<span data-ttu-id="ce9c2-105">調整點陣圖來源</span><span class="sxs-lookup"><span data-stu-id="ce9c2-105">To scale a bitmap source</span></span>

1.  <span data-ttu-id="ce9c2-106">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 物件，以建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-106">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) object to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  <span data-ttu-id="ce9c2-107">使用 [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) 方法從影像檔案建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-107">Use the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from an image file.</span></span>

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;
    IWICBitmapScaler *pIScaler = NULL;


    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  <span data-ttu-id="ce9c2-108">取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-108">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="ce9c2-109">JPEG 檔案格式只支援單一框架。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-109">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="ce9c2-110">因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-110">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="ce9c2-111">若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-111">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

4.  <span data-ttu-id="ce9c2-112">建立要用於影像縮放的 [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) 。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-112">Create the [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) to use for the image scaling.</span></span>

    ```C++
    // Create the scaler.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapScaler(&pIScaler);
    }
    ```

    

5.  <span data-ttu-id="ce9c2-113">使用點陣圖框架的影像資料，以大小一半的方式初始化 scaler 物件。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-113">Initialize the scaler object with the image data of the bitmap frame at half the size.</span></span>

    ```C++
    // Initialize the scaler to half the size of the original source.
    if (SUCCEEDED(hr))
    {
       hr = pIScaler->Initialize(
          pIDecoderFrame,                    // Bitmap source to scale.
          uiWidth/2,                         // Scale width to half of original.
          uiHeight/2,                        // Scale height to half of original.
          WICBitmapInterpolationModeFant);   // Use Fant mode interpolation.
    }
    ```

    

6.  <span data-ttu-id="ce9c2-114">繪製或處理縮放點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-114">Draw or process the scaled bitmap source.</span></span>

    <span data-ttu-id="ce9c2-115">下圖將示範映射調整。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-115">The following illustration demonstrates imaging scaling.</span></span> <span data-ttu-id="ce9c2-116">左邊的原始影像是 200 x 130 圖元。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-116">The original image on the left is 200 x 130 pixels.</span></span> <span data-ttu-id="ce9c2-117">右邊的影像是調整為大小一半的原始影像。</span><span class="sxs-lookup"><span data-stu-id="ce9c2-117">The image on the right is the original image scaled to half the size.</span></span>

    ![顯示如何將影像調整為較小大小的圖例](graphics/scaledregion.png)

## <a name="see-also"></a><span data-ttu-id="ce9c2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce9c2-119">See Also</span></span>

[<span data-ttu-id="ce9c2-120">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="ce9c2-120">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="ce9c2-121">參考</span><span class="sxs-lookup"><span data-stu-id="ce9c2-121">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="ce9c2-122">範例</span><span class="sxs-lookup"><span data-stu-id="ce9c2-122">Samples</span></span>](-wic-samples.md)


 

 



