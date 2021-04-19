---
description: Windows 影像處理元件 (WIC) 提供元件物件模型 (以 COM) 為基礎的 API，以用於 C 和 c + +。
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: WIC API 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998120"
---
# <a name="wic-api-overview"></a><span data-ttu-id="2ea20-103">WIC API 總覽</span><span class="sxs-lookup"><span data-stu-id="2ea20-103">WIC API Overview</span></span>

<span data-ttu-id="2ea20-104">Windows 影像處理元件 (WIC) 提供元件物件模型 (以 COM) 為基礎的 API，以用於 C 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="2ea20-104">The Windows Imaging Component (WIC) provides a Component Object Model (COM) based API for use in C and C++.</span></span> <span data-ttu-id="2ea20-105">WIC API 會公開各種與影像相關的功能，包括：</span><span class="sxs-lookup"><span data-stu-id="2ea20-105">The WIC API exposes a variety of image-related functionality, including:</span></span>

-   <span data-ttu-id="2ea20-106">標準 web 映射格式的內建編解碼器。</span><span class="sxs-lookup"><span data-stu-id="2ea20-106">Built-in codecs for the standard web image formats.</span></span>
-   <span data-ttu-id="2ea20-107">標準元資料格式的內建支援。</span><span class="sxs-lookup"><span data-stu-id="2ea20-107">Built-in support for standard metadata formats.</span></span>
-   <span data-ttu-id="2ea20-108">範圍廣泛的像素格式支援。</span><span class="sxs-lookup"><span data-stu-id="2ea20-108">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="2ea20-109">高彩支援;包含30位的延伸範圍、30位高精確度，以及48位高精確度和寬範圍像素格式。</span><span class="sxs-lookup"><span data-stu-id="2ea20-109">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="2ea20-110">映射編解碼器、像素格式和元資料格式的可擴充架構。</span><span class="sxs-lookup"><span data-stu-id="2ea20-110">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>

<span data-ttu-id="2ea20-111">本主題包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="2ea20-111">This topic contains the following topics.</span></span>

