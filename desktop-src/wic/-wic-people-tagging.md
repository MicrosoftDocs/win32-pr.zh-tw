---
description: 本主題將介紹新的可延伸中繼資料平臺 (XMP) 架構和 Windows 7 相片屬性 PeopleNames，可讓您在數位相片中標記個人。
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: 人員標記總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115777"
---
# <a name="people-tagging-overview"></a><span data-ttu-id="89c55-103">人員標記總覽</span><span class="sxs-lookup"><span data-stu-id="89c55-103">People Tagging Overview</span></span>

<span data-ttu-id="89c55-104">本主題將介紹新的可延伸中繼資料平臺 (XMP) 架構和 Windows 7 相片屬性 [PeopleNames](../properties/props-system-photo-peoplenames.md) ，可讓您在數位相片中標記個人。</span><span class="sxs-lookup"><span data-stu-id="89c55-104">This topic introduces the new Extensible Metadata Platform (XMP) schema and the Windows 7 photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) that enables the tagging of individuals in a digital photo.</span></span> <span data-ttu-id="89c55-105">本主題也會討論如何使用 Windows 影像處理元件 (WIC) API 來讀取和寫入人員標記所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="89c55-105">This topic also discusses how to use the Windows Imaging Component (WIC) API to both read and write the metadata needed for people tagging.</span></span>

