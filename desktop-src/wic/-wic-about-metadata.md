---
description: 本主題介紹 Windows 影像處理元件 (WIC) 所提供的映射中繼資料支援。
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: WIC 中繼資料總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563345"
---
# <a name="wic-metadata-overview"></a><span data-ttu-id="93e18-103">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="93e18-103">WIC Metadata Overview</span></span>

<span data-ttu-id="93e18-104">本主題介紹 Windows 影像處理元件 (WIC) 所提供的映射中繼資料支援。</span><span class="sxs-lookup"><span data-stu-id="93e18-104">This topic introduces the imaging metadata support provided by the Windows Imaging Component (WIC).</span></span> <span data-ttu-id="93e18-105">它提供讀取和寫入影像中繼資料、中繼資料查詢語言和元資料處理程式擴充性的簡介。</span><span class="sxs-lookup"><span data-stu-id="93e18-105">It provides an introduction to reading and writing image metadata, the metadata query language, and metadata handler extensibility.</span></span>

<span data-ttu-id="93e18-106">影像中繼資料是內嵌在影像檔內的資料，可提供映射的其他相關資訊，例如用來捕捉影像的裝置，或影像的維度。</span><span class="sxs-lookup"><span data-stu-id="93e18-106">Image metadata is data embedded inside an image file that provides additional information about the image, such as the device used to capture the image or the dimensions of the image.</span></span> <span data-ttu-id="93e18-107">雖然它包含在影像檔案本身內，但此中繼資料不是轉譯資料的一部分。</span><span class="sxs-lookup"><span data-stu-id="93e18-107">Although it is contained within the image file itself, this metadata is not part of the rendering data.</span></span> <span data-ttu-id="93e18-108">WIC 提供的介面可讓您針對數種常見的元資料格式讀取和寫入此中繼資料，包括可延伸的中繼資料平臺 (XMP) 、交換影像檔 (EXIF) ，以及 Png 文字資料 (文字) 。</span><span class="sxs-lookup"><span data-stu-id="93e18-108">WIC provides interfaces that enable you to read and write this metadata for several common metadata formats including Extensible Metadata Platform (XMP), Exchangeable Image File (EXIF), and Png Textual Data (tEXt).</span></span>