-   [<span data-ttu-id="2ea20-112">WIC 標頭檔</span><span class="sxs-lookup"><span data-stu-id="2ea20-112">WIC Header Files</span></span>](#wic-header-files)
-   [<span data-ttu-id="2ea20-113">程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="2ea20-113">Library Files</span></span>](#library-files)
-   [<span data-ttu-id="2ea20-114">Class factory</span><span class="sxs-lookup"><span data-stu-id="2ea20-114">Class Factories</span></span>](#class-factories)
-   [<span data-ttu-id="2ea20-115">影像處理元件</span><span class="sxs-lookup"><span data-stu-id="2ea20-115">Imaging Components</span></span>](#imaging-components)
-   [<span data-ttu-id="2ea20-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ea20-116">See Also</span></span>](#see-also)

## <a name="wic-header-files"></a><span data-ttu-id="2ea20-117">WIC 標頭檔</span><span class="sxs-lookup"><span data-stu-id="2ea20-117">WIC Header Files</span></span>

<span data-ttu-id="2ea20-118">WIC Api 定義于下列標頭和介面定義語言 (IDL) 檔：</span><span class="sxs-lookup"><span data-stu-id="2ea20-118">The WIC APIs are defined in the following header and Interface Definition Language (IDL) files:</span></span>



| <span data-ttu-id="2ea20-119">檔案</span><span class="sxs-lookup"><span data-stu-id="2ea20-119">File</span></span>              | <span data-ttu-id="2ea20-120">描述</span><span class="sxs-lookup"><span data-stu-id="2ea20-120">Description</span></span>                                          |
|-------------------|------------------------------------------------------|
| <span data-ttu-id="2ea20-121">wincodec。h</span><span class="sxs-lookup"><span data-stu-id="2ea20-121">wincodec.h</span></span>        | <span data-ttu-id="2ea20-122">定義主要 WIC Api 的 C 和 c + + 版本。</span><span class="sxs-lookup"><span data-stu-id="2ea20-122">Defines C and C++ versions of the primary WIC APIs.</span></span>  |
| <span data-ttu-id="2ea20-123">wincodec .idl</span><span class="sxs-lookup"><span data-stu-id="2ea20-123">wincodec.idl</span></span>      | <span data-ttu-id="2ea20-124">定義主要 WIC 介面。</span><span class="sxs-lookup"><span data-stu-id="2ea20-124">Defines the primary WIC interfaces.</span></span>                  |
| <span data-ttu-id="2ea20-125">wincodecsdk。h</span><span class="sxs-lookup"><span data-stu-id="2ea20-125">wincodecsdk.h</span></span>     | <span data-ttu-id="2ea20-126">定義 C 和 c + + 版本的中繼資料 WIC Api。</span><span class="sxs-lookup"><span data-stu-id="2ea20-126">Defines C and C++ versions of the metadata WIC APIs.</span></span> |
| <span data-ttu-id="2ea20-127">wincodecsdk .idl</span><span class="sxs-lookup"><span data-stu-id="2ea20-127">wincodecsdk.idl</span></span>   | <span data-ttu-id="2ea20-128">定義 WIC 中繼資料介面。</span><span class="sxs-lookup"><span data-stu-id="2ea20-128">Defines the WIC metadata interfaces.</span></span>                 |
| <span data-ttu-id="2ea20-129">wincodec \_ proxy。h</span><span class="sxs-lookup"><span data-stu-id="2ea20-129">wincodec\_proxy.h</span></span> | <span data-ttu-id="2ea20-130">定義 WIC proxy 匯出。</span><span class="sxs-lookup"><span data-stu-id="2ea20-130">Defines the WIC proxy exports.</span></span>                       |



 

<span data-ttu-id="2ea20-131">若要使用 WIC，您的應用程式必須包含 wincodec 和/或 wincodecsdk，視您應用程式所需的 API 而定。</span><span class="sxs-lookup"><span data-stu-id="2ea20-131">To use WIC, your applications must include wincodec.h and/or wincodecsdk.h, depending on the API your application needs.</span></span>

## <a name="library-files"></a><span data-ttu-id="2ea20-132">程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="2ea20-132">Library Files</span></span>

<span data-ttu-id="2ea20-133">WIC 程式庫檔案：</span><span class="sxs-lookup"><span data-stu-id="2ea20-133">The WIC library files:</span></span>



| <span data-ttu-id="2ea20-134">檔案</span><span class="sxs-lookup"><span data-stu-id="2ea20-134">File</span></span>              | <span data-ttu-id="2ea20-135">描述</span><span class="sxs-lookup"><span data-stu-id="2ea20-135">Description</span></span>                                                            |
|-------------------|------------------------------------------------------------------------|
| <span data-ttu-id="2ea20-136">windowscodecs .lib</span><span class="sxs-lookup"><span data-stu-id="2ea20-136">windowscodecs.lib</span></span> | <span data-ttu-id="2ea20-137">Windows 軟體開發套件 (SDK) 提供的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="2ea20-137">Import library provided by the Windows Software Development Kit (SDK).</span></span> |
| <span data-ttu-id="2ea20-138">windowscodecs.dll</span><span class="sxs-lookup"><span data-stu-id="2ea20-138">windowscodecs.dll</span></span> | <span data-ttu-id="2ea20-139">由作業系統提供的庫存執行程式庫。</span><span class="sxs-lookup"><span data-stu-id="2ea20-139">Stock implementation library provided by the operating system.</span></span>         |



 

<span data-ttu-id="2ea20-140">若要連結到 WIC Api，您的應用程式必須包含 windowscodec，做為額外的連結器相依性。</span><span class="sxs-lookup"><span data-stu-id="2ea20-140">To link to WIC APIs, your application must include windowscodec.lib as an additional linker dependency.</span></span>

## <a name="class-factories"></a><span data-ttu-id="2ea20-141">Class factory</span><span class="sxs-lookup"><span data-stu-id="2ea20-141">Class Factories</span></span>

<span data-ttu-id="2ea20-142">下表描述 WIC Api 針對建立 WIC 元件所提供的兩個 COM class factory。</span><span class="sxs-lookup"><span data-stu-id="2ea20-142">The following table describes the two COM class factories the WIC APIs provide for creating WIC components.</span></span>



| <span data-ttu-id="2ea20-143">Factory 介面</span><span class="sxs-lookup"><span data-stu-id="2ea20-143">Factory Interface</span></span>                                               | <span data-ttu-id="2ea20-144">Description</span><span class="sxs-lookup"><span data-stu-id="2ea20-144">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ea20-145">**IWICImagingFactory**</span><span class="sxs-lookup"><span data-stu-id="2ea20-145">**IWICImagingFactory**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | <span data-ttu-id="2ea20-146">使用 WIC 元件開發應用程式的主要 class factory。</span><span class="sxs-lookup"><span data-stu-id="2ea20-146">Primary class factory for application development using WIC components.</span></span> <span data-ttu-id="2ea20-147">此 factory 會建立映射解碼器、編碼器和資料流程等元件。</span><span class="sxs-lookup"><span data-stu-id="2ea20-147">This factory creates components such as image decoders, encoders and streams.</span></span>   |
| [<span data-ttu-id="2ea20-148">**IWICComponentFactory**</span><span class="sxs-lookup"><span data-stu-id="2ea20-148">**IWICComponentFactory**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | <span data-ttu-id="2ea20-149">以 WIC 元件開發人員為目標的 Class factory。</span><span class="sxs-lookup"><span data-stu-id="2ea20-149">Class factory targeted for WIC component developers.</span></span> <span data-ttu-id="2ea20-150">從這個 factory 建立的元件主要用於編解碼器和元資料處理程式開發。</span><span class="sxs-lookup"><span data-stu-id="2ea20-150">Components created from this factory are primarily used in codec and metadata handler development.</span></span> |



 

<span data-ttu-id="2ea20-151">若要建立任一個 class factory，請使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM 函數。</span><span class="sxs-lookup"><span data-stu-id="2ea20-151">To create either class factory, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="2ea20-152">下列範例示範如何建立 WIC 映射處理站。</span><span class="sxs-lookup"><span data-stu-id="2ea20-152">The following example demonstrates the creation of the WIC imaging factory.</span></span>


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a><span data-ttu-id="2ea20-153">影像處理元件</span><span class="sxs-lookup"><span data-stu-id="2ea20-153">Imaging Components</span></span>

<span data-ttu-id="2ea20-154">WIC Api 提供數種類型的影像處理元件。</span><span class="sxs-lookup"><span data-stu-id="2ea20-154">The WIC APIs provide several types of imaging components.</span></span> <span data-ttu-id="2ea20-155">下表說明一些常見的 WIC 元件。</span><span class="sxs-lookup"><span data-stu-id="2ea20-155">The following table describes some of the common WIC components.</span></span> <span data-ttu-id="2ea20-156">如需可用元件的完整清單，請參閱 [WIC 介面](-wic-codec-ifaces.md)。</span><span class="sxs-lookup"><span data-stu-id="2ea20-156">For a full list of available components, see [WIC interfaces](-wic-codec-ifaces.md).</span></span>



| <span data-ttu-id="2ea20-157">元件類型</span><span class="sxs-lookup"><span data-stu-id="2ea20-157">Component Type</span></span>                                                      | <span data-ttu-id="2ea20-158">Description</span><span class="sxs-lookup"><span data-stu-id="2ea20-158">Description</span></span>                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ea20-159">**點陣圖**</span><span class="sxs-lookup"><span data-stu-id="2ea20-159">**Bitmap**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | <span data-ttu-id="2ea20-160">表示 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)的可寫入記憶體中標記法。</span><span class="sxs-lookup"><span data-stu-id="2ea20-160">Represents a writable in-memory representation of an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource).</span></span> |
| [<span data-ttu-id="2ea20-161">**解碼 器**</span><span class="sxs-lookup"><span data-stu-id="2ea20-161">**Decoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | <span data-ttu-id="2ea20-162">用來將資料流程中的影像資料解碼成適用于影像處理的格式。</span><span class="sxs-lookup"><span data-stu-id="2ea20-162">Used to decode image data from a stream into a format that is useful for image processing.</span></span>                    |
| [<span data-ttu-id="2ea20-163">**編碼**</span><span class="sxs-lookup"><span data-stu-id="2ea20-163">**Encoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | <span data-ttu-id="2ea20-164">將影像資料寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="2ea20-164">Writes image data to a stream.</span></span>                                                                                |
| [<span data-ttu-id="2ea20-165">**串流**</span><span class="sxs-lookup"><span data-stu-id="2ea20-165">**Stream**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | <span data-ttu-id="2ea20-166">用來讀取和寫入檔案、網路資源、記憶體區塊等的資料。</span><span class="sxs-lookup"><span data-stu-id="2ea20-166">Used to read and write data from a file, network resource, a block of memory, and so on.</span></span>                      |
| [<span data-ttu-id="2ea20-167">**格式轉換器**</span><span class="sxs-lookup"><span data-stu-id="2ea20-167">**Format Converter**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | <span data-ttu-id="2ea20-168">用來從一個像素格式轉換成另一個圖元。</span><span class="sxs-lookup"><span data-stu-id="2ea20-168">Used to convert from one pixel format to another.</span></span>                                                             |
| [<span data-ttu-id="2ea20-169">**中繼資料查詢讀取器**</span><span class="sxs-lookup"><span data-stu-id="2ea20-169">**Metadata Query Reader**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | <span data-ttu-id="2ea20-170">用來讀取影像或影像框架的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2ea20-170">Used to read metadata of an image or image frame.</span></span>                                                             |
| [<span data-ttu-id="2ea20-171">**中繼資料查詢寫入器**</span><span class="sxs-lookup"><span data-stu-id="2ea20-171">**Metadata Query Writer**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | <span data-ttu-id="2ea20-172">用來將中繼資料寫入影像或影像框架。</span><span class="sxs-lookup"><span data-stu-id="2ea20-172">Used to write metadata to an image or image frame.</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="2ea20-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ea20-173">See Also</span></span>

[<span data-ttu-id="2ea20-174">參考</span><span class="sxs-lookup"><span data-stu-id="2ea20-174">References</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="2ea20-175">範例和程式碼範例</span><span class="sxs-lookup"><span data-stu-id="2ea20-175">Samples and Code Examples</span></span>](-wic-samples.md)


 

 