<span data-ttu-id="89c55-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="89c55-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="89c55-107">先決條件</span><span class="sxs-lookup"><span data-stu-id="89c55-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="89c55-108">簡介</span><span class="sxs-lookup"><span data-stu-id="89c55-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="89c55-109">人員標記</span><span class="sxs-lookup"><span data-stu-id="89c55-109">People Tagging</span></span>](#people-tagging-overview)
    -   [<span data-ttu-id="89c55-110">人員名稱</span><span class="sxs-lookup"><span data-stu-id="89c55-110">People Names</span></span>](#people-names)
    -   [<span data-ttu-id="89c55-111">人員矩形</span><span class="sxs-lookup"><span data-stu-id="89c55-111">People Rectangles</span></span>](#people-rectangles)
-   [<span data-ttu-id="89c55-112">架構參考</span><span class="sxs-lookup"><span data-stu-id="89c55-112">Schema Reference</span></span>](#schema-reference)
    -   [<span data-ttu-id="89c55-113">Microsoft Photo 1.2 架構</span><span class="sxs-lookup"><span data-stu-id="89c55-113">Microsoft Photo 1.2 Schema</span></span>](#microsoft-photo-12-schema)
    -   [<span data-ttu-id="89c55-114">Microsoft Photo RegionInfo 架構</span><span class="sxs-lookup"><span data-stu-id="89c55-114">Microsoft Photo RegionInfo Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="89c55-115">Microsoft 相片區域架構</span><span class="sxs-lookup"><span data-stu-id="89c55-115">Microsoft Photo Region Schema</span></span>](#microsoft-photo-regioninfo-schema)
    -   [<span data-ttu-id="89c55-116">範例中繼資料</span><span class="sxs-lookup"><span data-stu-id="89c55-116">Sample Metadata</span></span>](#sample-metadata)
-   [<span data-ttu-id="89c55-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="89c55-117">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="89c55-118">必要條件</span><span class="sxs-lookup"><span data-stu-id="89c55-118">Prerequisites</span></span>

<span data-ttu-id="89c55-119">若要瞭解本主題，您應該熟悉 WIC 解碼介面及其相關元件物件模型 (COM) 元件，如 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)所述。</span><span class="sxs-lookup"><span data-stu-id="89c55-119">To understand this topic, you should be familiar with the WIC decoder interfaces and its related Component Object Model (COM) components, as described in the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span> <span data-ttu-id="89c55-120">它也有助於對影像處理中繼資料（尤其是 XMP）有大致熟悉。</span><span class="sxs-lookup"><span data-stu-id="89c55-120">It also helps to have a general familiarity with imaging metadata, especially XMP.</span></span>

## <a name="introduction"></a><span data-ttu-id="89c55-121">簡介</span><span class="sxs-lookup"><span data-stu-id="89c55-121">Introduction</span></span>

<span data-ttu-id="89c55-122">Microsoft 建立了新的 XMP 架構來標記數位影像內的人員。</span><span class="sxs-lookup"><span data-stu-id="89c55-122">Microsoft has created a new XMP schema for tagging people within a digital image.</span></span> <span data-ttu-id="89c55-123">此架構可讓應用程式將影像中的個人名稱和位置，儲存為影像內的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="89c55-123">This schema enables applications to store the names and locations of individuals who are in the image as metadata within the image.</span></span> <span data-ttu-id="89c55-124">除了新的架構，Windows 7 也提供新的相片屬性 [PeopleNames](../properties/props-system-photo-peoplenames.md) 。</span><span class="sxs-lookup"><span data-stu-id="89c55-124">In addition to the new schema, the new photo property [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) is available in Windows 7.</span></span> <span data-ttu-id="89c55-125">這個新的屬性可讓應用程式讀取儲存在影像中繼資料中的個人名稱。</span><span class="sxs-lookup"><span data-stu-id="89c55-125">This new property enables applications to read the individual's names stored in the image metadata.</span></span> <span data-ttu-id="89c55-126">WIC 利用這些新功能，可讓應用程式輕鬆地讀取和寫入人員標記中繼資料到數位相片。</span><span class="sxs-lookup"><span data-stu-id="89c55-126">WIC utilizes these new features by enabling applications to easily read and write people tagging metadata to digital photos.</span></span>

## <a name="people-tagging"></a><span data-ttu-id="89c55-127">人員標記</span><span class="sxs-lookup"><span data-stu-id="89c55-127">People Tagging</span></span>

<span data-ttu-id="89c55-128">WIC 為應用程式開發人員提供讀取影像資料和影像中繼資料的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="89c55-128">WIC provides application developers with COM components which read image data as well as image metadata.</span></span> <span data-ttu-id="89c55-129">針對讀取和寫入中繼資料（例如新的人員標記功能），WIC 提供 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 和 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="89c55-129">For reading and writing metadata, such as the new people tagging feature, WIC provides the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) and [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interfaces.</span></span> <span data-ttu-id="89c55-130">這些介面可讓應用程式使用 [中繼資料查詢語言](-wic-codec-metadataquerylanguage.md) ，將中繼資料寫入影像的個別框架。</span><span class="sxs-lookup"><span data-stu-id="89c55-130">These interfaces enable applications to use the [metadata query language](-wic-codec-metadataquerylanguage.md) to write metadata to the individual frames of an image.</span></span> <span data-ttu-id="89c55-131">下一節示範如何使用 WIC 查詢讀取器和寫入器，將人員標記中繼資料讀取及寫入影像的中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="89c55-131">The following section demonstrates how to read and write the people-tagging metadata into an image's metadata by using WIC query readers and writers.</span></span>

### <a name="people-names"></a><span data-ttu-id="89c55-132">人員名稱</span><span class="sxs-lookup"><span data-stu-id="89c55-132">People Names</span></span>

<span data-ttu-id="89c55-133">人物標記功能的一部分，就是能夠直接取得在影像內標記的人員名稱清單。</span><span class="sxs-lookup"><span data-stu-id="89c55-133">Part of the people-tagging feature is the ability to simply get a list the names of the people tagged within the image.</span></span> <span data-ttu-id="89c55-134">[PeopleNames](../properties/props-system-photo-peoplenames.md)和 WIC 的元資料處理程式都支援這部分的功能。</span><span class="sxs-lookup"><span data-stu-id="89c55-134">This part of the feature is supported by the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) and WIC's metadata handlers.</span></span> <span data-ttu-id="89c55-135">[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)介面與 PeopleNames 屬性搭配使用，可讀取影像中所識別的人員名稱，並儲存在影像中繼資料中。</span><span class="sxs-lookup"><span data-stu-id="89c55-135">The [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) interface, in conjunction with the System.Photo.PeopleNames property, are used to read the names of people identified in an image and stored in the image metadata.</span></span>

<span data-ttu-id="89c55-136">下列程式碼範例示範從影像框架取得的查詢讀取器，以查詢影像的中繼資料是否有 [PeopleNames](../properties/props-system-photo-peoplenames.md) 屬性的標記名稱。</span><span class="sxs-lookup"><span data-stu-id="89c55-136">The following code example demonstrates a query reader obtained from an image frame to query an image's metadata for tagged names of the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



<span data-ttu-id="89c55-137">查詢運算式 "PeopleNames" 會查詢屬性的框架。</span><span class="sxs-lookup"><span data-stu-id="89c55-137">The query expression "System.Photo.PeopleNames" queries the frame for the property.</span></span> <span data-ttu-id="89c55-138">如果人物標記中繼資料存在且包含人員的名稱， [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 值將會設定為 VT LPWSTR， \_ 而且資料值將會包含已標記名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="89c55-138">If the people-tagging metadata exists and contains people's names, the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value will be set to VT\_LPWSTR and the data value will contain the list of tagged names.</span></span> <span data-ttu-id="89c55-139">如需有關讀取影像中繼資料的詳細資訊，請參閱 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)。</span><span class="sxs-lookup"><span data-stu-id="89c55-139">For more information on reading image metadata, see [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

<span data-ttu-id="89c55-140">如果影像實際包含人物標記中繼資料，則查詢 [人員名稱] 標籤只會很有用。</span><span class="sxs-lookup"><span data-stu-id="89c55-140">Querying for the people names tag is only useful if the image actually contains the people-tagging metadata.</span></span> <span data-ttu-id="89c55-141">若要執行此程式，應用程式必須先撰寫它。</span><span class="sxs-lookup"><span data-stu-id="89c55-141">For this to occur, an application must first have written it.</span></span> <span data-ttu-id="89c55-142">若要撰寫人員名稱中繼資料，請使用中繼資料的 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 和明確的 XMP 路徑。</span><span class="sxs-lookup"><span data-stu-id="89c55-142">To write the people names metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="89c55-143">下列程式碼範例將示範如何使用查詢寫入器，將名稱寫入至查詢路徑。</span><span class="sxs-lookup"><span data-stu-id="89c55-143">The following code example demonstrates using a query writer to write a name to the query path.</span></span>


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



<span data-ttu-id="89c55-144">請注意建立 XMP 結構並設定它的步驟 `MPRI:Regions/{ulong=0}` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-144">Note the step constructing the XMP structure and setting it under `MPRI:Regions/{ulong=0}`.</span></span> <span data-ttu-id="89c55-145">若未執行此步驟，WIC 將無法識別稍後要放置的位置 `PersonDisplayName` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-145">Without this step, the WIC can't identify where to place the `PersonDisplayName` later on.</span></span> <span data-ttu-id="89c55-146">另請注意，系統會使用明確的查詢路徑，而不是 [PeopleNames](-wic-photoprop-system-photo-peoplenames.md)，其中繼資料原則不支援寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="89c55-146">Also note that the explicit query path is used instead of [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md), whose metadata policy does not support writing metadata.</span></span>

### <a name="people-rectangles"></a><span data-ttu-id="89c55-147">人員矩形</span><span class="sxs-lookup"><span data-stu-id="89c55-147">People Rectangles</span></span>

<span data-ttu-id="89c55-148">不過，人們的名字只是人員標記功能的一部分。</span><span class="sxs-lookup"><span data-stu-id="89c55-148">People's names however, are only part of the people-tagging feature.</span></span> <span data-ttu-id="89c55-149">除了在中繼資料中儲存人員的名稱之外，架構也支援區域資訊，識別特定區域 (矩形) 該人員顯示于影像中。</span><span class="sxs-lookup"><span data-stu-id="89c55-149">In addition to storing people's names in the metadata, the schema also supports region information that identifies the specific area (a rectangle) the person is shown in the image.</span></span>

<span data-ttu-id="89c55-150">矩形資訊會以四個逗號分隔的十進位值來表示，例如 "0.25，0.25，0.25，0.25"。</span><span class="sxs-lookup"><span data-stu-id="89c55-150">The rectangle information is represented by four comma-delimited decimal values, such as "0.25, 0.25, 0.25, 0.25".</span></span> <span data-ttu-id="89c55-151">前兩個值指定左上角座標;最後兩個指定矩形的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="89c55-151">The first two values specify the top-left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="89c55-152">用來定義人物矩形的影像維度會正規化為1，這表示在 "0.25，0.25，0.25，0.25" 範例中，矩形會從影像左邊距離的上到上距離的距離開始的1/4。</span><span class="sxs-lookup"><span data-stu-id="89c55-152">The dimensions of the image for the purposes of defining people rectangles are normalized to 1, which means that in the "0.25, 0.25, 0.25, 0.25" example, the rectangle starts 1/4 of the distance from the top and 1/4 of the distance from the left of the image.</span></span> <span data-ttu-id="89c55-153">矩形的高度和寬度都是其個別影像維度大小的1/4。</span><span class="sxs-lookup"><span data-stu-id="89c55-153">Both the height and width of the rectangle are 1/4 of the size of their respective image dimensions.</span></span>

<span data-ttu-id="89c55-154">識別個人的矩形資訊會以與人員名稱相同的方式寫入，在相同的結構內。</span><span class="sxs-lookup"><span data-stu-id="89c55-154">The rectangle information that identifies individuals is written in the same way people's names are written, within the same structure.</span></span> <span data-ttu-id="89c55-155">若要撰寫矩形中繼資料，請使用中繼資料的 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 和明確的 XMP 路徑。</span><span class="sxs-lookup"><span data-stu-id="89c55-155">To write the rectangle metadata, use an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) and the explicit XMP path of the metadata.</span></span> <span data-ttu-id="89c55-156">下列程式碼範例會繼續上一個範例，並將代表 ' John Doe ' 的矩形加入至映射的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="89c55-156">The following code example continues the previous example and adds a rectangle representing 'John Doe' to the image's metadata.</span></span> <span data-ttu-id="89c55-157">請注意，它會使用相同的 `{ulong=0}` 索引，將這個矩形與 ' John Doe ' 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="89c55-157">Note that it uses the same `{ulong=0}` index to associate this rectangle with 'John Doe'.</span></span>


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a><span data-ttu-id="89c55-158">結構描述參考</span><span class="sxs-lookup"><span data-stu-id="89c55-158">Schema Reference</span></span>

<span data-ttu-id="89c55-159">適用于人員標記的 Microsoft XMP 架構會定義一組屬性，以在數位相片中標記個人。</span><span class="sxs-lookup"><span data-stu-id="89c55-159">The Microsoft XMP schemas for people tagging define a set of properties to tag individuals in digital photos.</span></span>

<span data-ttu-id="89c55-160">下列各節提供人員標記所需的架構定義。</span><span class="sxs-lookup"><span data-stu-id="89c55-160">The following sections provide the schema definitions needed for people tagging.</span></span> <span data-ttu-id="89c55-161">架構定義盡可能使用 Adobe 的可延伸中繼資料平臺所提供的慣例 [ (XMP) 規格](https://www.adobe.com/devnet/xmp/)。</span><span class="sxs-lookup"><span data-stu-id="89c55-161">Wherever possible, the schema definitions use the conventions provided by [Adobe's Extensible Metadata Platform (XMP) Specifications](https://www.adobe.com/devnet/xmp/).</span></span> <span data-ttu-id="89c55-162">本主題中的架構定義會顯示 XML 命名空間統一資源識別元 (URI) 來識別架構和慣用的架構命名空間前置詞，後面接著列出針對架構定義的所有屬性的資料表。</span><span class="sxs-lookup"><span data-stu-id="89c55-162">The schema definitions in this topic show the XML namespace Uniform Resource Identifier (URI) that identifies the schema and the preferred schema namespace prefix, followed by a table that lists all properties defined for the schema.</span></span> <span data-ttu-id="89c55-163">每個資料表都有下列資料行：</span><span class="sxs-lookup"><span data-stu-id="89c55-163">Each table has the following columns:</span></span>

-   <span data-ttu-id="89c55-164">**Property** -屬性的名稱，包括慣用的命名空間前置詞。</span><span class="sxs-lookup"><span data-stu-id="89c55-164">**Property** - The name of the property, including the preferred namespace prefix.</span></span>

-   <span data-ttu-id="89c55-165">**數值型別** -屬性的數值型別。</span><span class="sxs-lookup"><span data-stu-id="89c55-165">**Value type** - The value type of the property.</span></span> <span data-ttu-id="89c55-166">人員標記支援架構會盡可能使用 XMP 實數值型別，包括日期和文字。</span><span class="sxs-lookup"><span data-stu-id="89c55-166">The people-tagging support schemas use the XMP value types whenever possible, including Date and Text.</span></span> <span data-ttu-id="89c55-167">陣列類型的前面會有容器類型： `alt` 、 `bag` 或 `seq` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-167">Array types are preceded by the container type: `alt`, `bag`, or `seq`.</span></span>

-   <span data-ttu-id="89c55-168">**類別** 架構屬性是內部或外部：</span><span class="sxs-lookup"><span data-stu-id="89c55-168">**Category** - Schema properties are internal or external:</span></span>

    -   <span data-ttu-id="89c55-169">內部中繼資料必須由應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="89c55-169">Internal metadata must be set by the application.</span></span>

    -   <span data-ttu-id="89c55-170">外部中繼資料必須由使用者設定，而且與檔的內容無關。</span><span class="sxs-lookup"><span data-stu-id="89c55-170">External metadata must be set by the user and is independent of the contents of the document.</span></span>

-   <span data-ttu-id="89c55-171">**描述** -屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="89c55-171">**Description** - The description of the property.</span></span>

### <a name="microsoft-photo-12-schema"></a><span data-ttu-id="89c55-172">Microsoft Photo 1.2 架構</span><span class="sxs-lookup"><span data-stu-id="89c55-172">Microsoft Photo 1.2 Schema</span></span>

<span data-ttu-id="89c55-173">Microsoft Photo 1.2 架構為影像區域提供一組屬性。</span><span class="sxs-lookup"><span data-stu-id="89c55-173">The Microsoft Photo 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="89c55-174">架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-174">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/`.</span></span>
-   <span data-ttu-id="89c55-175">慣用的架構命名空間前置詞為 `MP` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-175">The preferred schema namespace prefix is `MP`.</span></span>



| <span data-ttu-id="89c55-176">屬性</span><span class="sxs-lookup"><span data-stu-id="89c55-176">Property</span></span>      | <span data-ttu-id="89c55-177">值類型</span><span class="sxs-lookup"><span data-stu-id="89c55-177">Value type</span></span> | <span data-ttu-id="89c55-178">類別</span><span class="sxs-lookup"><span data-stu-id="89c55-178">Category</span></span> | <span data-ttu-id="89c55-179">描述</span><span class="sxs-lookup"><span data-stu-id="89c55-179">Description</span></span>                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c55-180">MP： RegionInfo</span><span class="sxs-lookup"><span data-stu-id="89c55-180">MP:RegionInfo</span></span> | <span data-ttu-id="89c55-181">RegionInfo</span><span class="sxs-lookup"><span data-stu-id="89c55-181">RegionInfo</span></span> | <span data-ttu-id="89c55-182">內部</span><span class="sxs-lookup"><span data-stu-id="89c55-182">Internal</span></span> | <span data-ttu-id="89c55-183">**必要** ：儲存人物標記中繼資料的根目錄。</span><span class="sxs-lookup"><span data-stu-id="89c55-183">**required** : Stores the root of the people-tagging metadata.</span></span> <span data-ttu-id="89c55-184">請參閱下面的「Microsoft Photo RegionInfo 架構」一節。</span><span class="sxs-lookup"><span data-stu-id="89c55-184">See the Microsoft Photo RegionInfo Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-regioninfo-schema"></a><span data-ttu-id="89c55-185">Microsoft Photo RegionInfo 架構</span><span class="sxs-lookup"><span data-stu-id="89c55-185">Microsoft Photo RegionInfo Schema</span></span>

<span data-ttu-id="89c55-186">Microsoft Photo RegionInfo 1.2 架構會提供一組區域資訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="89c55-186">The Microsoft Photo RegionInfo 1.2 schema provides a set of properties for region info.</span></span>

-   <span data-ttu-id="89c55-187">架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-187">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/RegionInfo#`.</span></span>
-   <span data-ttu-id="89c55-188">慣用的架構命名空間前置詞為 `MPRI` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-188">The preferred schema namespace prefix is `MPRI`.</span></span>



| <span data-ttu-id="89c55-189">屬性</span><span class="sxs-lookup"><span data-stu-id="89c55-189">Property</span></span>              | <span data-ttu-id="89c55-190">值類型</span><span class="sxs-lookup"><span data-stu-id="89c55-190">Value type</span></span> | <span data-ttu-id="89c55-191">類別</span><span class="sxs-lookup"><span data-stu-id="89c55-191">Category</span></span> | <span data-ttu-id="89c55-192">描述</span><span class="sxs-lookup"><span data-stu-id="89c55-192">Description</span></span>                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c55-193">MPRI:DateRegionsValid</span><span class="sxs-lookup"><span data-stu-id="89c55-193">MPRI:DateRegionsValid</span></span> | <span data-ttu-id="89c55-194">Date</span><span class="sxs-lookup"><span data-stu-id="89c55-194">Date</span></span>       | <span data-ttu-id="89c55-195">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-195">External</span></span> | <span data-ttu-id="89c55-196">**選用** ：上次建立區域的日期。</span><span class="sxs-lookup"><span data-stu-id="89c55-196">**optional** : Date that the last region was created.</span></span>                                                          |
| <span data-ttu-id="89c55-197">MPRI：區域</span><span class="sxs-lookup"><span data-stu-id="89c55-197">MPRI:Regions</span></span>          | <span data-ttu-id="89c55-198">包區域</span><span class="sxs-lookup"><span data-stu-id="89c55-198">bag Region</span></span> | <span data-ttu-id="89c55-199">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-199">External</span></span> | <span data-ttu-id="89c55-200">**必要** ：儲存人物標記區域。</span><span class="sxs-lookup"><span data-stu-id="89c55-200">**required** : Stores the people tagging regions.</span></span> <span data-ttu-id="89c55-201">請參閱下面的「Microsoft 照片區域架構」一節。</span><span class="sxs-lookup"><span data-stu-id="89c55-201">See the Microsoft Photo Region Schema section which follows.</span></span> |



 

### <a name="microsoft-photo-region-schema"></a><span data-ttu-id="89c55-202">Microsoft 相片區域架構</span><span class="sxs-lookup"><span data-stu-id="89c55-202">Microsoft Photo Region Schema</span></span>

<span data-ttu-id="89c55-203">Microsoft Photo Region 1.2 架構為影像區域提供一組屬性。</span><span class="sxs-lookup"><span data-stu-id="89c55-203">The Microsoft Photo Region 1.2 schema provides a set of properties for image regions.</span></span>

-   <span data-ttu-id="89c55-204">架構命名空間 URI 為 `https://ns.microsoft.com/photo/1.2/t/Region#` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-204">The schema namespace URI is `https://ns.microsoft.com/photo/1.2/t/Region#`.</span></span>
-   <span data-ttu-id="89c55-205">慣用的架構命名空間前置詞為 `MPReg` 。</span><span class="sxs-lookup"><span data-stu-id="89c55-205">The preferred schema namespace prefix is `MPReg`.</span></span>



| <span data-ttu-id="89c55-206">MPReg：屬性</span><span class="sxs-lookup"><span data-stu-id="89c55-206">MPReg:Property</span></span>          | <span data-ttu-id="89c55-207">值類型</span><span class="sxs-lookup"><span data-stu-id="89c55-207">Value type</span></span> | <span data-ttu-id="89c55-208">類別</span><span class="sxs-lookup"><span data-stu-id="89c55-208">Category</span></span> | <span data-ttu-id="89c55-209">描述</span><span class="sxs-lookup"><span data-stu-id="89c55-209">Description</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c55-210">MPReg:PersonDisplayName</span><span class="sxs-lookup"><span data-stu-id="89c55-210">MPReg:PersonDisplayName</span></span> | <span data-ttu-id="89c55-211">Text</span><span class="sxs-lookup"><span data-stu-id="89c55-211">Text</span></span>       | <span data-ttu-id="89c55-212">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-212">External</span></span> | <span data-ttu-id="89c55-213">**必要** ：將人員的名稱儲存在指定的矩形中。</span><span class="sxs-lookup"><span data-stu-id="89c55-213">**required** : Stores the name of the person in the given rectangle.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="89c55-214">MPReg：矩形</span><span class="sxs-lookup"><span data-stu-id="89c55-214">MPReg:Rectangle</span></span>         | <span data-ttu-id="89c55-215">Text</span><span class="sxs-lookup"><span data-stu-id="89c55-215">Text</span></span>       | <span data-ttu-id="89c55-216">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-216">External</span></span> | <span data-ttu-id="89c55-217">**選擇性** ：儲存用來識別相片中人員的矩形。</span><span class="sxs-lookup"><span data-stu-id="89c55-217">**optional** : Stores the rectangle that identifies the person within the photo.</span></span> <span data-ttu-id="89c55-218">矩形會儲存為四個以逗號分隔的十進位值。</span><span class="sxs-lookup"><span data-stu-id="89c55-218">The rectangle is stored as four comma-delimited decimal values.</span></span> <span data-ttu-id="89c55-219">前兩個值會指定左上角座標;最後兩個指定矩形的高度和寬度。</span><span class="sxs-lookup"><span data-stu-id="89c55-219">The first two values specify the top left coordinate; the final two specify the height and width of the rectangle.</span></span> <span data-ttu-id="89c55-220">十進位值必須正規化為1。</span><span class="sxs-lookup"><span data-stu-id="89c55-220">The decimal values must be normalized to 1.</span></span> |
| <span data-ttu-id="89c55-221">MPReg:PersonEmailDigest</span><span class="sxs-lookup"><span data-stu-id="89c55-221">MPReg:PersonEmailDigest</span></span> | <span data-ttu-id="89c55-222">Text</span><span class="sxs-lookup"><span data-stu-id="89c55-222">Text</span></span>       | <span data-ttu-id="89c55-223">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-223">External</span></span> | <span data-ttu-id="89c55-224">**選擇性** ：儲存人員的即時電子郵件地址的 sha-1 加密訊息雜湊。</span><span class="sxs-lookup"><span data-stu-id="89c55-224">**optional** : Stores the SHA-1 encrypted message hash of the person's Live e-mail address.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="89c55-225">MPReg:PersonLiveIdCID</span><span class="sxs-lookup"><span data-stu-id="89c55-225">MPReg:PersonLiveIdCID</span></span>   | <span data-ttu-id="89c55-226">Text</span><span class="sxs-lookup"><span data-stu-id="89c55-226">Text</span></span>       | <span data-ttu-id="89c55-227">外部</span><span class="sxs-lookup"><span data-stu-id="89c55-227">External</span></span> | <span data-ttu-id="89c55-228">**選擇性** ：儲存人員的即時 CID 帶正負號的十進位標記法，這是公開識別即時身分識別的64位整數。</span><span class="sxs-lookup"><span data-stu-id="89c55-228">**optional** :Stores the signed decimal representation of the person's Live CID, a 64-bit integer that publicly identifies a Live identity.</span></span>                                                                                                                                                                     |



 

### <a name="sample-metadata"></a><span data-ttu-id="89c55-229">範例中繼資料</span><span class="sxs-lookup"><span data-stu-id="89c55-229">Sample Metadata</span></span>

<span data-ttu-id="89c55-230">以下是人員標記的 XMP 中繼資料標記法。</span><span class="sxs-lookup"><span data-stu-id="89c55-230">The following is a representation of the XMP metadata for people tagging.</span></span>

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a><span data-ttu-id="89c55-231">相關主題</span><span class="sxs-lookup"><span data-stu-id="89c55-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89c55-232">**概念**</span><span class="sxs-lookup"><span data-stu-id="89c55-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89c55-233">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="89c55-233">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="89c55-234">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="89c55-234">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="89c55-235">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="89c55-235">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="89c55-236">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="89c55-236">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