<span data-ttu-id="93e18-109">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="93e18-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="93e18-110">先決條件</span><span class="sxs-lookup"><span data-stu-id="93e18-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="93e18-111">簡介</span><span class="sxs-lookup"><span data-stu-id="93e18-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="93e18-112">讀取影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="93e18-112">Reading Image Metadata</span></span>](#reading-image-metadata)
-   [<span data-ttu-id="93e18-113">寫入影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="93e18-113">Writing Image Metadata</span></span>](#writing-image-metadata)
-   [<span data-ttu-id="93e18-114">中繼資料擴充性</span><span class="sxs-lookup"><span data-stu-id="93e18-114">Metadata Extensibility</span></span>](#metadata-extensibility)
-   [<span data-ttu-id="93e18-115">支援的元資料格式</span><span class="sxs-lookup"><span data-stu-id="93e18-115">Supported Metadata Formats</span></span>](#supported-metadata-formats)
-   [<span data-ttu-id="93e18-116">中繼資料元件摘要</span><span class="sxs-lookup"><span data-stu-id="93e18-116">Metadata Component Summary</span></span>](#metadata-component-summary)
-   [<span data-ttu-id="93e18-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="93e18-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="93e18-118">必要條件</span><span class="sxs-lookup"><span data-stu-id="93e18-118">Prerequisites</span></span>

<span data-ttu-id="93e18-119">若要瞭解本主題，您應該熟悉 WIC 編碼器和解碼器介面，以及其相關元件物件模型 (COM) 元件，如 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)所述。</span><span class="sxs-lookup"><span data-stu-id="93e18-119">To understand this topic, you should be familiar with the WIC encoder and decoder interfaces and their related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="93e18-120">它也有助於讓您大致熟悉目前使用的一些影像處理元資料格式。</span><span class="sxs-lookup"><span data-stu-id="93e18-120">It also helps to have a general familiarity with some of the imaging metadata formats in use today.</span></span>

## <a name="introduction"></a><span data-ttu-id="93e18-121">簡介</span><span class="sxs-lookup"><span data-stu-id="93e18-121">Introduction</span></span>

<span data-ttu-id="93e18-122">中繼資料提供有關影像的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="93e18-122">Metadata provides extended information about an image.</span></span> <span data-ttu-id="93e18-123">這項資訊可以用數種方式來使用。</span><span class="sxs-lookup"><span data-stu-id="93e18-123">This information can be used in several ways.</span></span> <span data-ttu-id="93e18-124">影像可能包含中繼資料，例如描述、評等、類別標記和著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="93e18-124">An image might contain metadata such as a description, rating, category tags, and copyright information.</span></span> <span data-ttu-id="93e18-125">存取中繼資料可讓您更輕鬆地執行工作，例如資產管理、檔案位置或決定著作權資訊。</span><span class="sxs-lookup"><span data-stu-id="93e18-125">Accessing the metadata makes it easier to perform tasks such as asset management, file location, or determining copyright information.</span></span> <span data-ttu-id="93e18-126">例如，Windows Vista 中的 Windows 影像中心可讓您將描述和類別標記新增至影像。</span><span class="sxs-lookup"><span data-stu-id="93e18-126">For example, the Windows Photo Gallery in Windows Vista enables you to add descriptions and category tags to images.</span></span> <span data-ttu-id="93e18-127">這可讓您更有效率地探索映射，並提供方便的方式來分類影像。</span><span class="sxs-lookup"><span data-stu-id="93e18-127">This allows for better discoverability of images and a convenient way to categorize images.</span></span> <span data-ttu-id="93e18-128">使用 WIC Api 和通用元資料格式，應用程式可以輕鬆地將這類的中繼資料寫入或讀取至影像。</span><span class="sxs-lookup"><span data-stu-id="93e18-128">Using the WIC APIs and common metadata formats, applications can easily write or read this type of metadata to or from images.</span></span>

<span data-ttu-id="93e18-129">下圖說明 JPEG 檔案的內容，其中包含內嵌的中繼資料區塊和中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="93e18-129">The following diagram illustrates the contents of a JPEG file that includes embedded metadata blocks and metadata items.</span></span>

![具有評等中繼資料的 jpeg 影像](graphics/jpeg.png)

<span data-ttu-id="93e18-131">在此範例影像中，中繼資料會內嵌在影像檔案框架內的影像檔案中。</span><span class="sxs-lookup"><span data-stu-id="93e18-131">In this example image, the metadata is embedded in the image file within an image frame.</span></span> <span data-ttu-id="93e18-132">JPEG 格式不支援多個影像框架，因此中繼資料在概念上會附加到這個單一框架。</span><span class="sxs-lookup"><span data-stu-id="93e18-132">The JPEG format does not support multiple image frames, so the metadata is conceptually attached to this single frame.</span></span> <span data-ttu-id="93e18-133">支援多個框架的格式（例如 TIFF）可能會有附加至每個影像框架的中繼資料，如圖所示。</span><span class="sxs-lookup"><span data-stu-id="93e18-133">Formats that support multiple frames, such as TIFF, may have metadata attached to each image frame as this diagram shows.</span></span> <span data-ttu-id="93e18-134">雖然目前並不受原生映射編解碼器支援，有些影像格式也可以支援影像框架以外的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-134">Though not common today and not supported by the native image codecs, some image formats may also support metadata outside of an image frame.</span></span> <span data-ttu-id="93e18-135">WIC 有足夠的彈性，可處理影像個別框架以外的框架層級中繼資料和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-135">WIC is flexible enough to handle both frame-level metadata and metadata outside of an image's individual frame.</span></span>

## <a name="reading-image-metadata"></a><span data-ttu-id="93e18-136">讀取影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="93e18-136">Reading Image Metadata</span></span>

<span data-ttu-id="93e18-137">WIC Api 提供 COM 元件，可讓應用程式輕鬆地讀取和寫入影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-137">The WIC APIs provide COM components that make it easy for applications to read and write image metadata.</span></span>

<span data-ttu-id="93e18-138">讀取中繼資料的主要方法是使用中繼資料查詢讀取器 ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) 來存取特定的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="93e18-138">The primary way to read metadata is to use a metadata query reader ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) to access specific metadata items.</span></span> <span data-ttu-id="93e18-139">中繼資料查詢讀取器元件是由編解碼器所執行，而且可以在解碼器層級或透過個別的影像框架（這是較常見的方法）來存取。</span><span class="sxs-lookup"><span data-stu-id="93e18-139">The metadata query reader component is implemented by the codec and can be accessed at the decoder level or through individual image frames, which is the more common method.</span></span> <span data-ttu-id="93e18-140">下列程式碼示範如何使用查詢讀取器的 **GetMetadataQueryReader** 方法，來存取個別框架的查詢讀取器。</span><span class="sxs-lookup"><span data-stu-id="93e18-140">The following code demonstrates how to access a query reader for an individual frame by using the query reader's **GetMetadataQueryReader** method.</span></span>


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



<span data-ttu-id="93e18-141">查詢讀取器會提供方法來取得特定中繼資料的相關資訊，以及用來指定要抓取之中繼資料專案的方法。</span><span class="sxs-lookup"><span data-stu-id="93e18-141">A query reader provides methods to obtain information about specific metadata, and a means to specify a metadata item to retrieve.</span></span> <span data-ttu-id="93e18-142">下列程式碼會使用查詢運算式，要求 (IFD) 區塊的 App1 嵌套影像檔案目錄內的特定中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="93e18-142">The following code uses a query expression to request a specific metadata item within the App1 nested image file directory (IFD) block.</span></span> <span data-ttu-id="93e18-143">這是藉由使用查詢讀取器的 **GetMetadataByName** 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="93e18-143">This is done by using the query reader's **GetMetadataByName** method.</span></span> <span data-ttu-id="93e18-144">下列程式碼示範如何使用查詢讀取器來取得 MicrosoftPhoto 分級值。</span><span class="sxs-lookup"><span data-stu-id="93e18-144">The following code demonstrates using the query reader to obtain the MicrosoftPhoto rating value.</span></span>


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



<span data-ttu-id="93e18-145">上述範例中的 pwzRatingQuery 變數是用來存取中繼資料專案 MicrosoftPhoto 評等的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="93e18-145">The pwzRatingQuery variable in the preceding example is the query string to access the metadata item MicrosoftPhoto rating.</span></span> <span data-ttu-id="93e18-146">這個字串是使用中繼資料查詢語言建立的。</span><span class="sxs-lookup"><span data-stu-id="93e18-146">This string is created by using the metadata query language.</span></span> <span data-ttu-id="93e18-147">若要建立這個字串，需要知道元資料格式和中繼資料查詢語言，才能取得個別的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="93e18-147">To create this string, knowledge of the metadata format and the metadata query language is needed to retrieve individual metadata items.</span></span> <span data-ttu-id="93e18-148">如需有關中繼資料查詢語言的詳細資訊，請參閱 [中繼資料查詢語言總覽](-wic-codec-metadataquerylanguage.md)。</span><span class="sxs-lookup"><span data-stu-id="93e18-148">For more information about the metadata query language, see the [Metadata Query Language Overview](-wic-codec-metadataquerylanguage.md).</span></span>

<span data-ttu-id="93e18-149">在幕後，查詢讀取器會使用中繼資料讀取器 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 來存取查詢運算式所描述的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-149">Behind the scenes, a query reader uses a metadata reader ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) to access the metadata described by the query expression.</span></span> <span data-ttu-id="93e18-150">除了使用查詢讀取器，您也可以直接存取中繼資料讀取器來讀取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-150">In addition to using a query reader, you can also access a metadata reader directly to read metadata.</span></span> <span data-ttu-id="93e18-151">您可以藉由查詢區塊讀取器 ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) 介面，從解碼器或個別的框架取得中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="93e18-151">You can obtain a metadata reader from the decoder or individual frames by querying for a block reader ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)) interface.</span></span>

