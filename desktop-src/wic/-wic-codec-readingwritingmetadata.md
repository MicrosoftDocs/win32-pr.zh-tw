---
description: 本主題概要說明如何使用 Windows 影像處理元件 (WIC) Api 來讀取和寫入內嵌于影像檔案的中繼資料。
ms.assetid: b1e0b936-a13a-42dd-8470-957ba1d90423
title: 讀取和寫入影像中繼資料的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 484d562b71184c20adf054f1de2a4203878da9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944439"
---
# <a name="overview-of-reading-and-writing-image-metadata"></a><span data-ttu-id="ad9ad-103">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="ad9ad-103">Overview of Reading and Writing Image Metadata</span></span>

<span data-ttu-id="ad9ad-104">本主題概要說明如何使用 Windows 影像處理元件 (WIC) Api 來讀取和寫入內嵌于影像檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-104">This topic provides an overview of how you can use the Windows Imaging Component (WIC) APIs to read and write metadata that is embedded in image files.</span></span>

<span data-ttu-id="ad9ad-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ad9ad-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="ad9ad-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="ad9ad-107">簡介</span><span class="sxs-lookup"><span data-stu-id="ad9ad-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ad9ad-108">使用查詢讀取器讀取 Metadadata</span><span class="sxs-lookup"><span data-stu-id="ad9ad-108">Reading Metadadata Using a Query Reader</span></span>](#reading-metadadata-using-a-query-reader)
    -   [<span data-ttu-id="ad9ad-109">取得查詢讀取器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-109">Obtaining a Query Reader</span></span>](#obtaining-a-query-reader)
    -   [<span data-ttu-id="ad9ad-110">讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-110">Reading Metadata</span></span>](#reading-metadata)
    -   [<span data-ttu-id="ad9ad-111">其他查詢讀取器方法</span><span class="sxs-lookup"><span data-stu-id="ad9ad-111">Additional Query Reader Methods</span></span>](#additional-query-reader-methods)
-   [<span data-ttu-id="ad9ad-112">使用查詢寫入器撰寫中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-112">Writing Metadata Using a Query Writer</span></span>](#writing-metadata-using-a-query-writer)
    -   [<span data-ttu-id="ad9ad-113">取得查詢寫入器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-113">Obtaining a Query Writer</span></span>](#obtaining-a-query-writer)
    -   [<span data-ttu-id="ad9ad-114">新增中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-114">Adding Metadata</span></span>](#adding-metadata)
    -   [<span data-ttu-id="ad9ad-115">移除中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-115">Removing Metadata</span></span>](#removing-metadata)
    -   [<span data-ttu-id="ad9ad-116">複製重新編碼的中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-116">Copying Metadata for Re-encoding</span></span>](#copying-metadata-for-re-encoding)
-   [<span data-ttu-id="ad9ad-117">快速中繼資料編碼</span><span class="sxs-lookup"><span data-stu-id="ad9ad-117">Fast Metadata Encoding</span></span>](#fast-metadata-encoding)
    -   [<span data-ttu-id="ad9ad-118">將填補加入中繼資料區塊</span><span class="sxs-lookup"><span data-stu-id="ad9ad-118">Adding Padding to Metadata Blocks</span></span>](#adding-padding-to-metadata-blocks)
    -   [<span data-ttu-id="ad9ad-119">取得快速中繼資料編碼器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-119">Obtaining a Fast Metadata Encoder</span></span>](#obtaining-a-fast-metadata-encoder)
    -   [<span data-ttu-id="ad9ad-120">使用快速中繼資料編碼器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-120">Using the Fast Metadata Encoder</span></span>](#using-the-fast-metadata-encoder)
-   [<span data-ttu-id="ad9ad-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad9ad-121">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="ad9ad-122">必要條件</span><span class="sxs-lookup"><span data-stu-id="ad9ad-122">Prerequisites</span></span>

<span data-ttu-id="ad9ad-123">若要瞭解本主題，您應該熟悉 wic 中繼資料系統（如 [Wic 中繼資料總覽](-wic-about-metadata.md)中所述）。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-123">To understand this topic, you should be familiar with the WIC metadata system as described in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ad9ad-124">您也應該熟悉用來讀取和寫入中繼資料的查詢語言，如 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-124">You should also be familiar with the query language used to read and write metadata, as described in [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="ad9ad-125">簡介</span><span class="sxs-lookup"><span data-stu-id="ad9ad-125">Introduction</span></span>

<span data-ttu-id="ad9ad-126">WIC 為應用程式開發人員提供元件物件模型 (COM) 元件，以讀取和寫入內嵌在影像檔中的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-126">WIC provides application developers with Component Object Model (COM) components to read and write metadata embedded in image files.</span></span> <span data-ttu-id="ad9ad-127">有兩種方式可以讀取和寫入中繼資料：</span><span class="sxs-lookup"><span data-stu-id="ad9ad-127">There are two ways to read and write metadata:</span></span>

-   <span data-ttu-id="ad9ad-128">使用查詢讀取器/寫入器和查詢運算式來查詢區塊內的嵌套區塊或特定中繼資料的中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-128">Using a query reader/writer and a query expression to query metadata blocks for nested blocks or specific metadata within a block.</span></span>
-   <span data-ttu-id="ad9ad-129">使用元資料處理程式 (中繼資料讀取器或中繼資料寫入器) 來存取中繼資料區塊內的嵌套中繼資料區塊或特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-129">Using a metadata handler (a metadata reader or a metadata writer) to access the nested metadata blocks or specific metadata within the metadata blocks.</span></span>

<span data-ttu-id="ad9ad-130">最簡單的方法是使用查詢讀取器/寫入器和查詢運算式來存取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-130">The easiest of these is to use a query reader/writer and a query expression to access the metadata.</span></span> <span data-ttu-id="ad9ad-131">查詢讀取器 ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) 用來讀取中繼資料，而查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 用來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-131">A query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) is used to read metadata while a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used to write metadata.</span></span> <span data-ttu-id="ad9ad-132">這兩種都使用查詢運算式來讀取或寫入所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-132">Both of these use a query expression to read or write the desired metadata.</span></span> <span data-ttu-id="ad9ad-133">在幕後，查詢讀取器 (和寫入器) 會使用元資料處理程式來存取查詢運算式所描述的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-133">Behind the scenes, a query reader (and writer) uses a metadata handler to access the metadata described by the query expression.</span></span>

<span data-ttu-id="ad9ad-134">更先進的方法是直接存取元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-134">The more advanced method is to directly access the metadata handlers.</span></span> <span data-ttu-id="ad9ad-135">使用區塊讀取器 ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) 或區塊寫入器 ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) ，從個別的框架取得元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-135">A metadata handler is obtained from the individual frames using a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) or a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).</span></span> <span data-ttu-id="ad9ad-136">可用的元資料處理程式有兩種類型：中繼資料讀取器 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 和中繼資料寫入器 ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-136">The two types of metadata handlers available are the metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) and the metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)).</span></span>

<span data-ttu-id="ad9ad-137">本主題的整個範例都會使用 JPEG 影像檔案的下圖。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-137">The following diagram of the contents of a JPEG image file is used throughout the examples in this topic.</span></span> <span data-ttu-id="ad9ad-138">此圖表表示的影像是使用 Microsoft 小畫家建立的;評等中繼資料是使用 Windows Vista 的影像中心功能新增的。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-138">The image represented by this diagram was created by using Microsoft Paint; the rating metadata was added by using the Photo Gallery feature of Windows Vista.</span></span>

![包含評等中繼資料之 jpeg 影像的圖例](graphics/jpeg.png)

## <a name="reading-metadadata-using-a-query-reader"></a><span data-ttu-id="ad9ad-140">使用查詢讀取器讀取 Metadadata</span><span class="sxs-lookup"><span data-stu-id="ad9ad-140">Reading Metadadata Using a Query Reader</span></span>

<span data-ttu-id="ad9ad-141">讀取中繼資料最簡單的方式是使用查詢讀取器介面 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-141">The easiest way to read metadata is to use the query reader interface, [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader).</span></span> <span data-ttu-id="ad9ad-142">查詢讀取器可讓您使用查詢運算式，讀取中繼資料區塊內的中繼資料區塊和專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-142">The query reader enables you to read metadata blocks and items within metadata blocks using a query expression.</span></span>

<span data-ttu-id="ad9ad-143">取得查詢讀取器的方法有三種：透過點陣圖解碼 ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)) 、透過其個別的框架 ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) ，或透過查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-143">There are three ways to obtain a query reader: through a bitmap decoder ([**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)), through its individual frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)), or through a query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span>

### <a name="obtaining-a-query-reader"></a><span data-ttu-id="ad9ad-144">取得查詢讀取器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-144">Obtaining a Query Reader</span></span>

<span data-ttu-id="ad9ad-145">下列範例程式碼示範如何從影像處理站取得點陣圖解碼器，以及取得個別點陣圖框架。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-145">The following example code shows how to obtain a bitmap decoder from the imaging factory and retrieve an individual bitmap frame.</span></span> <span data-ttu-id="ad9ad-146">這段程式碼也會執行從已解碼的框架取得查詢讀取器所需的設定工作。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-146">This code also performs setup work needed to obtain a query reader from a decoded frame.</span></span>


```
IWICImagingFactory *pFactory = NULL;
IWICBitmapDecoder *pDecoder = NULL;
IWICBitmapFrameDecode *pFrameDecode = NULL;
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pEmbedReader = NULL;
PROPVARIANT value;

// Initialize COM
CoInitialize(NULL);

// Initialize PROPVARIANT
PropVariantInit(&value);

//Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_IWICImagingFactory,
    (LPVOID*)&pFactory);

// Create the decoder
if (SUCCEEDED(hr))
{
    hr = pFactory->CreateDecoderFromFilename(
        L"test.jpg",
        NULL,
        GENERIC_READ,
        WICDecodeMetadataCacheOnDemand,
        &pDecoder);
}

// Get a single frame from the image
if (SUCCEEDED(hr))
{
    hr = pDecoder->GetFrame(
         0,  //JPEG has only one frame.
         &pFrameDecode); 
}
```



<span data-ttu-id="ad9ad-147">您可以使用映射處理站的 **CreateDecoderFromFilename** 方法，取得 test.jpg 檔案的點陣圖解碼器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-147">The bitmap decoder for the test.jpg file is obtained by using the **CreateDecoderFromFilename** method of the imaging factory.</span></span> <span data-ttu-id="ad9ad-148">在這個方法中，第四個參數會設定為從 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 列舉 WICDecodeMetadataCacheOnDemand 的值。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-148">In this method, the fourth parameter is set to the value WICDecodeMetadataCacheOnDemand from the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) enumeration.</span></span> <span data-ttu-id="ad9ad-149">這會告知解碼器在需要中繼資料時快取中繼資料;您可以藉由取得查詢讀取器或基礎中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-149">This tells the decoder to cache the metadata when the metadata is needed; either by obtaining a query reader or the underlying metadata reader.</span></span> <span data-ttu-id="ad9ad-150">使用這個選項可讓您將資料流程保留給快速中繼資料編碼所需的中繼資料，並啟用 JPEG 影像的不失真解碼。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-150">Using this option enables you to retain the stream to the metadata required for fast metadata encoding and enables lossless decoding of the JPEG image.</span></span> <span data-ttu-id="ad9ad-151">或者，您可以使用其他 **WICDecodeOptions** 值 WICDecodeMetadataCacheOnLoad，這會在載入映射時立即快取內嵌影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-151">Alternatively, you could use the other **WICDecodeOptions** value, WICDecodeMetadataCacheOnLoad, which caches the embedded image metadata as soon as the image is loaded.</span></span>

<span data-ttu-id="ad9ad-152">若要取得框架的查詢讀取器，請對框架的 **GetMetadataQueryReader** 方法進行簡單的呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-152">To obtain the frame's query reader, make a simple call to the frame's **GetMetadataQueryReader** method.</span></span> <span data-ttu-id="ad9ad-153">下列程式碼示範此呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-153">The following code demonstrates this call.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="ad9ad-154">同樣地，也可以在解碼器層級取得查詢讀取器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-154">Similarly, a query reader can also be obtained at the decoder level.</span></span> <span data-ttu-id="ad9ad-155">對解碼器的 **GetMetadataQueryReader** 方法進行簡單的呼叫，會取得該解碼器的查詢讀取器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-155">A simple call to the decoder's **GetMetadataQueryReader** method gets the decoder's query reader.</span></span> <span data-ttu-id="ad9ad-156">與框架的查詢讀取器不同的是，相較于框架的查詢讀取器，它會讀取個別畫面格以外的影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-156">An decoder's query reader, unlike a frame's query reader, reads metadata for an image that is outside of the individual frames.</span></span> <span data-ttu-id="ad9ad-157">不過，此案例並不常見，原生映射格式不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-157">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ad9ad-158">在框架層級，WIC 讀取和寫入中繼資料所提供的原生映射編解碼器，甚至是針對單一框架格式（例如 JPEG）。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-158">The native image CODECS provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

### <a name="reading-metadata"></a><span data-ttu-id="ad9ad-159">讀取中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-159">Reading Metadata</span></span>

<span data-ttu-id="ad9ad-160">在您繼續實際讀取中繼資料之前，請查看下列 JPEG 檔案的圖表，其中包含內嵌的中繼資料區塊，以及要取出的實際資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-160">Before you move on to actually reading metadata, look at the following diagram of a JPEG file that includes embedded metadata blocks and actual data to retrieve.</span></span> <span data-ttu-id="ad9ad-161">此圖表提供在影像內的特定中繼資料區塊和專案的標注，提供每個區塊或專案的中繼資料查詢運算式。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-161">This diagram provides callouts to specific metadata blocks and items within the image providing the metadata query expression to each block or item.</span></span>

![具有中繼資料標注之 jpeg 影像的圖例](graphics/jpegwithcallouts.png)

<span data-ttu-id="ad9ad-163">若要依名稱查詢內嵌的中繼資料區塊或特定專案，請呼叫 **GetMetadataByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-163">To query for embedded metadata blocks or specific items by name, call the **GetMetadataByName** method.</span></span> <span data-ttu-id="ad9ad-164">這個方法會採用查詢運算式和傳回中繼資料專案的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-164">This method takes a query expression and a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) in which the metadata item is returned.</span></span> <span data-ttu-id="ad9ad-165">下列程式碼會查詢嵌套的中繼資料區塊，並將 PROPVARIANT 值所提供的 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) 元件轉換成查詢讀取器（如果有找到）。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-165">The following code queries for a nested metadata block and converts the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) component provided by the PROPVARIANT value to a query reader if found.</span></span>


```
if (SUCCEEDED(hr))
{
    // Get the nested IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ad9ad-166">查詢運算式 "/app1/ifd" 正在查詢 App1 區塊中嵌套的 IFD 區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-166">The query expression "/app1/ifd" is querying for the IFD block nested in the App1 block.</span></span> <span data-ttu-id="ad9ad-167">JPEG 影像檔案包含 IFD 的嵌套中繼資料區塊，因此[](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)會以 (vt) 的變數類型 `VT_UNKNOWN` 和 (PunkVal) 的[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面指標來傳回 PROPVARIANT。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-167">The JPEG image file contains the IFD nested metadata block, so the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) is returned with a variable type (vt) of `VT_UNKNOWN` and a pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface (punkVal).</span></span> <span data-ttu-id="ad9ad-168">然後，您可以查詢 IUnknown 介面是否有查詢讀取器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-168">You then query the IUnknown interface for a query reader.</span></span>

<span data-ttu-id="ad9ad-169">下列程式碼會根據與嵌套的 IFD 區塊相關的新查詢讀取器，示範新的查詢。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-169">The following code demonstrates a new query based on the new query reader relative to the nested IFD block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetMetadataByName(L"/{ushort=18249}", &value);
    PropVariantClear(&value); // Clear value for new query
}
```



<span data-ttu-id="ad9ad-170">查詢運算式 "/{ushort = 18249}" 會查詢 IFD 區塊，以取得內嵌在標記18249下的 MicrosoftPhoto 評等。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-170">The query expression "/{ushort=18249}" queries the IFD block for the MicrosoftPhoto rating embedded under tag 18249.</span></span> <span data-ttu-id="ad9ad-171">[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)值現在會包含的實值型別 `VT_UI2` 和資料值50。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-171">The [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will now contain a value type of `VT_UI2` and a data value of 50.</span></span>

<span data-ttu-id="ad9ad-172">不過，在查詢特定資料值之前，不需要取得嵌套區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-172">However, it is not necessary to obtain a nested block before querying for specific data values.</span></span> <span data-ttu-id="ad9ad-173">例如，您可以改為使用根中繼資料區塊和下列程式碼中所示的查詢來取得相同的資訊，而不是查詢嵌套的 IFD，然後再查詢 MicrosoftPhoto 評等。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-173">For instance, instead of querying for the nested IFD and then for the MicrosoftPhoto rating, you can instead use the root metadata block and the query shown in the following code to obtain the same information.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```



<span data-ttu-id="ad9ad-174">除了查詢中繼資料區塊中的特定中繼資料專案以外，您也可以列舉中繼資料區塊中的所有中繼資料專案， (不包括) 的嵌套中繼資料區塊中的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-174">In addition to querying for specific metadata items in a metadata block, you can also enumerate all the metadata items in a metadata block (not including metadata items in nested metadata blocks).</span></span> <span data-ttu-id="ad9ad-175">若要列舉目前區塊中的中繼資料專案，請使用查詢讀取器的 **GetEnumeration** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-175">To enumerate the metadata items in the current block, the query reader's **GetEnumeration** method is used.</span></span> <span data-ttu-id="ad9ad-176">這個方法會取得 **IEnumString** 介面，此介面會填入目前區塊中的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-176">This method obtains an **IEnumString** interface populated with the metadata items in the current block.</span></span> <span data-ttu-id="ad9ad-177">例如，下列程式碼會列舉先前取得之嵌套的 IFD 區塊的 XMP 評等和 MicrosoftPhoto 評等。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-177">For example, the following code enumerates the XMP rating and MicrosoftPhoto rating for the nested IFD block that was obtained earlier.</span></span>


```
IEnumString *metadataItems = NULL;

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetEnumerator(&metadataItems);
}
```



<span data-ttu-id="ad9ad-178">如需識別各種影像格式和元資料格式之適當標記的詳細資訊，請參閱 [原生影像格式中繼資料查詢](-wic-native-image-format-metadata-queries.md)。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-178">For more information on identifying appropriate tags for various image formats and metadata formats, see [Native Image Format Metadata Queries](-wic-native-image-format-metadata-queries.md).</span></span>

### <a name="additional-query-reader-methods"></a><span data-ttu-id="ad9ad-179">其他查詢讀取器方法</span><span class="sxs-lookup"><span data-stu-id="ad9ad-179">Additional Query Reader Methods</span></span>

<span data-ttu-id="ad9ad-180">除了讀取中繼資料，您也可以取得有關查詢讀取器的其他資訊，並透過其他方式取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-180">In addition to reading metadata, you can also obtain additional information about the query reader and obtain metadata through other means.</span></span> <span data-ttu-id="ad9ad-181">查詢讀取器提供兩種方法，提供查詢讀取器（ **GetContainerFormat** 和 **GetLocation**）的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-181">The query reader provides two methods that provide information about the query reader, **GetContainerFormat** and **GetLocation**.</span></span>

<span data-ttu-id="ad9ad-182">使用內嵌查詢讀取器時，您可以使用 **GetContainerFormat** 來判斷中繼資料區塊的類型，而且您可以呼叫 **GetLocation** 來取得相對於根中繼資料區塊的路徑。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-182">With the embedded query reader, you can use **GetContainerFormat** to determine the type of metadata block, and you can call **GetLocation** to obtain the path relative to the root metadata block.</span></span> <span data-ttu-id="ad9ad-183">下列程式碼會查詢內嵌查詢讀取器的位置。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-183">The following code queries the embedded query reader for its location.</span></span>


```
// Determine the metadata block format

if (SUCCEEDED(hr))
{
    hr = pEmbedReader->GetContainerFormat(&containerGUID);
}

// Determine the query reader's location
if (SUCCEEDED(hr))
{
    UINT length;
    WCHAR readerNamespace[100];
    hr = pEmbedReader->GetLocation(100, readerNamespace, &length);
}
```



<span data-ttu-id="ad9ad-184">內嵌查詢讀取器的 **GetContainerFormat** 呼叫會傳回 IFD 元資料格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-184">The call to **GetContainerFormat** for the embedded query reader returns the IFD metadata format GUID.</span></span> <span data-ttu-id="ad9ad-185">對 **GetLocation** 的呼叫會傳回 "/app1/ifd" 的命名空間;為您提供將執行後續查詢來執行新查詢讀取器的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-185">The call to **GetLocation** returns a namespace of "/app1/ifd"; providing you with the relative path from which subsequent queries to the new query reader will be executed.</span></span> <span data-ttu-id="ad9ad-186">當然，上述程式碼並沒有什麼用處，但它確實會示範如何使用 **GetLocation** 方法來尋找嵌套的中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-186">Of course, the preceding code isn't very useful, but it does demonstrate how to use the **GetLocation** method for finding nested metadata blocks.</span></span>

## <a name="writing-metadata-using-a-query-writer"></a><span data-ttu-id="ad9ad-187">使用查詢寫入器撰寫中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-187">Writing Metadata Using a Query Writer</span></span>

> [!Note]  
> <span data-ttu-id="ad9ad-188">本節提供的一些程式碼範例不會顯示在撰寫中繼資料所需的實際步驟內容中。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-188">Some of the code examples provided in this section are not shown in the context of the actual steps required to write metadata.</span></span> <span data-ttu-id="ad9ad-189">若要在工作範例的內容中查看程式碼範例，請參閱 how to：使用中繼資料重新編碼影像教學課程。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-189">To view the code examples in the context of a working sample, see the How-to: Re-encode an Image with Metadata tutorial.</span></span>

 

<span data-ttu-id="ad9ad-190">寫入中繼資料的主要元件是查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-190">The main component for writing metadata is the query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)).</span></span> <span data-ttu-id="ad9ad-191">查詢寫入器可讓您設定和移除中繼資料區塊中的中繼資料區塊和專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-191">The query writer enables you to set and remove metadata blocks and items within a metadata block.</span></span>

<span data-ttu-id="ad9ad-192">如同查詢讀取器，有三種方式可以取得查詢寫入器：透過點陣圖編碼器 ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)) 、透過其個別的框架 ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)) ，或透過快速的中繼資料編碼器 ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-192">Like the query reader, there are three ways to obtain a query writer: through a bitmap encoder ([**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)), through its individual frames ([**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)), or through a fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)).</span></span>

### <a name="obtaining-a-query-writer"></a><span data-ttu-id="ad9ad-193">取得查詢寫入器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-193">Obtaining a Query Writer</span></span>

<span data-ttu-id="ad9ad-194">最常見的查詢寫入器適用于點陣圖的個別框架。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-194">The most common query writer is for an individual frame of a bitmap.</span></span> <span data-ttu-id="ad9ad-195">此查詢寫入器會設定並移除影像框架的中繼資料區塊和專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-195">This query writer sets and removes an image frame's metadata blocks and items.</span></span> <span data-ttu-id="ad9ad-196">若要取得影像框架的查詢寫入器，請呼叫框架的 **GetMetadataQueryWriter** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-196">To obtain an image frame's query writer, call the frame's **GetMetadataQueryWriter** method.</span></span> <span data-ttu-id="ad9ad-197">下列程式碼示範簡單的方法呼叫，以取得框架的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-197">The following code demonstrates the simple method call to obtain a frame's query writer.</span></span>


```
IWICMetadataQueryWriter &pFrameQWriter = NULL;

//Obtain a query writer from the frame.
hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
```



<span data-ttu-id="ad9ad-198">同樣地，也可以取得編碼器層級的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-198">Similarly, a query writer can also be obtained for the encoder level.</span></span> <span data-ttu-id="ad9ad-199">編碼器的 **GetMetadataQueryWriter** 方法的簡單呼叫會取得編碼器的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-199">A simple call to the encoder's **GetMetadataQueryWriter** method gets the encoder's query writer.</span></span> <span data-ttu-id="ad9ad-200">編碼器的查詢寫入器與框架的查詢編寫器不同，它會在個別框架外寫入影像的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-200">An encoder's query writer, unlike a frame's query writer, writes metadata for an image outside of the individual frame.</span></span> <span data-ttu-id="ad9ad-201">不過，此案例並不常見，原生映射格式不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-201">However, this scenario is not common, and the native image formats do not support this capability.</span></span> <span data-ttu-id="ad9ad-202">在框架層級，WIC 讀取和寫入中繼資料所提供的原生映射編解碼器，甚至是針對單一框架格式（例如 JPEG）。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-202">The native image codecs provided by WIC read and write metadata at the frame level even for single-frame formats such as JPEG.</span></span>

<span data-ttu-id="ad9ad-203">您也可以直接從映射處理站取得查詢寫入器 ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)) 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-203">You can also obtain a query writer directly from the imaging factory ([**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)).</span></span> <span data-ttu-id="ad9ad-204">有兩種影像處理站方法會傳回查詢寫入器： **CreateQueryWriter** 和 **CreateQueryWriterFromReader**。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-204">There are two imaging factory methods that return a query writer: **CreateQueryWriter** and **CreateQueryWriterFromReader**.</span></span>

<span data-ttu-id="ad9ad-205">**CreateQueryWriter** 會建立指定之元資料格式和廠商的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-205">**CreateQueryWriter** creates a query writer for the specified metadata format and vendor.</span></span> <span data-ttu-id="ad9ad-206">此查詢寫入器可讓您撰寫特定元資料格式的中繼資料，並將其新增至影像。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-206">This query writer enables you to write metadata for a specific metadata format and add it to the image.</span></span> <span data-ttu-id="ad9ad-207">下列程式碼示範用來建立 XMP 查詢寫入器的 **CreateQueryWriter** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-207">The following code demonstrates a **CreateQueryWriter** call to create an XMP query writer.</span></span>


```
IWICMetadataQueryWriter *pXMPWriter = NULL;

// Create XMP block
GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriter(
        GUID_MetadataFormatXMP,
        &vendor,
        &pXMPWriter);
```



<span data-ttu-id="ad9ad-208">在此範例中，易記名稱 `GUID_MetadataFormatXMP` 會用來做為 *guidMetadataFormat* 參數。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-208">In this example, the friendly name `GUID_MetadataFormatXMP` is used as the *guidMetadataFormat* parameter.</span></span> <span data-ttu-id="ad9ad-209">它代表 XMP 元資料格式 GUID，而廠商則代表 Microsoft 建立的處理常式。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-209">It represents the XMP metadata format GUID, and vendor represents the Microsoft created handler.</span></span> <span data-ttu-id="ad9ad-210">或者，如果沒有其他的 XMP 處理常式存在，則可以使用相同的結果來傳遞 **Null** 作為 *pguidVendor* 參數。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-210">Alternatively, **NULL** can be passed as the *pguidVendor* parameter with the same results if no other XMP handler exists.</span></span> <span data-ttu-id="ad9ad-211">如果自訂的 XMP 處理常式與原生 XMP 處理常式一起安裝，則傳遞 **Null** 給廠商會導致查詢寫入器傳回最小的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-211">If a custom XMP handler is installed alongside the native XMP handler, passing **NULL** for the vendor will result in the query writer with the lowest GUID being returned.</span></span>

<span data-ttu-id="ad9ad-212">**CreateQueryWriterFromReader** 與 **CreateQueryWriter** 方法類似，不同之處在于它會以查詢讀取器所提供的資料會預先填入新的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-212">**CreateQueryWriterFromReader** is similar to the **CreateQueryWriter** method except that it prepopulates the new query writer with the data provided by the query reader.</span></span> <span data-ttu-id="ad9ad-213">在維護現有的中繼資料，或移除不想要的中繼資料時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-213">This is useful for re-encoding an image while maintaining the existing metadata, or for removing unwanted metadata.</span></span> <span data-ttu-id="ad9ad-214">下列程式碼示範 **CreateQueryWriterFromReader** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-214">The following code demonstrates a **CreateQueryWriterFromReader** call.</span></span>


```
hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

// Copy metadata using query readers
if(SUCCEEDED(hr) && pFrameQReader)
{
    IWICMetadataQueryWriter *pNewWriter = NULL;

    GUID vendor = GUID_VendorMicrosoft;
    hr = pFactory->CreateQueryWriterFromReader(
        pFrameQReader,
        &vendor,
        &pNewWriter);
```



### <a name="adding-metadata"></a><span data-ttu-id="ad9ad-215">新增中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-215">Adding Metadata</span></span>

<span data-ttu-id="ad9ad-216">取得查詢寫入器之後，您可以使用它來加入中繼資料區塊和專案。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-216">After you obtain a query writer, you can use it to add metadata blocks and items.</span></span> <span data-ttu-id="ad9ad-217">若要寫入中繼資料，您可以使用查詢寫入器的 **SetMetadataByName** 方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-217">To write metadata, you use the query writer's **SetMetadataByName** method.</span></span> <span data-ttu-id="ad9ad-218">**SetMetadataByName** 接受兩個參數：查詢運算式 (*WzName*) 和 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*) 的指標。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-218">**SetMetadataByName** takes two parameters: a query expression (*wzName*) and a pointer to a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (*pvarValue*).</span></span> <span data-ttu-id="ad9ad-219">查詢運算式會定義要設定的區塊或專案，而 PROPVARIANT 會提供要設定的實際資料值。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-219">The query expression defines the block or item to set while the PROPVARIANT provides the actual data value to set.</span></span>

<span data-ttu-id="ad9ad-220">下列範例示範如何使用先前使用 **CreateQueryWriter** 方法取得的 XMP 查詢寫入器來加入標題。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-220">The following example demonstrates how to add a title by using the XMP query writer previously obtained by using the **CreateQueryWriter** method.</span></span>


```
// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
   
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```



<span data-ttu-id="ad9ad-221">在此範例中，值的類型 (vt) 設定為 `VT_LPWSTR` ，表示將會使用字串作為資料值。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-221">In this example, value's type (vt) is set to `VT_LPWSTR`, indicating that a string will be used as the data value.</span></span> <span data-ttu-id="ad9ad-222">因為 *值* 的類型是字串，所以會使用 *pwszVal* 來設定要使用的標題。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-222">Because *value*'s type is a string, *pwszVal* is used to set the title to use.</span></span> <span data-ttu-id="ad9ad-223">接著會使用查詢運算式 "/dc： title" 和新設定的 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)來呼叫 **SetMetadataByName** 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-223">**SetMetadataByName** is then called using the query expression "/dc:title" and the newly set [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ad9ad-224">使用的查詢運算式表示應該設定數位相機 (dc) 架構中的 title 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-224">The query expression used indicates that the title property in the digital camera (dc) schema should be set.</span></span> <span data-ttu-id="ad9ad-225">請注意，運算式不是 "/xmp/dc： title";這是因為查詢編寫器已經是 XMP 專屬的，而且不包含內嵌的 XMP 區塊，其中 "/xmp/dc： title" 會建議。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-225">Note that the expression is not "/xmp/dc:title"; this is because the query writer is already specific to XMP and does not contain an embedded XMP block, which "/xmp/dc:title" would suggest.</span></span>

<span data-ttu-id="ad9ad-226">到目前為止，您沒有實際將任何中繼資料新增至影像框架。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-226">Up to this point you haven't actually added any metadata to an image frame.</span></span> <span data-ttu-id="ad9ad-227">您只是將資料填入查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-227">You've simply populated a query writer with data.</span></span> <span data-ttu-id="ad9ad-228">若要將查詢寫入器所代表的中繼資料區塊加入至框架，您可以使用查詢寫入器作為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的值，再次呼叫 **SetMetadataByName** 。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-228">To add to a frame a metadata block represented by the query writer, you again call **SetMetadataByName** using the query writer as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant).</span></span> <span data-ttu-id="ad9ad-229">這可有效地將查詢寫入器中的中繼資料複製到影像框架。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-229">This effectively copies the metadata in the query writer to the image frame.</span></span> <span data-ttu-id="ad9ad-230">下列程式碼示範如何在先前取得至框架根中繼資料區塊的 XMP 查詢寫入器中加入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-230">The following code demonstrates how to add the metadata in the XMP query writer previously obtained to a frame's root metadata block.</span></span>


```
// Get the frame's query writer and write the XMP query writer to it
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);

    // Copy the metadata in the XMP query writer to the frame
    if (SUCCEEDED(hr))
    {
        PROPVARIANT value;

        PropVariantInit(&value);
        value.vt = VT_UNKNOWN;
        value.punkVal = pXMPWriter;
        value.punkVal->AddRef();

        hr = pFrameQWriter->SetMetadataByName(L"/", &value);

        PropVariantClear(&value);
    }
}
```



<span data-ttu-id="ad9ad-231">在此範例中，會使用 (vt) 的實值型別， `VT_UNKOWN` 表示 COM 介面的值型別。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-231">In this example, a value type (vt) of `VT_UNKOWN` is used; indicating a COM interface value type.</span></span> <span data-ttu-id="ad9ad-232">然後，會使用 XMP 查詢寫入器 (piXMPWriter) 做為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)的值，使用 AddRef 方法來加入它的參考。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-232">The XMP query writer (piXMPWriter) is then used as the value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), adding a reference to it by using the AddRef method.</span></span> <span data-ttu-id="ad9ad-233">最後，藉由呼叫框架的 **SetMetadataByName** 方法來設定 XMP 查詢寫入器，並傳遞查詢運算式 "/"，指出根區塊和新設定的 PROPVARIANT。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-233">Finally, the XMP query writer is set by calling the frame's **SetMetadataByName** method and passing the query expression "/", indicating the root block, and the newly set PROPVARIANT.</span></span>

> [!Note]  
> <span data-ttu-id="ad9ad-234">如果框架已包含您嘗試新增的中繼資料區塊，則會新增您要加入的中繼資料，並覆寫現有的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-234">If the frame already contains the metadata block you are trying to add, the metadata you are adding will be added and existing metadata overwritten.</span></span>

 

### <a name="removing-metadata"></a><span data-ttu-id="ad9ad-235">移除中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-235">Removing Metadata</span></span>

<span data-ttu-id="ad9ad-236">查詢寫入器也可讓您藉由呼叫 **RemoveMetadataByName** 方法來移除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-236">A query writer also enables you to remove metadata by calling the **RemoveMetadataByName** method.</span></span> <span data-ttu-id="ad9ad-237">**RemoveMetadataByName** 會採用查詢運算式，並移除中繼資料區塊或專案（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-237">**RemoveMetadataByName** takes a query expression and removes the metadata block or item if it exists.</span></span> <span data-ttu-id="ad9ad-238">下列程式碼示範如何移除先前加入的標題。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-238">The following code demonstrates how to remove the title that was previously added.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp/dc:title");
}
```



<span data-ttu-id="ad9ad-239">下列程式碼示範如何移除整個 XMP 中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-239">The following code demonstrates how to remove the entire XMP metadata block.</span></span>


```
if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/xmp");
}
```



### <a name="copying-metadata-for-re-encoding"></a><span data-ttu-id="ad9ad-240">複製重新編碼的中繼資料</span><span class="sxs-lookup"><span data-stu-id="ad9ad-240">Copying Metadata for Re-encoding</span></span>

> [!Note]  
> <span data-ttu-id="ad9ad-241">此區段中的程式碼只有在來源和目的影像格式相同時才有效。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-241">The code in this section is valid only when the source and destination image formats are the same.</span></span> <span data-ttu-id="ad9ad-242">編碼為不同的影像格式時，無法在單一作業中複製映射的所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-242">You cannot copy all of an image's metadata in a single operation when encoding to a different image format.</span></span>

 

<span data-ttu-id="ad9ad-243">若要在將影像重新編碼為相同的影像格式時保留中繼資料，有方法可在單一作業中複製所有中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-243">To preserve metadata while re-encoding an image to the same image format, there are methods available for copying all the metadata in a single operation.</span></span> <span data-ttu-id="ad9ad-244">這些作業都遵循類似的模式;每個都會將已解碼的框架中繼資料直接設定為所編碼的新框架。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-244">Each of these operations follows a similar pattern; each sets the decoded frame's metadata directly into the new frame being encoded.</span></span>

<span data-ttu-id="ad9ad-245">複製中繼資料的慣用方法是使用已解碼框架的區塊讀取器來初始化新框架的區塊寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-245">The preferred method to copy metadata is to initialize the new frame's block writer with the decoded frame's block reader.</span></span> <span data-ttu-id="ad9ad-246">下列程式碼示範這個方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-246">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    // Copy metadata using metadata block reader/writer
    if (SUCCEEDED(hr))
    {
        pFrameDecode->QueryInterface(
            IID_IWICMetadataBlockReader,
            (void**)&pBlockReader);
    }
    if (SUCCEEDED(hr))
    {
        pFrameEncode->QueryInterface(
            IID_IWICMetadataBlockWriter,
            (void**)&pBlockWriter);
    }
    if (SUCCEEDED(hr))
    {
        pBlockWriter->InitializeFromBlockReader(pBlockReader);
    }
}
```



<span data-ttu-id="ad9ad-247">在此範例中，會分別從來源畫面格和目的框架取得區塊讀取器和區塊寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-247">In this example, the block reader and the block writer are obtained from the source frame and destination frame, respectively.</span></span> <span data-ttu-id="ad9ad-248">區塊寫入器接著會從封鎖讀取器初始化。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-248">The block writer is then initialized from the block reader.</span></span> <span data-ttu-id="ad9ad-249">這會以封鎖讀取器預先填入的中繼資料來初始化封鎖讀取器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-249">This initializes the block reader with the pre-populated metadata of the block reader.</span></span>

<span data-ttu-id="ad9ad-250">複製中繼資料的另一個方法是使用編碼器的查詢寫入器來寫入查詢讀取器所參考的中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-250">Another method to copy metadata is to write the metadata block referenced by the query reader using the encoder's query writer.</span></span> <span data-ttu-id="ad9ad-251">下列程式碼示範這個方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-251">The following code demonstrates this method.</span></span>


```
if (SUCCEEDED(hr) && formatsEqual)
{
    hr = pFrameDecode->GetMetadataQueryReader(&pFrameQReader);

    // Copy metadata using query readers
    if(SUCCEEDED(hr))
    {
        hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
        if (SUCCEEDED(hr))
        {
            PropVariantClear(&value);
            value.vt=VT_UNKNOWN;
            value.punkVal=pFrameQReader;
            value.punkVal->AddRef();
            hr = pFrameQWriter->SetMetadataByName(L"/", &value);
            PropVariantClear(&value);
        }
    }
}
```



<span data-ttu-id="ad9ad-252">在這裡，會從已解碼的框架取得查詢讀取器，然後用來做為 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 的屬性值，並將值型別設定為 VT \_ UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-252">Here, a query reader is obtained from the decoded frame and then used as the property value of the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) with a value type set to VT\_UNKNOWN.</span></span> <span data-ttu-id="ad9ad-253">會取得編碼器的查詢寫入器，並使用查詢運算式 "/" 來設定根導覽路徑的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-253">The query writer for the encoder is obtained and the query expression "/" is used to set the metadata at the root navigation path.</span></span> <span data-ttu-id="ad9ad-254">您也可以在設定 nested 中繼資料區塊時使用這個方法，方法是將查詢運算式調整至所需的位置。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-254">You can also use this method when setting nested metadata blocks, by adjusting the query expression to the desired location.</span></span>

<span data-ttu-id="ad9ad-255">同樣地，您也可以使用映射處理站的 **CreateQueryWriterFromReader** 方法，根據已解碼框架的查詢讀取器來建立查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-255">Similarly, you can create a query writer based on the decoded frame's query reader by using the imaging factory's **CreateQueryWriterFromReader** method.</span></span> <span data-ttu-id="ad9ad-256">在這項作業中建立的查詢寫入器將會使用查詢讀取器中的中繼資料預先填入，然後可以在框架中設定。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-256">The query writer created in this operation will be prepopulated with the metadata from the query reader and can then be set in the frame.</span></span> <span data-ttu-id="ad9ad-257">下列程式碼示範 **CreateQueryWriterFromReader** 複製作業。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-257">The following code demonstrates the **CreateQueryWriterFromReader** copy operation.</span></span>


```
IWICMetadataQueryWriter *pNewWriter = NULL;

GUID vendor = GUID_VendorMicrosoft;
hr = pFactory->CreateQueryWriterFromReader(
    pFrameQReader,
    &vendor,
    &pNewWriter);

if (SUCCEEDED(hr))
{
    // Get the frame's query writer
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

// Set the query writer to the frame.
if (SUCCEEDED(hr))
{
    PROPVARIANT value;

    PropVariantInit(&value);
    value.vt = VT_UNKNOWN;
    value.punkVal = pNewWriter;
    value.punkVal->AddRef();
    hr = pFrameQWriter->SetMetadataByName(L"/",&value);
}
```



<span data-ttu-id="ad9ad-258">這個方法會根據查詢讀取器的資料來建立個別的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-258">This method uses a separate query writer is created that is based on the data of the query reader.</span></span> <span data-ttu-id="ad9ad-259">這個新的查詢寫入器接著會在框架中設定。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-259">This new query writer then set in the frame.</span></span>

<span data-ttu-id="ad9ad-260">同樣地，只有當來源和目的地映射的格式相同時，才會使用這些複製中繼資料的作業。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-260">Again, these operations to copy metadata only work when the source and destination images have the same format.</span></span> <span data-ttu-id="ad9ad-261">這是因為不同的影像格式會將中繼資料區塊儲存在不同的位置。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-261">This is because different image formats store the metadata blocks in different locations.</span></span> <span data-ttu-id="ad9ad-262">舉例來說，JPEG 和 TIFF 都支援 XMP 中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-262">For instance, both JPEG and TIFF support XMP metadata blocks.</span></span> <span data-ttu-id="ad9ad-263">在 JPEG 影像中，XMP 區塊位於「 [WIC 中繼資料」總覽](-wic-about-metadata.md)中所述的根中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-263">In JPEG images, the XMP block is at the root metadata block as illustrated in the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="ad9ad-264">不過，在 TIFF 影像中，XMP 區塊會嵌套在根目錄的 IFD 區塊中。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-264">However, in a TIFF image, the XMP block is nested in a root IFD block.</span></span> <span data-ttu-id="ad9ad-265">下圖說明 JPEG 影像與具有相同評等中繼資料的 TIFF 影像之間的差異。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-265">The following diagram illustrates the differences between a JPEG image and a TIFF image with the same rating metadata.</span></span>

![jpeg 和 tiff 比較。](graphics/jpgvstiff.png)

## <a name="fast-metadata-encoding"></a><span data-ttu-id="ad9ad-267">快速中繼資料編碼</span><span class="sxs-lookup"><span data-stu-id="ad9ad-267">Fast Metadata Encoding</span></span>

<span data-ttu-id="ad9ad-268">不一定需要重新編碼影像，才能將新的中繼資料寫入其中。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-268">It is not always necessary to re-encode an image to write new metadata to it.</span></span> <span data-ttu-id="ad9ad-269">您也可以使用快速的中繼資料編碼器來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-269">Metadata can also be written by using a fast metadata encoder.</span></span> <span data-ttu-id="ad9ad-270">快速中繼資料編碼器可將有限數量的中繼資料寫入影像，而不需要重新編碼影像。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-270">A fast metadata encoder can write a limited amount of metadata to an image without re-encoding the image.</span></span> <span data-ttu-id="ad9ad-271">這是藉由在部分元資料格式所提供的空白填補內撰寫新的中繼資料來完成。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-271">This is accomplished by writing the new metadata within the empty padding provided by some metadata formats.</span></span> <span data-ttu-id="ad9ad-272">支援中繼資料填補的原生元資料格式為 Exif、IFD、GPS 和 XMP。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-272">The native metadata formats that support metadata padding are Exif, IFD, GPS and XMP.</span></span>

### <a name="adding-padding-to-metadata-blocks"></a><span data-ttu-id="ad9ad-273">將填補加入中繼資料區塊</span><span class="sxs-lookup"><span data-stu-id="ad9ad-273">Adding Padding to Metadata Blocks</span></span>

<span data-ttu-id="ad9ad-274">您必須要有中繼資料區塊內的空間來寫入更多中繼資料，才能執行快速中繼資料編碼。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-274">Before you can perform fast metadata encoding, there must be room within the metadata block to write more metadata.</span></span> <span data-ttu-id="ad9ad-275">如果現有填補內沒有足夠的空間來寫入新的中繼資料，快速中繼資料編碼將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-275">If there is not enough room within the existing padding to write the new metadata, the fast metadata encoding will fail.</span></span> <span data-ttu-id="ad9ad-276">若要在影像中加入中繼資料填補，必須重新編碼影像。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-276">To add metadata padding to an image, the image must be re-encoded.</span></span> <span data-ttu-id="ad9ad-277">如果您要填補的中繼資料區塊支援，您可以使用查詢運算式，以新增任何其他中繼資料專案的相同方式加入填補。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-277">You can add padding the same way you would add any other metadata item, by using a query expression, if the metadata block you are padding supports it.</span></span> <span data-ttu-id="ad9ad-278">下列範例示範如何將填補新增至內嵌于 App1 區塊中的 IFD 區塊。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-278">The following example demonstrates how to add padding to an IFD block embedded in an App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    // Add metadata padding
    PROPVARIANT padding;

    PropVariantInit(&padding);
    padding.vt = VT_UI4;
    padding.uiVal = 4096; // 4KB

    hr = pFrameQWriter->SetMetadataByName(L"/app1/ifd/PaddingSchema:padding", &padding);

    PropVariantClear(&padding);
}
```



<span data-ttu-id="ad9ad-279">若要加入填補，請建立 VT UI4 類型的 PROPVARIANT \_ ，以及對應至要加入的填補位元組數目的值。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-279">To add padding, create a PROPVARIANT of type VT\_UI4 and a value corresponding to the number of bytes of padding to add.</span></span> <span data-ttu-id="ad9ad-280">一般值為4096個位元組。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-280">A typical value is 4096 bytes.</span></span> <span data-ttu-id="ad9ad-281">JPEG、TIFF 和 JPEG XR 的中繼資料查詢是在此表格中。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-281">The metadata queries for JPEG, TIFF, and JPEG-XR are in this table.</span></span>



| <span data-ttu-id="ad9ad-282">元資料格式</span><span class="sxs-lookup"><span data-stu-id="ad9ad-282">Metadata format</span></span> | <span data-ttu-id="ad9ad-283">JPEG 中繼資料查詢</span><span class="sxs-lookup"><span data-stu-id="ad9ad-283">JPEG metadata query</span></span>                  | <span data-ttu-id="ad9ad-284">TIFF，JPEG XR 中繼資料查詢</span><span class="sxs-lookup"><span data-stu-id="ad9ad-284">TIFF, JPEG-XR metadata query</span></span>    |
|-----------------|--------------------------------------|---------------------------------|
| <span data-ttu-id="ad9ad-285">IFD</span><span class="sxs-lookup"><span data-stu-id="ad9ad-285">IFD</span></span>             | <span data-ttu-id="ad9ad-286">/app1/ifd/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-286">/app1/ifd/PaddingSchema:Padding</span></span>      | <span data-ttu-id="ad9ad-287">/ifd/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-287">/ifd/PaddingSchema:Padding</span></span>      |
| <span data-ttu-id="ad9ad-288">Exif</span><span class="sxs-lookup"><span data-stu-id="ad9ad-288">EXIF</span></span>            | <span data-ttu-id="ad9ad-289">/app1/ifd/exif/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-289">/app1/ifd/exif/PaddingSchema:Padding</span></span> | <span data-ttu-id="ad9ad-290">/ifd/exif/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-290">/ifd/exif/PaddingSchema:Padding</span></span> |
| <span data-ttu-id="ad9ad-291">XMP</span><span class="sxs-lookup"><span data-stu-id="ad9ad-291">XMP</span></span>             | <span data-ttu-id="ad9ad-292">/xmp/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-292">/xmp/PaddingSchema:Padding</span></span>           | <span data-ttu-id="ad9ad-293">/ifd/xmp/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-293">/ifd/xmp/PaddingSchema:Padding</span></span>  |
| <span data-ttu-id="ad9ad-294">GPS</span><span class="sxs-lookup"><span data-stu-id="ad9ad-294">GPS</span></span>             | <span data-ttu-id="ad9ad-295">/app1/ifd/gps/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-295">/app1/ifd/gps/PaddingSchema:Padding</span></span>  | <span data-ttu-id="ad9ad-296">/ifd/gps/PaddingSchema：填補</span><span class="sxs-lookup"><span data-stu-id="ad9ad-296">/ifd/gps/PaddingSchema:Padding</span></span>  |



 

### <a name="obtaining-a-fast-metadata-encoder"></a><span data-ttu-id="ad9ad-297">取得快速中繼資料編碼器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-297">Obtaining a Fast Metadata Encoder</span></span>

<span data-ttu-id="ad9ad-298">當您擁有具有中繼資料填補的影像時，可以使用映射處理站方法 **CreateFastMetadataEncoderFromDecoder** 和 **CreateFastMetadataEncoderFromFrameDecode** 來取得快速中繼資料編碼器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-298">When you have an image with metadata padding, a fast metadata encoder can be obtained by using the imaging factory methods **CreateFastMetadataEncoderFromDecoder** and **CreateFastMetadataEncoderFromFrameDecode**.</span></span>

<span data-ttu-id="ad9ad-299">顧名思義， **CreateFastMetadataEncoderFromDecoder** 會為編碼器層級的中繼資料建立快速的中繼資料編碼器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-299">As the name implies, **CreateFastMetadataEncoderFromDecoder** creates a fast metadata encoder for decoder-level metadata.</span></span> <span data-ttu-id="ad9ad-300">WIC 提供的原生影像格式不支援解碼器層級的中繼資料，但在未來開發影像格式的情況下，會提供此方法。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-300">The native image formats provided by WIC do not support decoder-level metadata but this method is provided in case such an image format is developed in the future.</span></span>

<span data-ttu-id="ad9ad-301">較常見的案例是使用 **CreateFastMetadataEncoderFromFrameDecode** 從影像框架取得快速的中繼資料編碼器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-301">The more common scenario is to obtain a fast metadata encoder from an image frame by using **CreateFastMetadataEncoderFromFrameDecode**.</span></span> <span data-ttu-id="ad9ad-302">下列程式碼會取得已解碼的框架快速中繼資料編碼器，並變更 App1 區塊中的分級值。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-302">The following code obtains a decoded frame's fast metadata encoder and changes the rating value in the App1 block.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode, 
        &pFME);
}
```



### <a name="using-the-fast-metadata-encoder"></a><span data-ttu-id="ad9ad-303">使用快速中繼資料編碼器</span><span class="sxs-lookup"><span data-stu-id="ad9ad-303">Using the Fast Metadata Encoder</span></span>

<span data-ttu-id="ad9ad-304">您可以從快速中繼資料編碼器取得查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-304">From the fast metadata encoder, you can obtain a query writer.</span></span> <span data-ttu-id="ad9ad-305">這可讓您使用先前所示範的查詢運算式來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-305">This enables you to write metadata by using a query expression as previously demonstrated.</span></span> <span data-ttu-id="ad9ad-306">在查詢寫入器中設定中繼資料之後，請認可快速中繼資料編碼器來完成中繼資料更新。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-306">After metadata has been set in the query writer, commit the fast metadata encoder to finalize the metadata update.</span></span> <span data-ttu-id="ad9ad-307">下列程式碼示範如何設定和認可中繼資料變更。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-307">The following code demonstrates setting and committing the metadata changes</span></span>


```
    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



<span data-ttu-id="ad9ad-308">如果 **Commit** 因為任何原因而失敗，您將需要重新編碼影像，以確保新的中繼資料會加入至映射。</span><span class="sxs-lookup"><span data-stu-id="ad9ad-308">If **Commit** fails for any reason, you will need to re-encode the image to ensure the new metadata is added to the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad9ad-309">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad9ad-309">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad9ad-310">**概念**</span><span class="sxs-lookup"><span data-stu-id="ad9ad-310">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad9ad-311">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ad9ad-311">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ad9ad-312">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="ad9ad-312">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="ad9ad-313">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="ad9ad-313">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="ad9ad-314">中繼資料擴充性總覽</span><span class="sxs-lookup"><span data-stu-id="ad9ad-314">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="ad9ad-315">How to：使用中繼資料重新編碼 JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="ad9ad-315">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
