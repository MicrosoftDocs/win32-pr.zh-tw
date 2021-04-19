---
description: 下列範例示範如何將影像和其中繼資料重新編碼為相同格式的新檔案。
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: 如何使用中繼資料重新編碼 JPEG 影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "106986778"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a><span data-ttu-id="bf4a2-103">如何使用中繼資料重新編碼 JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="bf4a2-103">How-to re-encode a JPEG image with metadata</span></span>

<span data-ttu-id="bf4a2-104">下列範例示範如何將影像和其中繼資料重新編碼為相同格式的新檔案。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-104">The following example demonstrates how to re-encode an image and its metadata to a new file of the same format.</span></span> <span data-ttu-id="bf4a2-105">此外，這個範例會加入中繼資料來示範查詢寫入器所使用的單一專案運算式。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-105">In addition, this example adds metadata to demonstrate a single-item expression used by a query writer.</span></span>

<span data-ttu-id="bf4a2-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bf4a2-107">先決條件</span><span class="sxs-lookup"><span data-stu-id="bf4a2-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="bf4a2-108">第1部分：將影像解碼</span><span class="sxs-lookup"><span data-stu-id="bf4a2-108">Part 1: Decode an Image</span></span>](#part-1-decode-an-image)
-   [<span data-ttu-id="bf4a2-109">第2部分：建立和初始化影像編碼器</span><span class="sxs-lookup"><span data-stu-id="bf4a2-109">Part 2: Create and Initialize the Image Encoder</span></span>](#part-2-create-and-initialize-the-image-encoder)
-   [<span data-ttu-id="bf4a2-110">第3部分：複製已解碼的框架資訊</span><span class="sxs-lookup"><span data-stu-id="bf4a2-110">Part 3: Copy Decoded Frame Information</span></span>](#part-3-copy-decoded-frame-information)
-   [<span data-ttu-id="bf4a2-111">第4部分：複製中繼資料</span><span class="sxs-lookup"><span data-stu-id="bf4a2-111">Part 4: Copy the Metadata</span></span>](#part-4-copy-the-metadata)
-   [<span data-ttu-id="bf4a2-112">第5部分：新增額外的中繼資料</span><span class="sxs-lookup"><span data-stu-id="bf4a2-112">Part 5: Add Additional Metadata</span></span>](#part-5-add-additional-metadata)
-   [<span data-ttu-id="bf4a2-113">第6部分：完成編碼的影像</span><span class="sxs-lookup"><span data-stu-id="bf4a2-113">Part 6: Finalize the Encoded Image</span></span>](#part-6-finalize-the-encoded-image)
-   [<span data-ttu-id="bf4a2-114">JPEG 重新編碼範例程式碼</span><span class="sxs-lookup"><span data-stu-id="bf4a2-114">JPEG Re-encode Example Code</span></span>](#jpeg-re-encode-example-code)
-   [<span data-ttu-id="bf4a2-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf4a2-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="bf4a2-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="bf4a2-116">Prerequisites</span></span>

<span data-ttu-id="bf4a2-117">若要瞭解本主題，您應該熟悉 [Wic 中繼資料總覽](-wic-about-metadata.md)中所述的 WINDOWS 影像處理元件 (wic) 中繼資料系統。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-117">To understand this topic, you should be familiar with the Windows Imaging Component (WIC) metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="bf4a2-118">您也應該熟悉 WIC 編解碼器元件，如 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-118">You should also be familiar with the WIC codec components as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="part-1-decode-an-image"></a><span data-ttu-id="bf4a2-119">第1部分：將影像解碼</span><span class="sxs-lookup"><span data-stu-id="bf4a2-119">Part 1: Decode an Image</span></span>

<span data-ttu-id="bf4a2-120">在您可以將影像資料或中繼資料複製到新的影像檔案之前，您必須先為要重新編碼的現有映射建立一個解碼器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-120">Before you can copy image data or metadata to a new image file, you must first create a decoder for the existing image that you want to re-encode.</span></span> <span data-ttu-id="bf4a2-121">下列程式碼示範如何為影像檔案 test.jpg 建立 WIC 解碼器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-121">The following code demonstrates how to create a WIC decoder for the image file test.jpg.</span></span>


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



<span data-ttu-id="bf4a2-122">對 **CreateDecoderFromFilename** 的呼叫會使用 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 列舉中 WICDecodeMetadataCacheOnDemand 的值做為第四個參數。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-122">The call to **CreateDecoderFromFilename** used the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration as the fourth parameter.</span></span> <span data-ttu-id="bf4a2-123">這會告知解碼器在需要中繼資料時快取中繼資料，方法是取得查詢讀取器，或使用基礎中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-123">This tells the decoder to cache the metadata when the metadata is needed, either by obtaining a query reader or by using the underlying metadata reader.</span></span> <span data-ttu-id="bf4a2-124">使用這個選項可讓您將資料流程保留在中繼資料中，這是執行快速中繼資料編碼的必要項，並且可讓 JPEG 影像進行不失真的解碼和編碼。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-124">Using this option enables you to retain the stream to the metadata, which is required for performing fast metadata encoding and enables lossless decoding and encoding of JPEG images.</span></span> <span data-ttu-id="bf4a2-125">或者，您可以使用其他 **WICDecodeOptions** 值 WICDecodeMetadataCacheOnLoad，這會在載入映射時立即快取內嵌影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-125">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

## <a name="part-2-create-and-initialize-the-image-encoder"></a><span data-ttu-id="bf4a2-126">第2部分：建立和初始化影像編碼器</span><span class="sxs-lookup"><span data-stu-id="bf4a2-126">Part 2: Create and Initialize the Image Encoder</span></span>

<span data-ttu-id="bf4a2-127">下列程式碼示範如何建立您將用來編碼先前解碼之影像的編碼器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-127">The following code demonstrates the creation of the encoder you will use to encode the image you previously decoded.</span></span>


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



<span data-ttu-id="bf4a2-128">建立並初始化 WIC 檔案資料流程 piFileStream，以寫入影像檔案 "test2.jpg"。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-128">A WIC file stream piFileStream is created and initialized for writing to the image file "test2.jpg".</span></span> <span data-ttu-id="bf4a2-129">接著會使用 piFileStream 來初始化編碼器，並通知編碼器在編碼完成時寫入影像位的位置。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-129">piFileStream is then used to initialize the encoder, informing the encoder where to write the image bits when the encoding is complete.</span></span>

## <a name="part-3-copy-decoded-frame-information"></a><span data-ttu-id="bf4a2-130">第3部分：複製已解碼的框架資訊</span><span class="sxs-lookup"><span data-stu-id="bf4a2-130">Part 3: Copy Decoded Frame Information</span></span>

<span data-ttu-id="bf4a2-131">下列程式碼會將影像的每個畫面格複製到編碼器的新畫面。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-131">The following code copies each frame of an image to a new frame of the encoder.</span></span> <span data-ttu-id="bf4a2-132">此複本包含大小、解析度和像素格式;所有這些都是建立有效框架的必要項。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-132">This copy includes size, resolution, and pixel format; all of which are necessary to create a valid frame.</span></span>

> [!Note]  
> <span data-ttu-id="bf4a2-133">JPEG 影像只會有一個畫面格，而且下面的迴圈並不是必要的，但也會納入以示範支援它之格式的多重畫面使用方式。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-133">JPEG images will only have one frame and the loop below is not technically necessary but is included to demonstrate multi-frame usage for formats that support it.</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



<span data-ttu-id="bf4a2-134">下列程式碼會執行快速檢查，以判斷來源和目的地影像格式是否相同。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-134">The following code performs a quick check to determine whether the source and destination image formats are the same.</span></span> <span data-ttu-id="bf4a2-135">這是必要的，因為第4部分所顯示的作業只有在來源和目的地格式相同時才受支援。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-135">This is needed as Part 4 shows an operation that is only supported when the source and destination format are the same.</span></span>


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a><span data-ttu-id="bf4a2-136">第4部分：複製中繼資料</span><span class="sxs-lookup"><span data-stu-id="bf4a2-136">Part 4: Copy the Metadata</span></span>

> [!Note]  
> <span data-ttu-id="bf4a2-137">此區段中的程式碼只有在來源和目的影像格式相同時才有效。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-137">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="bf4a2-138">編碼為不同的影像格式時，無法在單一作業中複製映射的所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-138">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="bf4a2-139">若要在將影像重新編碼為相同的影像格式時保留中繼資料，有方法可在單一作業中複製所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-139">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="bf4a2-140">這些作業都遵循類似的模式;每個都會將已解碼的框架中繼資料直接設定為所編碼的新框架。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-140">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span> <span data-ttu-id="bf4a2-141">請注意，這是針對每個個別的影像框架進行的。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-141">Note that this is done for each individual image frame.</span></span>

<span data-ttu-id="bf4a2-142">複製中繼資料的慣用方法是使用已解碼框架的區塊讀取器來初始化新框架的區塊寫入器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-142">The preferred method for copying metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="bf4a2-143">下列程式碼示範這個方法。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-143">The following code demonstrates this method.</span></span>


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



<span data-ttu-id="bf4a2-144">在此範例中，您只需從來源畫面格和目的框架分別取得區塊讀取器和封鎖寫入器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-144">In this example, you simply obtain the block reader and block writer from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="bf4a2-145">區塊寫入器接著會從封鎖讀取器初始化。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-145">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="bf4a2-146">這會以封鎖讀取器預先填入的中繼資料初始化區塊寫入器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-146">This initializes the block writer with the pre-populated metadata of the block reader.</span></span> <span data-ttu-id="bf4a2-147">若要瞭解複製中繼資料的其他方法，請參閱 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)中的寫入中繼資料一節。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-147">To learn additional methods for copying metadata, see the Writing Metadata section in the [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="bf4a2-148">同樣地，此作業只適用于來源和目的映射具有相同的格式時。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-148">Again, this operation works only when the source and destination images have the same format.</span></span> <span data-ttu-id="bf4a2-149">這是因為不同的影像格式會將中繼資料區塊儲存在不同的位置。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-149">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="bf4a2-150">例如，JPEG 和標記的影像檔案格式 (TIFF) 支援可延伸的中繼資料平臺 (XMP) 中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-150">For instance, both JPEG and Tagged Image File Format (TIFF) support Extensible Metadata Platform (XMP) metadata blocks.</span></span> <span data-ttu-id="bf4a2-151">在 JPEG 影像中，XMP 區塊位於「 [WIC 中繼資料」總覽](-wic-about-metadata.md)中所述的根中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-151">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="bf4a2-152">不過，在 TIFF 影像中，XMP 區塊內嵌于根的 IFD 區塊中。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-152">However, in a TIFF image, the XMP block is embedded in the root IFD block.</span></span>

## <a name="part-5-add-additional-metadata"></a><span data-ttu-id="bf4a2-153">第5部分：新增額外的中繼資料</span><span class="sxs-lookup"><span data-stu-id="bf4a2-153">Part 5: Add Additional Metadata</span></span>

<span data-ttu-id="bf4a2-154">下列範例示範如何將中繼資料新增至目的映射。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-154">The following example demonstrates how to add metadata to the destination image.</span></span> <span data-ttu-id="bf4a2-155">這是藉由使用查詢運算式和儲存在 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)中的資料呼叫查詢寫入器的 **SetMetadataByName** 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-155">This is done by calling the query writer's **SetMetadataByName** method using a query expression and the data stored in a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span>


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



<span data-ttu-id="bf4a2-156">如需查詢運算式的詳細資訊，請參閱 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-156">For more information on the query expression, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="part-6-finalize-the-encoded-image"></a><span data-ttu-id="bf4a2-157">第6部分：完成編碼的影像</span><span class="sxs-lookup"><span data-stu-id="bf4a2-157">Part 6: Finalize the Encoded Image</span></span>

<span data-ttu-id="bf4a2-158">複製映射的最後步驟是撰寫框架的圖元資料、將畫面格認可至編碼器，以及認可編碼器。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-158">The final steps for copying the image are to write the pixel data for the frame, commit the frame to the encoder, and commit the encoder.</span></span> <span data-ttu-id="bf4a2-159">認可編碼器會將影像串流寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-159">Committing the encoder writes the image stream to the file.</span></span>


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



<span data-ttu-id="bf4a2-160">框架的 **WriteSource** 方法是用來寫入影像的圖元資料。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-160">The frame's **WriteSource** method is used to write the pixel data for the image.</span></span> <span data-ttu-id="bf4a2-161">請注意，這是在寫入中繼資料之後完成的。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-161">Note that this is done after the metadata has been written.</span></span> <span data-ttu-id="bf4a2-162">這是必要的，以確保中繼資料在影像檔案內有足夠的空間。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-162">This is necessary to ensure that the metadata has enough space within the image file.</span></span> <span data-ttu-id="bf4a2-163">寫入圖元資料之後，會使用框架的 **Commit** 方法將框架寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-163">After the pixel data is written, the frame is written to the stream using the frame's **Commit** method.</span></span> <span data-ttu-id="bf4a2-164">處理完所有框架之後，編碼器 (，因此會使用編碼器的 **Commit** 方法來完成映射) 。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-164">After all frames have been processed, the encoder (and thus the image) is finalized using the encoder's **Commit** method.</span></span>

<span data-ttu-id="bf4a2-165">認可框架之後，您必須釋放在迴圈中建立的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-165">Once you commit the frame, you must release the COM objects created in the loop.</span></span>

## <a name="jpeg-re-encode-example-code"></a><span data-ttu-id="bf4a2-166">JPEG 重新編碼範例程式碼</span><span class="sxs-lookup"><span data-stu-id="bf4a2-166">JPEG Re-encode Example Code</span></span>

<span data-ttu-id="bf4a2-167">以下是一個 convienient 區塊中第1到6部分的程式碼。</span><span class="sxs-lookup"><span data-stu-id="bf4a2-167">The following is the code from Parts 1 through 6 in one convienient block.</span></span>


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="bf4a2-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf4a2-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bf4a2-169">**概念**</span><span class="sxs-lookup"><span data-stu-id="bf4a2-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bf4a2-170">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="bf4a2-170">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="bf4a2-171">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="bf4a2-171">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="bf4a2-172">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="bf4a2-172">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="bf4a2-173">中繼資料擴充性總覽</span><span class="sxs-lookup"><span data-stu-id="bf4a2-173">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