## <a name="writing-image-metadata"></a><span data-ttu-id="93e18-152">寫入影像中繼資料</span><span class="sxs-lookup"><span data-stu-id="93e18-152">Writing Image Metadata</span></span>

<span data-ttu-id="93e18-153">寫入中繼資料的程式與讀取的方式類似，差別在於使用中繼資料查詢寫入器 ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) 。</span><span class="sxs-lookup"><span data-stu-id="93e18-153">The process of writing metadata is similar to the way it is read except that a metadata query writer ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) is used.</span></span> <span data-ttu-id="93e18-154">查詢編寫器介面是由影像編碼器所執行，而且在查詢讀取器中，中繼資料會在編碼器和個別畫面上 (存取，視影像格式支援) 而定。</span><span class="sxs-lookup"><span data-stu-id="93e18-154">The query writer interface is implemented by the image encoder and, as in the query reader, metadata is accessed both on the encoder and on individual frames (depending on image format support).</span></span>

<span data-ttu-id="93e18-155">下列程式碼示範如何從編碼器框架取得查詢寫入器，並移除先前讀取的分級值。</span><span class="sxs-lookup"><span data-stu-id="93e18-155">The following code demonstrates how to obtain a query writer from an encoder frame and remove the rating value that was previously read.</span></span>


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



