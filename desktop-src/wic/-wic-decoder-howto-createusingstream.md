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
# <a name="how-to-create-a-decoder-using-a-stream"></a><span data-ttu-id="e41c7-103">如何使用資料流程建立解碼器</span><span class="sxs-lookup"><span data-stu-id="e41c7-103">How to Create a Decoder Using a Stream</span></span>

<span data-ttu-id="e41c7-104">本主題說明如何使用資料流程建立點陣圖解碼器。</span><span class="sxs-lookup"><span data-stu-id="e41c7-104">This topic describes how to create a bitmap decoder by using a stream.</span></span>

<span data-ttu-id="e41c7-105">使用資料流程建立點陣圖解碼</span><span class="sxs-lookup"><span data-stu-id="e41c7-105">To create a bitmap decoder by using a stream</span></span>

1.  <span data-ttu-id="e41c7-106">將影像檔載入資料流程中。</span><span class="sxs-lookup"><span data-stu-id="e41c7-106">Load an image file into a stream.</span></span> <span data-ttu-id="e41c7-107">在此範例中，會建立應用程式資源的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e41c7-107">In this example, a stream is created for an application resource.</span></span>

    <span data-ttu-id="e41c7-108">在應用程式資源定義 ( .rc) 檔案中，定義資源。</span><span class="sxs-lookup"><span data-stu-id="e41c7-108">In the application resource definition (.rc) file, define the resource.</span></span> <span data-ttu-id="e41c7-109">下列範例會定義 `Image` 名為的資源 `IDR_SAMPLE_IMAGE` 。</span><span class="sxs-lookup"><span data-stu-id="e41c7-109">The following example defines an `Image` resource named `IDR_SAMPLE_IMAGE`.</span></span>

    ```C++
    IDR_SAMPLE_IMAGE IMAGE "turtle.jpg"
    ```

    

    <span data-ttu-id="e41c7-110">建立應用程式時，會將資源新增至應用程式的資源。</span><span class="sxs-lookup"><span data-stu-id="e41c7-110">The resource will be added to the application's resources when the application is built.</span></span>

2.  <span data-ttu-id="e41c7-111">從應用程式載入資源。</span><span class="sxs-lookup"><span data-stu-id="e41c7-111">Load the resource from the application.</span></span>

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

    

3.  <span data-ttu-id="e41c7-112">鎖定資源並取得大小。</span><span class="sxs-lookup"><span data-stu-id="e41c7-112">Lock the resource and get the size.</span></span>

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

    

4.  <span data-ttu-id="e41c7-113">建立 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) 來建立 WINDOWS 影像處理元件 (WIC) 物件。</span><span class="sxs-lookup"><span data-stu-id="e41c7-113">Create an [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) to create Windows Imaging Component (WIC) objects.</span></span>

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

5.  <span data-ttu-id="e41c7-114">使用 [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) 方法來建立 [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) 物件，並使用映射記憶體指標將它初始化。</span><span class="sxs-lookup"><span data-stu-id="e41c7-114">Use the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method to create an [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object and initialize it by using the image memory pointer.</span></span>

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

    

6.  <span data-ttu-id="e41c7-115">使用 [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法，從新的資料流程物件建立 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 。</span><span class="sxs-lookup"><span data-stu-id="e41c7-115">Create an [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) from the new stream object using the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

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

    

7.  <span data-ttu-id="e41c7-116">取得映射的第一個 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="e41c7-116">Get the first [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) of the image.</span></span>

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    <span data-ttu-id="e41c7-117">JPEG 檔案格式只支援單一框架。</span><span class="sxs-lookup"><span data-stu-id="e41c7-117">The JPEG file format only supports a single frame.</span></span> <span data-ttu-id="e41c7-118">因為此範例中的檔案是 JPEG 檔案，所以會使用第一個框架 (`0`) 。</span><span class="sxs-lookup"><span data-stu-id="e41c7-118">Because the file in this example is a JPEG file, the first frame (`0`) is used.</span></span> <span data-ttu-id="e41c7-119">若為具有多個框架的影像格式，請參閱 [如何取出影像的框架](-wic-bitmapsources-howto-retrieveimageframes.md) 以存取影像的每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="e41c7-119">For image formats that have multiple frames, see [How to Retrieve the Frames of an Image](-wic-bitmapsources-howto-retrieveimageframes.md) for accessing each frame of the image.</span></span>

8.  <span data-ttu-id="e41c7-120">處理影像框架。</span><span class="sxs-lookup"><span data-stu-id="e41c7-120">Process the image frame.</span></span> <span data-ttu-id="e41c7-121">如需 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件的詳細資訊，請參閱 [點陣圖來源總覽](-wic-bitmapsources.md)。</span><span class="sxs-lookup"><span data-stu-id="e41c7-121">For additional information about [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) objects, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e41c7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e41c7-122">See Also</span></span>

[<span data-ttu-id="e41c7-123">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="e41c7-123">Programming Guide</span></span>](-wic-programming-guide.md)


[<span data-ttu-id="e41c7-124">參考</span><span class="sxs-lookup"><span data-stu-id="e41c7-124">Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="e41c7-125">範例</span><span class="sxs-lookup"><span data-stu-id="e41c7-125">Samples</span></span>](-wic-samples.md)


 

 