<span data-ttu-id="93e18-156">寫入中繼資料的另一種方式是透過快速中繼資料更新。</span><span class="sxs-lookup"><span data-stu-id="93e18-156">Another way to write metadata is through fast metadata updates.</span></span> <span data-ttu-id="93e18-157">快速中繼資料編碼是一種寫入影像中繼資料的方式，而不需要重新編碼影像檔案。</span><span class="sxs-lookup"><span data-stu-id="93e18-157">Fast metadata encoding is a way to write image metadata without having to re-encode an image file.</span></span> <span data-ttu-id="93e18-158">這是藉由將新的中繼資料資訊寫入元資料格式的填補區域來完成。</span><span class="sxs-lookup"><span data-stu-id="93e18-158">This is done by writing new metadata information to a padded region of the metadata format.</span></span> <span data-ttu-id="93e18-159">快速中繼資料編碼器 ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) 是從元件 factory 取得（以映射編碼器為基礎）。</span><span class="sxs-lookup"><span data-stu-id="93e18-159">The fast metadata encoder ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) is obtained from the component factory, based on the image decoder.</span></span> <span data-ttu-id="93e18-160">快速中繼資料編碼器接著會取得用來寫入中繼資料的查詢寫入器。</span><span class="sxs-lookup"><span data-stu-id="93e18-160">The fast metadata encoder then obtains a query writer that is used to write the metadata.</span></span> <span data-ttu-id="93e18-161">最後，快速編碼器會認可變更。</span><span class="sxs-lookup"><span data-stu-id="93e18-161">Finally, the fast encoder commits the change.</span></span>

<span data-ttu-id="93e18-162">下列程式碼示範如何取得快速的中繼資料編碼器，並使用它來寫入 MicrosoftRating 值。</span><span class="sxs-lookup"><span data-stu-id="93e18-162">The following code demonstrates how to obtain a fast metadata encoder and use it to write the MicrosoftRating value.</span></span>


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

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



<span data-ttu-id="93e18-163">並非所有的元資料格式都支援快速中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-163">Not all metadata formats support fast metadata.</span></span> <span data-ttu-id="93e18-164">若要查看支援快速中繼資料編碼的原生支援格式，請參閱本檔稍後的 [支援的元資料格式](#supported-metadata-formats) 一節中的表格。</span><span class="sxs-lookup"><span data-stu-id="93e18-164">To see which natively supported formats support fast metadata encoding, see the table in the [Supported Metadata Formats](#supported-metadata-formats) section later in this document.</span></span>

<span data-ttu-id="93e18-165">在幕後，查詢寫入器會使用中繼資料寫入器 ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 來寫入查詢運算式所描述的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-165">Behind the scenes, a query writer uses a metadata writer ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) to write the metadata described by the query expression.</span></span> <span data-ttu-id="93e18-166">除了使用查詢讀取器之外，您也可以直接存取中繼資料寫入器來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-166">In addition to using a query reader, you can also access a metadata writer directly to write metadata.</span></span> <span data-ttu-id="93e18-167">您可以使用查詢區塊寫入器 ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) 介面，從解碼器或個別的框架取得中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="93e18-167">You can obtain a metadata writer from the decoder or individual frames using querying for a block writer ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)) interface.</span></span>

## <a name="metadata-extensibility"></a><span data-ttu-id="93e18-168">中繼資料擴充性</span><span class="sxs-lookup"><span data-stu-id="93e18-168">Metadata Extensibility</span></span>

<span data-ttu-id="93e18-169">如先前所述，WIC 提供數個元資料處理程式來讀取和寫入一般元資料格式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-169">As mentioned previously, WIC provides several metadata handlers to read and write metadata for common metadata formats.</span></span> <span data-ttu-id="93e18-170">不過，有些元資料格式並非原生支援。</span><span class="sxs-lookup"><span data-stu-id="93e18-170">However, there are some metadata formats that are not natively supported.</span></span> <span data-ttu-id="93e18-171">因此，WIC 會提供 Api 來建立可將中繼資料支援延伸至其他格式的其他元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="93e18-171">Therefore, WIC provides APIs for creating additional metadata handlers that can extend metadata support to other formats.</span></span>

<span data-ttu-id="93e18-172">若要完全支援其他元資料格式，必須開發兩種類型的處理常式：中繼資料讀取器，用來讀取中繼資料和中繼資料寫入器來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-172">To fully support other metadata formats, two types of handlers must be developed — a metadata reader to read metadata and a metadata writer to write metadata.</span></span> <span data-ttu-id="93e18-173">雖然這兩個處理常式通常會以特定格式的配對來執行，但這不是必要條件。</span><span class="sxs-lookup"><span data-stu-id="93e18-173">Although these two handlers are usually implemented in pairs for a specific format, that is not a requirement.</span></span> <span data-ttu-id="93e18-174">在某些情況下，可能只有讀取能力或只需要寫入功能。</span><span class="sxs-lookup"><span data-stu-id="93e18-174">There might be some cases in which only the read ability or only the write ability is needed.</span></span>

<span data-ttu-id="93e18-175">如需有關使用 WIC Api 的中繼資料擴充性的詳細資訊，請參閱 [中繼資料](-wic-codec-metadatahandlers.md)擴充性總覽。</span><span class="sxs-lookup"><span data-stu-id="93e18-175">For more information on metadata extensibility using the WIC APIs, see the [Metadata Extensibility Overview](-wic-codec-metadatahandlers.md).</span></span>

## <a name="supported-metadata-formats"></a><span data-ttu-id="93e18-176">支援的元資料格式</span><span class="sxs-lookup"><span data-stu-id="93e18-176">Supported Metadata Formats</span></span>

<span data-ttu-id="93e18-177">WIC 提供數種常見元資料格式的支援。</span><span class="sxs-lookup"><span data-stu-id="93e18-177">WIC provides support for several common metadata formats.</span></span> <span data-ttu-id="93e18-178">下表列出支援的元資料格式、其版本、支援元資料格式的影像格式，以及元資料格式是否支援快速中繼資料編碼。</span><span class="sxs-lookup"><span data-stu-id="93e18-178">The following table lists the supported metadata formats, their versions, the image formats that support the metadata format, and whether the metadata format supports fast metadata encoding.</span></span> <span data-ttu-id="93e18-179">如需快速中繼資料編碼的詳細資訊，請參閱本檔稍早的「 [撰寫映射中繼資料](#writing-image-metadata) 」一節。</span><span class="sxs-lookup"><span data-stu-id="93e18-179">For more information about fast metadata encoding, see the [Writing Image Metadata](#writing-image-metadata) section earlier in this document.</span></span>



| <span data-ttu-id="93e18-180">支援的元資料格式</span><span class="sxs-lookup"><span data-stu-id="93e18-180">Supported metadata formats</span></span> | <span data-ttu-id="93e18-181">中繼資料規格版本</span><span class="sxs-lookup"><span data-stu-id="93e18-181">Metadata specification version</span></span> | <span data-ttu-id="93e18-182">影像格式支援</span><span class="sxs-lookup"><span data-stu-id="93e18-182">Image format support</span></span> | <span data-ttu-id="93e18-183">支援快速中繼資料編碼</span><span class="sxs-lookup"><span data-stu-id="93e18-183">Supports fast metadata encoding</span></span> |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| <span data-ttu-id="93e18-184">App0</span><span class="sxs-lookup"><span data-stu-id="93e18-184">App0</span></span>                       | <span data-ttu-id="93e18-185">JFIF 1.02</span><span class="sxs-lookup"><span data-stu-id="93e18-185">JFIF 1.02</span></span>                      | <span data-ttu-id="93e18-186">JPEG</span><span class="sxs-lookup"><span data-stu-id="93e18-186">JPEG</span></span>                 | <span data-ttu-id="93e18-187">No</span><span class="sxs-lookup"><span data-stu-id="93e18-187">No</span></span>                              |
| <span data-ttu-id="93e18-188">App1</span><span class="sxs-lookup"><span data-stu-id="93e18-188">App1</span></span>                       | <span data-ttu-id="93e18-189">JFIF 1.02</span><span class="sxs-lookup"><span data-stu-id="93e18-189">JFIF 1.02</span></span>                      | <span data-ttu-id="93e18-190">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-190">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-191">No</span><span class="sxs-lookup"><span data-stu-id="93e18-191">No</span></span>                              |
| <span data-ttu-id="93e18-192">App13</span><span class="sxs-lookup"><span data-stu-id="93e18-192">App13</span></span>                      | <span data-ttu-id="93e18-193">Unknown</span><span class="sxs-lookup"><span data-stu-id="93e18-193">Unknown</span></span>                        | <span data-ttu-id="93e18-194">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-194">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-195">No</span><span class="sxs-lookup"><span data-stu-id="93e18-195">No</span></span>                              |
| <span data-ttu-id="93e18-196">IFD</span><span class="sxs-lookup"><span data-stu-id="93e18-196">IFD</span></span>                        | <span data-ttu-id="93e18-197">TIFF 6。0</span><span class="sxs-lookup"><span data-stu-id="93e18-197">TIFF 6.0</span></span>                       | <span data-ttu-id="93e18-198">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-198">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-199">Yes</span><span class="sxs-lookup"><span data-stu-id="93e18-199">Yes</span></span>                             |
| <span data-ttu-id="93e18-200">Irb</span><span class="sxs-lookup"><span data-stu-id="93e18-200">IRB</span></span>                        | <span data-ttu-id="93e18-201">Unknown</span><span class="sxs-lookup"><span data-stu-id="93e18-201">Unknown</span></span>                        | <span data-ttu-id="93e18-202">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-202">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-203">No</span><span class="sxs-lookup"><span data-stu-id="93e18-203">No</span></span>                              |
| <span data-ttu-id="93e18-204">Exif</span><span class="sxs-lookup"><span data-stu-id="93e18-204">Exif</span></span>                       | <span data-ttu-id="93e18-205">Exif 2。2</span><span class="sxs-lookup"><span data-stu-id="93e18-205">Exif 2.2</span></span>                       | <span data-ttu-id="93e18-206">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-206">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-207">Yes</span><span class="sxs-lookup"><span data-stu-id="93e18-207">Yes</span></span>                             |
| <span data-ttu-id="93e18-208">XMP</span><span class="sxs-lookup"><span data-stu-id="93e18-208">XMP</span></span>                        | <span data-ttu-id="93e18-209">XMP 1.0 (9 月 2005) </span><span class="sxs-lookup"><span data-stu-id="93e18-209">XMP 1.0 (Sept 2005)</span></span>            | <span data-ttu-id="93e18-210">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-210">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-211">Yes</span><span class="sxs-lookup"><span data-stu-id="93e18-211">Yes</span></span>                             |
| <span data-ttu-id="93e18-212">GPS</span><span class="sxs-lookup"><span data-stu-id="93e18-212">GPS</span></span>                        | <span data-ttu-id="93e18-213">Exif 2。2</span><span class="sxs-lookup"><span data-stu-id="93e18-213">Exif 2.2</span></span>                       | <span data-ttu-id="93e18-214">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-214">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-215">Yes</span><span class="sxs-lookup"><span data-stu-id="93e18-215">Yes</span></span>                             |
| <span data-ttu-id="93e18-216">IPTC</span><span class="sxs-lookup"><span data-stu-id="93e18-216">IPTC</span></span>                       | <span data-ttu-id="93e18-217">IPTC 4。0</span><span class="sxs-lookup"><span data-stu-id="93e18-217">IPTC 4.0</span></span>                       | <span data-ttu-id="93e18-218">JPEG、TIFF</span><span class="sxs-lookup"><span data-stu-id="93e18-218">JPEG, TIFF</span></span>           | <span data-ttu-id="93e18-219">Yes</span><span class="sxs-lookup"><span data-stu-id="93e18-219">Yes</span></span>                             |
| <span data-ttu-id="93e18-220">文本</span><span class="sxs-lookup"><span data-stu-id="93e18-220">tEXt</span></span>                       | <span data-ttu-id="93e18-221">PNG 1。2</span><span class="sxs-lookup"><span data-stu-id="93e18-221">PNG 1.2</span></span>                        | <span data-ttu-id="93e18-222">PNG</span><span class="sxs-lookup"><span data-stu-id="93e18-222">PNG</span></span>                  | <span data-ttu-id="93e18-223">No</span><span class="sxs-lookup"><span data-stu-id="93e18-223">No</span></span>                              |



 

> [!Note]  
> <span data-ttu-id="93e18-224">如果區塊的大小成長，則 IPTC 只支援 FME，因為 IPTC 不支援填補。</span><span class="sxs-lookup"><span data-stu-id="93e18-224">IPTC only supports FME if the blocks grow in size, as IPTC does not support padding.</span></span>

 

## <a name="metadata-component-summary"></a><span data-ttu-id="93e18-225">中繼資料元件摘要</span><span class="sxs-lookup"><span data-stu-id="93e18-225">Metadata Component Summary</span></span>

<span data-ttu-id="93e18-226">下表描述支援中繼資料的 WIC 介面，以及其對應的元件。</span><span class="sxs-lookup"><span data-stu-id="93e18-226">The following table describes the WIC interfaces that support metadata, and their corresponding components.</span></span> <span data-ttu-id="93e18-227">這些元件提供映射中繼資料的存取權。</span><span class="sxs-lookup"><span data-stu-id="93e18-227">These components provide the access to an image's metadata.</span></span> <span data-ttu-id="93e18-228">如需這些元件的詳細資訊，請參閱 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)。</span><span class="sxs-lookup"><span data-stu-id="93e18-228">For more information about these components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93e18-229">元件</span><span class="sxs-lookup"><span data-stu-id="93e18-229">Component</span></span></th>
<th><span data-ttu-id="93e18-230">描述</span><span class="sxs-lookup"><span data-stu-id="93e18-230">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93e18-231">點陣圖解碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-231">Bitmap Decoder (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-232">讀取影像資料流程並產生可用的點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="93e18-232">Reads an image stream and produces a usable bitmap source.</span></span> <span data-ttu-id="93e18-233">與容器格式相關聯，例如標記的影像檔案格式 (TIFF) 或 (JPEG) 的聯合攝影專家群組。</span><span class="sxs-lookup"><span data-stu-id="93e18-233">Associated with a container format such as Tagged Image File Format (TIFF) or Joint Photographic Experts Group (JPEG).</span></span></li>
<li><span data-ttu-id="93e18-234">執行 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> 介面，以列舉不在框架內的解碼器資料流程中的所有中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="93e18-234">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the decoder's data stream that are not inside a frame.</span></span></li>
<li><span data-ttu-id="93e18-235">公開查詢讀取器，以讀取與不在框架內的影像相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-235">Exposes a query reader to read the metadata associated with the image that is not inside a frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e18-236">點陣圖框架解碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-236">Bitmap Frame Decode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-237">從解碼器所持有的影像串流存取個別的畫面格。</span><span class="sxs-lookup"><span data-stu-id="93e18-237">Accesses individual frames from the image stream held by the decoder.</span></span></li>
<li><span data-ttu-id="93e18-238">實 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> 介面，以列舉框架資料流程中的所有中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="93e18-238">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> interface to enumerate all of the metadata blocks in the frame's data stream.</span></span></li>
<li><span data-ttu-id="93e18-239">使用查詢運算式來公開查詢讀取器，以讀取與框架相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-239">Exposes a query reader to read the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93e18-240">點陣圖編碼器 (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-240">Bitmap Encoder (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-241">將點陣圖來源寫入影像資料流程。</span><span class="sxs-lookup"><span data-stu-id="93e18-241">Writes a bitmap source to an image stream.</span></span> <span data-ttu-id="93e18-242">與容器格式相關聯，例如 TIFF 或 JPEG。</span><span class="sxs-lookup"><span data-stu-id="93e18-242">Associated with a container format such as TIFF or JPEG.</span></span></li>
<li><span data-ttu-id="93e18-243">執行 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> 介面，以建立要寫入編碼器資料流程的中繼資料區塊清單。</span><span class="sxs-lookup"><span data-stu-id="93e18-243">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the data stream of the encoder.</span></span></li>
<li><span data-ttu-id="93e18-244">使用查詢運算式，公開查詢寫入器來寫入與影像相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-244">Exposes a query writer to write the metadata associated with the image, using query expressions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e18-245">Bitma 框架編碼 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-245">Bitma Frame Encode (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-246">建立將編碼為編碼器所持有之資料流程的框架。</span><span class="sxs-lookup"><span data-stu-id="93e18-246">Creates a frame that will be encoded into the stream held by the encoder.</span></span></li>
<li><span data-ttu-id="93e18-247">實 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> 介面，以建立要寫入框架資料流程的中繼資料區塊清單。</span><span class="sxs-lookup"><span data-stu-id="93e18-247">Implements an <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> interface to build up a list of metadata blocks to write into the frame's data stream.</span></span></li>
<li><span data-ttu-id="93e18-248">使用查詢運算式，公開查詢寫入器來寫入與框架相關聯的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-248">Exposes a query writer to write the metadata associated with the frame, using query expressions.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="93e18-249">下表描述 WIC 中繼資料元件。</span><span class="sxs-lookup"><span data-stu-id="93e18-249">The following table describes the WIC metadata components.</span></span> <span data-ttu-id="93e18-250">這些元件可讓您在上表所列的元件所公開的影像中讀取和寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-250">These components enable you to read and write the metadata in an image exposed by the components listed in the previous table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93e18-251">元件</span><span class="sxs-lookup"><span data-stu-id="93e18-251">Component</span></span></th>
<th><span data-ttu-id="93e18-252">描述</span><span class="sxs-lookup"><span data-stu-id="93e18-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93e18-253">中繼資料查詢讀取器 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-253">Metadata Query Reader (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-254">接受查詢字串，並流覽基礎中繼資料階層以取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-254">Takes a query string and navigates the underlying metadata hierarchy to get metadata.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e18-255">中繼資料查詢寫入器 (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-255">Metadata Query Writer (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-256">接受查詢字串，並流覽基礎中繼資料階層以取得、設定和移除中繼資料。</span><span class="sxs-lookup"><span data-stu-id="93e18-256">Takes a query string and navigates the underlying metadata hierarchy to get, set, and remove metadata.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93e18-257">中繼資料區塊讀取器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-257">Metadata Block Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-258">管理位於中繼資料階層最上方之 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> 物件的唯讀集合，並啟用所有中繼資料區塊的列舉。</span><span class="sxs-lookup"><span data-stu-id="93e18-258">Manages a read-only collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> objects at the top of the metadata hierarchy and enables enumeration of all metadata blocks.</span></span></li>
<li><span data-ttu-id="93e18-259">由點陣圖解碼器和解碼點陣圖框架所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-259">Implemented by a bitmap decoder and a decoded bitmap frame.</span></span></li>
<li><span data-ttu-id="93e18-260">由協力廠商元件開發人員為自訂編解碼器所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-260">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e18-261">中繼資料區塊寫入器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-261">Metadata Block Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-262">管理中繼資料階層頂端 <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> 物件的讀取和寫入集合。</span><span class="sxs-lookup"><span data-stu-id="93e18-262">Manages a read and write collection of <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> objects at the top of the metadata hierarchy.</span></span></li>
<li><span data-ttu-id="93e18-263">由點陣圖編碼器和點陣圖框架編碼所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-263">Implemented by a bitmap encoder and a bitmap frame encode.</span></span></li>
<li><span data-ttu-id="93e18-264">由協力廠商元件開發人員為自訂編解碼器所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-264">Implemented by third-party component developers for custom codecs.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93e18-265">中繼資料讀取器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-265">Metadata Reader (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-266">剖析中繼資料的資料流程，並管理中繼資料專案的唯讀集合。</span><span class="sxs-lookup"><span data-stu-id="93e18-266">Parses a stream of metadata and manages a read-only collection of the metadata items.</span></span> <span data-ttu-id="93e18-267">與元資料格式（如 EXIF、IFD 和 XMP）相關聯。</span><span class="sxs-lookup"><span data-stu-id="93e18-267">Associated with a metadata format such as EXIF, IFD, and XMP.</span></span></li>
<li><span data-ttu-id="93e18-268">作為字典，並在給定格式和識別碼時傳回值。</span><span class="sxs-lookup"><span data-stu-id="93e18-268">Acts as a dictionary, returning a value when given a format and ID pair.</span></span></li>
<li><span data-ttu-id="93e18-269">由自訂元資料類型的協力廠商元件開發人員所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-269">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93e18-270">中繼資料寫入器 (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>) </span><span class="sxs-lookup"><span data-stu-id="93e18-270">Metadata Writer (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-271">剖析和序列化中繼資料的資料流程，並管理中繼資料專案的讀取/寫入集合。</span><span class="sxs-lookup"><span data-stu-id="93e18-271">Parses and serializes a stream of metadata and manages a read/write collection of metadata items.</span></span></li>
<li><span data-ttu-id="93e18-272">由自訂元資料類型的協力廠商元件開發人員所執行。</span><span class="sxs-lookup"><span data-stu-id="93e18-272">Implemented by third-party component developers for custom metadata types.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93e18-273">快速中繼資料編碼器<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="93e18-273">Fast Metadata Encoder<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong>IWICFastMetadataEncoder</strong></a></span></span></td>
<td><ul>
<li><span data-ttu-id="93e18-274">公開寫入中繼資料階層的語義，這些中繼資料會就地更新中繼資料，而不需要重新編碼影像。</span><span class="sxs-lookup"><span data-stu-id="93e18-274">Exposes semantics for writing on a metadata hierarchy that will update metadata in place without re-encoding the image.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="93e18-275">相關主題</span><span class="sxs-lookup"><span data-stu-id="93e18-275">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="93e18-276">**概念**</span><span class="sxs-lookup"><span data-stu-id="93e18-276">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="93e18-277">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="93e18-277">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="93e18-278">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="93e18-278">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="93e18-279">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="93e18-279">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="93e18-280">中繼資料擴充性總覽</span><span class="sxs-lookup"><span data-stu-id="93e18-280">Metadata Extensibility Overview</span></span>](-wic-codec-metadatahandlers.md)
</dt> <dt>

[<span data-ttu-id="93e18-281">How to：使用中繼資料重新編碼 JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="93e18-281">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



