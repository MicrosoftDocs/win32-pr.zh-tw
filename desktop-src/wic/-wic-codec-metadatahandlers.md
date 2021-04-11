---
description: 本主題將介紹針對 Windows 影像處理元件 (WIC) （包括中繼資料讀取器和寫入器）建立自訂元資料處理程式的需求。
ms.assetid: 08f1872b-6e4d-44ee-abc7-48685e435acc
title: 中繼資料擴充性總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6576585f7f35628432504086695dd6c64091d3b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193563"
---
# <a name="metadata-extensibility-overview"></a><span data-ttu-id="71e9f-103">中繼資料擴充性總覽</span><span class="sxs-lookup"><span data-stu-id="71e9f-103">Metadata Extensibility Overview</span></span>

<span data-ttu-id="71e9f-104">本主題將介紹針對 Windows 影像處理元件 (WIC) （包括中繼資料讀取器和寫入器）建立自訂元資料處理程式的需求。</span><span class="sxs-lookup"><span data-stu-id="71e9f-104">This topic introduces the requirements for creating custom metadata handlers for the Windows Imaging Component (WIC), including both metadata readers and writers.</span></span> <span data-ttu-id="71e9f-105">此外，也會討論擴充 WIC 執行時間元件探索以包含自訂元資料處理程式的需求。</span><span class="sxs-lookup"><span data-stu-id="71e9f-105">It also discusses the requirements for extending WIC run-time component discovery to include your custom metadata handlers.</span></span>

<span data-ttu-id="71e9f-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="71e9f-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="71e9f-107">先決條件</span><span class="sxs-lookup"><span data-stu-id="71e9f-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="71e9f-108">簡介</span><span class="sxs-lookup"><span data-stu-id="71e9f-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="71e9f-109">建立中繼資料讀取器</span><span class="sxs-lookup"><span data-stu-id="71e9f-109">Creating a Metadata Reader</span></span>](#creating-a-metadata-reader)
    -   [<span data-ttu-id="71e9f-110">IWICMetadataReader 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-110">IWICMetadataReader Interface</span></span>](#iwicmetadatareader-interface)
    -   [<span data-ttu-id="71e9f-111">IWICPersistStream 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-111">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="71e9f-112">IWICStreamProvider 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-112">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="71e9f-113">建立中繼資料寫入器</span><span class="sxs-lookup"><span data-stu-id="71e9f-113">Creating a Metadata Writer</span></span>](#creating-a-metadata-writer)
    -   [<span data-ttu-id="71e9f-114">IWICMetadataWriter 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-114">IWICMetadataWriter Interface</span></span>](#iwicmetadatawriter-interface)
    -   [<span data-ttu-id="71e9f-115">IWICPersistStream 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-115">IWICPersistStream Interface</span></span>](#iwicpersiststream-interface)
    -   [<span data-ttu-id="71e9f-116">IWICStreamProvider 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-116">IWICStreamProvider Interface</span></span>](#iwicstreamprovider-interface)
-   [<span data-ttu-id="71e9f-117">安裝和註冊元資料處理程式</span><span class="sxs-lookup"><span data-stu-id="71e9f-117">Installing and Registering a Metadata Handler</span></span>](#installing-and-registering-a-metadata-handler)
    -   [<span data-ttu-id="71e9f-118">元資料處理程式登錄機碼</span><span class="sxs-lookup"><span data-stu-id="71e9f-118">Metadata Handler Registry Keys</span></span>](#metadata-handler-registry-keys)
    -   [<span data-ttu-id="71e9f-119">中繼資料讀取器</span><span class="sxs-lookup"><span data-stu-id="71e9f-119">Metadata Readers</span></span>](#metadata-readers)
    -   [<span data-ttu-id="71e9f-120">中繼資料寫入器</span><span class="sxs-lookup"><span data-stu-id="71e9f-120">Metadata Writers</span></span>](#metadata-writers)
    -   [<span data-ttu-id="71e9f-121">簽署元資料處理程式</span><span class="sxs-lookup"><span data-stu-id="71e9f-121">Signing a Metadata Handler</span></span>](#signing-a-metadata-handler)
-   [<span data-ttu-id="71e9f-122">特殊考慮</span><span class="sxs-lookup"><span data-stu-id="71e9f-122">Special Considerations</span></span>](#special-considerations)
    -   [<span data-ttu-id="71e9f-123">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="71e9f-123">PROPVARIANTS</span></span>](#propvariants)
    -   [<span data-ttu-id="71e9f-124">8BIM 處理常式</span><span class="sxs-lookup"><span data-stu-id="71e9f-124">8BIM Handlers</span></span>](#8bim-handlers)
-   [<span data-ttu-id="71e9f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e9f-125">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="71e9f-126">必要條件</span><span class="sxs-lookup"><span data-stu-id="71e9f-126">Prerequisites</span></span>

<span data-ttu-id="71e9f-127">若要瞭解本主題，您應該對 WIC、其元件和映射的中繼資料有深入的瞭解。</span><span class="sxs-lookup"><span data-stu-id="71e9f-127">To understand this topic you should have an in-depth understanding of WIC, its components, and metadata for images.</span></span> <span data-ttu-id="71e9f-128">如需 WIC 中繼資料的詳細資訊，請參閱 [Wic 中繼資料總覽](-wic-about-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="71e9f-128">For more information on WIC metadata, see the [WIC Metadata Overview](-wic-about-metadata.md).</span></span> <span data-ttu-id="71e9f-129">如需 WIC 元件的詳細資訊，請參閱 [Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)。</span><span class="sxs-lookup"><span data-stu-id="71e9f-129">For more information on WIC components, see the [Windows Imaging Component Overview](-wic-about-windows-imaging-codec.md).</span></span>

## <a name="introduction"></a><span data-ttu-id="71e9f-130">簡介</span><span class="sxs-lookup"><span data-stu-id="71e9f-130">Introduction</span></span>

<span data-ttu-id="71e9f-131">如 [WIC 中繼資料總覽](-wic-about-metadata.md)中所述，影像中通常會有多個中繼資料區塊，每個區塊都會以不同的元資料格式公開不同類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-131">As discussed in the [WIC Metadata Overview](-wic-about-metadata.md), there are often multiple blocks of metadata within an image, each exposing different types of information in different metadata formats.</span></span> <span data-ttu-id="71e9f-132">若要與內嵌于影像內的元資料格式互動，應用程式必須使用適當的元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-132">To interact with a metadata format embedded within an image, an application must use an appropriate metadata handler.</span></span> <span data-ttu-id="71e9f-133">WIC 提供數個元資料處理程式 (中繼資料讀取器和寫入器，) 可讓您讀取和寫入特定類型的中繼資料，例如 Exif 或 XMP。</span><span class="sxs-lookup"><span data-stu-id="71e9f-133">WIC provides several metadata handlers (both metadata readers and writers) that enable you to read and write specific types of metadata such as Exif or XMP.</span></span>

<span data-ttu-id="71e9f-134">除了提供的原生處理常式之外，WIC 還提供 Api，可讓您建立新的元資料處理程式來參與 WIC 的執行時間元件探索。</span><span class="sxs-lookup"><span data-stu-id="71e9f-134">In addition to the native handlers provided, WIC provides APIs that enable you to create new metadata handlers that participate in WIC's run-time component discovery.</span></span> <span data-ttu-id="71e9f-135">這可讓使用 WIC 的應用程式讀取及寫入您的自訂元資料格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-135">This enables applications that use WIC to read and write your custom metadata formats.</span></span>

<span data-ttu-id="71e9f-136">下列步驟可讓您的元資料處理程式參與 WIC 的執行時間中繼資料探索。</span><span class="sxs-lookup"><span data-stu-id="71e9f-136">The following steps enable your metadata handlers to participate in WIC's run-time metadata discovery.</span></span>

-   <span data-ttu-id="71e9f-137">實 ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) 的中繼資料讀取器處理常式類別，其會公開所需的 WIC 介面以讀取您的自訂元資料格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-137">Implement a metadata-reader handler class ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) that exposes the required WIC interfaces for reading your custom metadata format.</span></span> <span data-ttu-id="71e9f-138">這可讓 WIC 型應用程式以讀取原生元資料格式的相同方式讀取您的元資料格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-138">This enables WIC-based applications to read your metadata format the same way they read native metadata formats.</span></span>
-   <span data-ttu-id="71e9f-139">將中繼資料寫入器處理常式類別 (為公開必要的 WIC 介面以編碼自訂元資料格式的 [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) 。</span><span class="sxs-lookup"><span data-stu-id="71e9f-139">Implement a metadata-writer handler class ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) that exposes the required WIC interfaces for encoding your custom metadata format.</span></span> <span data-ttu-id="71e9f-140">這可讓 WIC 型應用程式將您的元資料格式序列化為支援的影像格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-140">This enables WIC-based applications to serialize your metadata format into supported image formats.</span></span>
-   <span data-ttu-id="71e9f-141">以數位方式簽署並註冊您的元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-141">Digitally sign and register your metadata handlers.</span></span> <span data-ttu-id="71e9f-142">這可讓您在執行時間探索元資料處理程式，方法是將登錄中的識別模式與內嵌在影像檔中的模式比對。</span><span class="sxs-lookup"><span data-stu-id="71e9f-142">This enables your metadata handlers to be discovered at run time by matching the identifying pattern in the registry with the pattern embedded in the image file.</span></span>

## <a name="creating-a-metadata-reader"></a><span data-ttu-id="71e9f-143">建立中繼資料讀取器</span><span class="sxs-lookup"><span data-stu-id="71e9f-143">Creating a Metadata Reader</span></span>

<span data-ttu-id="71e9f-144">編解碼器內中繼資料區塊的主要存取是透過每個 WIC 編解碼器所實行的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 介面。</span><span class="sxs-lookup"><span data-stu-id="71e9f-144">The main access to metadata blocks within a codec is through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface that each WIC codec implements.</span></span> <span data-ttu-id="71e9f-145">此介面會列舉以影像格式內嵌的每個中繼資料區塊，以針對每個區塊探索並具現化適當的元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-145">This interface enumerates each of the metadata blocks embedded in an image format so that the appropriate metadata handler can be discovered and instantiated for each block.</span></span> <span data-ttu-id="71e9f-146">WIC 無法辨識的中繼資料區塊會被視為未知，而且會定義為 GUID CLSID \_ WICUnknownMetadataReader。</span><span class="sxs-lookup"><span data-stu-id="71e9f-146">The metadata blocks that are not recognized by WIC are considered unknown and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="71e9f-147">若要讓 WIC 辨識您的元資料格式，您必須建立可執行三個介面的類別： [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)、 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)和 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)。</span><span class="sxs-lookup"><span data-stu-id="71e9f-147">To have your metadata format recognized by WIC, you must create a class that implements three interfaces: [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="71e9f-148">如果您的元資料格式具有可轉譯某些必要介面方法的限制，這類方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="71e9f-148">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatareader-interface"></a><span data-ttu-id="71e9f-149">IWICMetadataReader 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-149">IWICMetadataReader Interface</span></span>

<span data-ttu-id="71e9f-150">建立中繼資料讀取器時，必須執行 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) 介面。</span><span class="sxs-lookup"><span data-stu-id="71e9f-150">The [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) interface must be implemented when creating a metadata reader.</span></span> <span data-ttu-id="71e9f-151">這個介面可讓您存取元資料格式之資料流程內的基礎中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-151">This interface provides access to the underling metadata items within the data stream of a metadata format.</span></span>

<span data-ttu-id="71e9f-152">下列程式碼顯示 wincodecsdk .idl 檔中所定義之中繼資料讀取器介面的定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-152">The following code shows the definition of the metadata reader interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataReader : IUnknown
{
    HRESULT GetMetadataFormat(
        [out] GUID *pguidMetadataFormat
        );

    HRESULT GetMetadataHandlerInfo(
        [out] IWICMetadataHandlerInfo **ppIHandler
        );

    HRESULT GetCount(
        [out] UINT *pcCount
        );

    HRESULT GetValueByIndex(
        [in] UINT nIndex,
        [in, out, unique] PROPVARIANT *pvarSchema,
        [in, out, unique] PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in, out, unique] PROPVARIANT *pvarValue
        );

    HRESULT GetEnumerator(
        [out] IWICEnumMetadataItem **ppIEnumMetadata
        );
};
```

<span data-ttu-id="71e9f-153">**GetMetadataFormat** 方法會傳回元資料格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-153">The **GetMetadataFormat** method returns the GUID of your metadata format.</span></span>

<span data-ttu-id="71e9f-154">**GetMetadataHandlerInfo** 方法會傳回 [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo)介面，提供元資料處理程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-154">The **GetMetadataHandlerInfo** method returns an [**IWICMetadataHandlerInfo**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo) interface that provides information about your metadata handler.</span></span> <span data-ttu-id="71e9f-155">這包括了哪些影像格式支援元資料格式的資訊，以及您的中繼資料讀取器是否需要存取完整的中繼資料資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-155">This includes information such as what image formats support the metadata format and whether your metadata reader requires access to the full metadata stream.</span></span>

<span data-ttu-id="71e9f-156">**GetCount** 方法會傳回個別中繼資料專案的數目 (包括中繼資料資料流程中) 找到的內嵌中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-156">The **GetCount** method returns the number of individual metadata items (including embedded metadata blocks) found within the metadata stream.</span></span>

<span data-ttu-id="71e9f-157">**GetValueByIndex** 方法會依索引值傳回中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-157">The **GetValueByIndex** method returns a metadata item by an index value.</span></span> <span data-ttu-id="71e9f-158">這個方法可讓應用程式在中繼資料區塊中的每個中繼資料專案之間執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="71e9f-158">This method enables applications to loop through each metadata item in a metadata block.</span></span> <span data-ttu-id="71e9f-159">下列程式碼將示範應用程式如何使用這個方法來取得中繼資料區塊中的每個中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-159">The following code demonstrates how an application can use this method to retrieve each metadata item in a metadata block.</span></span>


```C++
PROPVARIANT readerValue;
IWICMetadataBlockReader *blockReader = NULL;
IWICMetadataReader *reader = NULL;

PropVariantInit(&readerValue);

hr = pFrameDecode->QueryInterface(IID_IWICMetadataBlockReader, (void**)&blockReader);

if (SUCCEEDED(hr))
{
    // Retrieve the third block in the image. This is image specific and
    // ideally you should call this by retrieving the reader count
    // first.
    hr = blockReader->GetReaderByIndex(2, &reader);
}

if (SUCCEEDED(hr))
{
    UINT numValues = 0;

    hr = reader->GetCount(&numValues);

    // Loop through each item and retrieve by index
    for (UINT i = 0; SUCCEEDED(hr) && i < numValues; i++)
    {
        PROPVARIANT id, value;

        PropVariantInit(&id);
        PropVariantInit(&value);

        hr = reader->GetValueByIndex(i, NULL, &id, &value);

        if (SUCCEEDED(hr))
        {
            // Do something with the metadata item.
            //...
        }
        PropVariantClear(&id);
        PropVariantClear(&value);
    }               
}
```



<span data-ttu-id="71e9f-160">**GetValue** 方法會依架構和/或識別碼來抓取特定的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-160">The **GetValue** method retrieves a specific metadata item by schema and/or ID.</span></span> <span data-ttu-id="71e9f-161">這個方法類似于 **GetValueByIndex** 方法，不同之處在于它會抓取具有特定架構或識別碼的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-161">This method is similar to the **GetValueByIndex** method except that it retrieves a metadata item that has a specific schema or ID.</span></span>

<span data-ttu-id="71e9f-162">**GetEnumerator** 方法會傳回中繼資料區塊中每個中繼資料專案的列舉值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-162">The **GetEnumerator** method returns an enumerator of each metadata item in the metadata block.</span></span> <span data-ttu-id="71e9f-163">這可讓應用程式使用列舉值來流覽您的元資料格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-163">This enables applications to use an enumerator to navigate your metadata format.</span></span>

<span data-ttu-id="71e9f-164">如果您的元資料格式沒有中繼資料專案的架構概念，則為 GetValue .。。方法應該忽略這個屬性。</span><span class="sxs-lookup"><span data-stu-id="71e9f-164">If your metadata format does not have a notion of schemas for metadata items, the GetValue... methods should ignore this property.</span></span> <span data-ttu-id="71e9f-165">但是，如果您的格式支援架構命名，您應該預期會有 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-165">If, however, your format supports schema naming, you should anticipate a **NULL** value.</span></span>

<span data-ttu-id="71e9f-166">如果中繼資料專案是內嵌的中繼資料區塊，請從內嵌內容的子流建立元資料處理程式，並傳回新的元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-166">If a metadata item is an embedded metadata block, create a metadata handler from the substream of the embedded content and return the new metadata handler.</span></span> <span data-ttu-id="71e9f-167">如果沒有可用於嵌套區塊的中繼資料讀取器，請具現化並傳回未知的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="71e9f-167">If there is no metadata reader available for the nested block, instantiate and return an unknown metadata reader.</span></span> <span data-ttu-id="71e9f-168">若要為內嵌區塊建立新的中繼資料讀取器，請呼叫元件 factory 的 **CreateMetadataReaderFromContainer** 或 **CreateMetadataReader** 方法，或呼叫 [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) 函數。</span><span class="sxs-lookup"><span data-stu-id="71e9f-168">To create a new metadata reader for the embedded block, call the component factory's **CreateMetadataReaderFromContainer** or **CreateMetadataReader** methods, or call the [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent) function.</span></span>

<span data-ttu-id="71e9f-169">如果中繼資料資料流程包含位元組由大到小的內容，中繼資料讀取器會負責交換其處理的任何資料值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-169">If the metadata stream contains big-endian content, the metadata reader is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="71e9f-170">它也會負責通知任何嵌套的中繼資料讀取器，其正在使用位元組由大到小的資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-170">It is also responsible for informing any nested metadata readers that they are working with big-endian data stream.</span></span> <span data-ttu-id="71e9f-171">不過，所有值都應該以位元組由小到大的格式傳回。</span><span class="sxs-lookup"><span data-stu-id="71e9f-171">However, all values should be returned in little-endian format.</span></span>

<span data-ttu-id="71e9f-172">藉由支援查詢（中繼資料專案識別碼是 `VT_CLSID` (GUID) 對應至元資料格式），來執行命名空間導覽的支援。</span><span class="sxs-lookup"><span data-stu-id="71e9f-172">Implement support for namespace navigation by supporting queries where the metadata item ID is a `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="71e9f-173">如果在剖析期間識別出該格式的嵌套中繼資料讀取器，則必須將它傳回。</span><span class="sxs-lookup"><span data-stu-id="71e9f-173">If a nested metadata reader for that format is identified during parsing, it must be returned.</span></span> <span data-ttu-id="71e9f-174">這可讓應用程式使用中繼資料查詢讀取器來搜尋您的元資料格式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-174">This enables applications to use a metadata query reader to search your metadata format.</span></span>

<span data-ttu-id="71e9f-175">依識別碼取得中繼資料專案時，您應該使用 [PropVariantChangeType](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) 函式將識別碼強制轉型為預期的型別。</span><span class="sxs-lookup"><span data-stu-id="71e9f-175">When getting a metadata item by ID, you should use [PropVariantChangeType Function](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) to coerce the ID into the expected type.</span></span> <span data-ttu-id="71e9f-176">例如，IFD 讀取器會將識別碼強制轉換成型別 `VT_UI2` ，以符合 IFD 標記識別項 USHORT 的資料型別。</span><span class="sxs-lookup"><span data-stu-id="71e9f-176">For example, the IFD reader will coerce an ID to type `VT_UI2` to coincide with the data type of an IFD tag ID USHORT.</span></span> <span data-ttu-id="71e9f-177">輸入型別和預期的型別都必須 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 來進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="71e9f-177">The input type and expected type must both be [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to do this.</span></span> <span data-ttu-id="71e9f-178">這並不是必要的，但執行這項強制轉換可簡化呼叫讀取器以查詢中繼資料專案的程式碼。</span><span class="sxs-lookup"><span data-stu-id="71e9f-178">This is not required, but doing this coercion simplifies code that calls the reader to query for metadata items.</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="71e9f-179">IWICPersistStream 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-179">IWICPersistStream Interface</span></span>

<span data-ttu-id="71e9f-180">[**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)介面繼承自 **IPersistStream** ，並提供使用 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉來儲存和載入物件的其他方法。</span><span class="sxs-lookup"><span data-stu-id="71e9f-180">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="71e9f-181">下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) 介面的定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-181">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="71e9f-182">**LoadEx** 方法會為您的中繼資料讀取器提供包含中繼資料區塊的資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-182">The **LoadEx** method provides your metadata reader with a data stream containing your metadata block.</span></span> <span data-ttu-id="71e9f-183">您的讀取器會剖析此資料流程以存取基礎中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-183">Your reader parses this stream to access the underlying metadata items.</span></span> <span data-ttu-id="71e9f-184">您的中繼資料讀取器會使用位於原始中繼資料內容開頭的子流進行初始化。</span><span class="sxs-lookup"><span data-stu-id="71e9f-184">Your metadata reader is initialized with a substream that is positioned at the beginning of the raw metadata content.</span></span> <span data-ttu-id="71e9f-185">如果您的讀取器不需要完整資料流程，則子資料流程的範圍僅限於中繼資料區塊的內容;否則，系統會提供完整的中繼資料資料流程，並在中繼資料區塊的開頭設定位置。</span><span class="sxs-lookup"><span data-stu-id="71e9f-185">If your reader does not require the full stream, the substream is limited in range to only the content of the metadata block; otherwise, the full metadata stream is provided with the position set at the beginning of your metadata block.</span></span>

<span data-ttu-id="71e9f-186">中繼資料寫入器會使用 **SaveEx** 方法來序列化中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-186">The **SaveEx** method is used by metadata writers to serialize your metadata block.</span></span> <span data-ttu-id="71e9f-187">當 **SaveEx** 用於中繼資料讀取器時，它應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="71e9f-187">When **SaveEx** is used in a metadata reader, it should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="71e9f-188">IWICStreamProvider 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-188">IWICStreamProvider Interface</span></span>

<span data-ttu-id="71e9f-189">[**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)介面可讓您的中繼資料讀取器提供其內容資料流程的參考、提供資料流程的相關資訊，以及重新整理資料流程的快取版本。</span><span class="sxs-lookup"><span data-stu-id="71e9f-189">The [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface enables your metadata reader to provide references to its content stream, provide information about the stream, and refresh cached versions of the stream.</span></span>

<span data-ttu-id="71e9f-190">下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) 介面的定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-190">The following code shows the definition of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICStreamProvider : IUnknown
{
    HRESULT GetStream(
        [out] IStream **ppIStream
        );

    HRESULT GetPersistOptions(
        [out] DWORD *pdwPersistOptions
        );

    HRESULT GetPreferredVendorGUID(
        [out] GUID *pguidPreferredVendor
        );

    HRESULT RefreshStream(
        );
};
```

<span data-ttu-id="71e9f-191">**GetStream** 方法會捕獲中繼資料資料流程的參考。</span><span class="sxs-lookup"><span data-stu-id="71e9f-191">The **GetStream** method retrieves a reference to your metadata stream.</span></span> <span data-ttu-id="71e9f-192">您傳回的資料流程應該將資料流程指標重設為開始位置。</span><span class="sxs-lookup"><span data-stu-id="71e9f-192">The stream you return should have the stream pointer reset to the start position.</span></span> <span data-ttu-id="71e9f-193">如果您的元資料格式需要完整的資料流程存取，則開始位置應該是中繼資料區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="71e9f-193">If your metadata format requires full stream access, the start position should be the start of your metadata block.</span></span>

<span data-ttu-id="71e9f-194">**GetPersistOptions** 方法會從 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉傳回資料流程的目前選項。</span><span class="sxs-lookup"><span data-stu-id="71e9f-194">The **GetPersistOptions** method returns the stream's current options from the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="71e9f-195">**GetPreferredVendorGUID** 方法會傳回中繼資料讀取器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-195">The **GetPreferredVendorGUID** method returns the GUID of the vendor of the metadata reader.</span></span>

<span data-ttu-id="71e9f-196">**RefreshStream** 方法會重新整理中繼資料資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-196">The **RefreshStream** method refreshes the metadata stream.</span></span> <span data-ttu-id="71e9f-197">此方法必須為任何嵌套中繼資料區塊呼叫具有 **Null** 資料流程的 **LoadEx** 。</span><span class="sxs-lookup"><span data-stu-id="71e9f-197">This method must call **LoadEx** with a **NULL** stream for any nested metadata blocks.</span></span> <span data-ttu-id="71e9f-198">這是必要的，因為就地編輯時，因為有嵌套的中繼資料區塊及其專案可能已不存在。</span><span class="sxs-lookup"><span data-stu-id="71e9f-198">This is necessary because nested metadata blocks and their items may no longer exist, due to in-place editing.</span></span>

## <a name="creating-a-metadata-writer"></a><span data-ttu-id="71e9f-199">建立中繼資料寫入器</span><span class="sxs-lookup"><span data-stu-id="71e9f-199">Creating a Metadata Writer</span></span>

<span data-ttu-id="71e9f-200">中繼資料寫入器是一種元資料處理程式類型，可讓您將中繼資料區塊序列化至影像框架，或在個別框架之外（如果影像格式支援的話）。</span><span class="sxs-lookup"><span data-stu-id="71e9f-200">A metadata writer is a type of metadata handler that provides a way to serialize a metadata block to an image frame, or outside an individual frame if the image format supports it.</span></span> <span data-ttu-id="71e9f-201">編解碼器內中繼資料寫入器的主要存取是透過每個 WIC 編碼器所實行的 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="71e9f-201">The main access to the metadata writers within a codec is through the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface that each WIC encoder implements.</span></span> <span data-ttu-id="71e9f-202">這個介面可讓應用程式列舉內嵌于影像中的每個中繼資料區塊，以針對每個中繼資料區塊探索和具現化適當的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-202">This interface enables applications to enumerate each of the metadata blocks embedded in an image so that the appropriate metadata writer can be discovered and instantiated for each metadata block.</span></span> <span data-ttu-id="71e9f-203">沒有對應中繼資料寫入器的中繼資料區塊會被視為未知，而且會定義為 GUID CLSID \_ WICUnknownMetadataReader。</span><span class="sxs-lookup"><span data-stu-id="71e9f-203">Metadata blocks that do not have a corresponding metadata writer are considered unknown, and are defined as the GUID CLSID\_WICUnknownMetadataReader.</span></span> <span data-ttu-id="71e9f-204">若要啟用已啟用 WIC 的應用程式來序列化和寫入您的元資料格式，您必須建立可執行下列介面的類別： [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)、 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)、 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)和 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider)。</span><span class="sxs-lookup"><span data-stu-id="71e9f-204">To enable WIC enabled applications to serialize and write your metadata format, you must create a class that implements the following interfaces: [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter), [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream), and [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider).</span></span>

> [!Note]  
> <span data-ttu-id="71e9f-205">如果您的元資料格式具有可轉譯某些必要介面方法的限制，這類方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="71e9f-205">If your metadata format has restrictions that render some methods of the required interfaces inappropriate, such methods should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

 

### <a name="iwicmetadatawriter-interface"></a><span data-ttu-id="71e9f-206">IWICMetadataWriter 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-206">IWICMetadataWriter Interface</span></span>

<span data-ttu-id="71e9f-207">[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)介面必須由您的中繼資料寫入器來執行。</span><span class="sxs-lookup"><span data-stu-id="71e9f-207">The [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) interface must be implemented by your metadata writer.</span></span> <span data-ttu-id="71e9f-208">此外，由於 **IWICMetadataWriter** 繼承自 [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)，因此您也必須執行 **IWICMetadataReader** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="71e9f-208">Additionally, because **IWICMetadataWriter** inherits from [**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader), you must also implement all the methods of **IWICMetadataReader**.</span></span> <span data-ttu-id="71e9f-209">由於這兩種處理常式類型都需要相同的介面繼承，因此您可能會想要建立可同時提供讀取和寫入功能的單一類別。</span><span class="sxs-lookup"><span data-stu-id="71e9f-209">Because both handler types require the same interface inheritance, you might want to create a single class that provides both reading and writing functionality.</span></span>

<span data-ttu-id="71e9f-210">下列程式碼顯示 wincodecsdk .idl 檔中所定義之中繼資料寫入器介面的定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-210">The following code shows the definition of the metadata writer interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICMetadataWriter : IWICMetadataReader
{
    HRESULT SetValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT SetValueByIndex(
        [in] UINT nIndex,
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId,
        [in] const PROPVARIANT *pvarValue
        );

    HRESULT RemoveValue(
        [in, unique] const PROPVARIANT *pvarSchema,
        [in] const PROPVARIANT *pvarId
        );

    HRESULT RemoveValueByIndex(
        [in] UINT nIndex
        );
};
```

<span data-ttu-id="71e9f-211">**SetValue** 方法會將指定的中繼資料專案寫入中繼資料資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-211">The **SetValue** method writes the specified metadata item to the metadata stream.</span></span>

<span data-ttu-id="71e9f-212">**SetValueByIndex** 方法會將指定的中繼資料專案寫入中繼資料資料流程中的指定索引處。</span><span class="sxs-lookup"><span data-stu-id="71e9f-212">The **SetValueByIndex** method writes the specified metadata item to the specified index in the metadata stream.</span></span> <span data-ttu-id="71e9f-213">索引不會參考識別碼，而是參考中繼資料區塊內的專案位置。</span><span class="sxs-lookup"><span data-stu-id="71e9f-213">The index does not refer to the ID but to the position of the item within the metadata block.</span></span>

<span data-ttu-id="71e9f-214">**RemoveValue** 方法會從中繼資料資料流程中移除指定的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-214">The **RemoveValue** method removes the specified metadata item from the metadata stream.</span></span>

<span data-ttu-id="71e9f-215">**RemoveValueByIndex** 方法會從中繼資料資料流程中移除位於指定索引位置的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-215">The **RemoveValueByIndex** method removes the metadata item at the specified index from the metadata stream.</span></span> <span data-ttu-id="71e9f-216">移除專案之後，如果索引不是最後一個索引，則其餘的中繼資料專案應該會佔用空的索引。</span><span class="sxs-lookup"><span data-stu-id="71e9f-216">After removing an item, it is expected that the remaining metadata items will occupy the vacated index if the index is not the last index.</span></span> <span data-ttu-id="71e9f-217">這也預期計數會在移除專案之後變更。</span><span class="sxs-lookup"><span data-stu-id="71e9f-217">It is also expected that the count will change after the item is removed.</span></span>

<span data-ttu-id="71e9f-218">中繼資料編寫者必須負責將 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 專案轉換成您的格式所需的基礎結構。</span><span class="sxs-lookup"><span data-stu-id="71e9f-218">It is the metadata writer's responsibility to convert the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) items to the underlying structure required by your format.</span></span> <span data-ttu-id="71e9f-219">不過，與中繼資料讀取器不同的是，變數類型通常不應該強制轉型成不同的類型，因為呼叫端會特別指出要使用的資料型別。</span><span class="sxs-lookup"><span data-stu-id="71e9f-219">However, unlike the metadata reader, VARIANT types should not normally be coerced to different types as the caller is specifically indicating what data type to use.</span></span>

<span data-ttu-id="71e9f-220">您的中繼資料寫入器必須將所有中繼資料專案認可至影像資料流程，包括隱藏或無法辨識的值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-220">Your metadata writer must commit all metadata items to the image stream, including hidden or unrecognized values.</span></span> <span data-ttu-id="71e9f-221">這包括未知的嵌套中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-221">This includes unknown nested metadata blocks.</span></span> <span data-ttu-id="71e9f-222">不過，編碼器在起始儲存作業之前，必須負責設定任何重要的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-222">However, it is the encoder's responsibility to set any critical metadata items prior to initiating the save operation.</span></span>

<span data-ttu-id="71e9f-223">如果中繼資料資料流程包含位元組由大到小的內容，中繼資料寫入器就會負責交換其處理的任何資料值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-223">If the metadata stream contains big-endian content, the metadata writer is responsible for swapping any data values it processes.</span></span> <span data-ttu-id="71e9f-224">它也負責通知任何嵌套的中繼資料寫入器，以便在儲存時使用位元組由大到小的資料流程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-224">It is also responsible for informing any nested metadata writers that they are working with a big-endian data stream when they save.</span></span>

<span data-ttu-id="71e9f-225">藉由 `VT_CLSID` (GUID) 對應至元資料格式的中繼資料專案支援集合和移除作業，來支援建立和移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="71e9f-225">Implement support for namespace creation and removal by supporting set and remove operations on metadata items with a type of `VT_CLSID` (a GUID) corresponding to a metadata format.</span></span> <span data-ttu-id="71e9f-226">中繼資料寫入器會呼叫 [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) 函式，將嵌套的中繼資料寫入器內容正確地內嵌至父中繼資料寫入器中。</span><span class="sxs-lookup"><span data-stu-id="71e9f-226">The metadata writer calls the [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) function to properly embed the nested metadata writer content into the parent metadata writer.</span></span>

<span data-ttu-id="71e9f-227">如果您的元資料格式支援就地編碼，則必須負責管理必要的填補。</span><span class="sxs-lookup"><span data-stu-id="71e9f-227">If your metadata format supports in-place encoding, you are responsible for managing the required padding.</span></span> <span data-ttu-id="71e9f-228">如需就地編碼的詳細資訊，請參閱 [WIC 中繼資料總覽](-wic-about-metadata.md) 和 [讀取和寫入影像中繼資料的總覽](-wic-codec-readingwritingmetadata.md)。</span><span class="sxs-lookup"><span data-stu-id="71e9f-228">For more information on in-place encoding, see [WIC Metadata Overview](-wic-about-metadata.md) and [Overview of Reading and Writing Image Metadata](-wic-codec-readingwritingmetadata.md).</span></span>

### <a name="iwicpersiststream-interface"></a><span data-ttu-id="71e9f-229">IWICPersistStream 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-229">IWICPersistStream Interface</span></span>

<span data-ttu-id="71e9f-230">[**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream)介面繼承自 **IPersistStream** ，並提供使用 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)列舉來儲存和載入物件的其他方法。</span><span class="sxs-lookup"><span data-stu-id="71e9f-230">The [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface inherits from **IPersistStream** and provides additional methods for saving and loading objects by using the [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) enumeration.</span></span>

<span data-ttu-id="71e9f-231">下列程式碼顯示 wincodecsdk .idl 檔中所定義之 [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) 介面的定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-231">The following code shows the definition of the [**IWICPersistStream**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicpersiststream) interface as defined in the wincodecsdk.idl file.</span></span>

``` syntax
interface IWICPersistStream : IPersistStream
{
    HRESULT LoadEx(
        [in, unique] IStream *pIStream,
        [in, unique] const GUID *pguidPreferredVendor,
        [in] DWORD dwPersistOptions
        );

    HRESULT SaveEx(
        [in] IStream *pIStream,
        [in] DWORD dwPersistOptions,
        [in] BOOL fClearDirty
        );
};
```

<span data-ttu-id="71e9f-232">**LoadEx** 方法會使用包含中繼資料區塊的資料流程來提供元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-232">The **LoadEx** method provides your metadata handler with a data stream containing your metadata block.</span></span>

<span data-ttu-id="71e9f-233">**SaveEx** 方法會將中繼資料序列化為數據流。</span><span class="sxs-lookup"><span data-stu-id="71e9f-233">The **SaveEx** method serializes the metadata into a stream.</span></span> <span data-ttu-id="71e9f-234">如果提供的資料流程與初始化資料流程相同，您應該執行就地編碼。</span><span class="sxs-lookup"><span data-stu-id="71e9f-234">If the provided stream is the same as initialization stream, you should perform in-place encoding.</span></span> <span data-ttu-id="71e9f-235">如果支援就地編碼，則在沒有 \_ \_ 足夠填補可執行就地編碼時，此方法應該會傳回 WINCODEC 錯誤 TOOMUCHMETADATA。</span><span class="sxs-lookup"><span data-stu-id="71e9f-235">If in-place encoding is supported, this method should return WINCODEC\_ERR\_TOOMUCHMETADATA when there is insufficient padding to perform in-place encoding.</span></span> <span data-ttu-id="71e9f-236">如果不支援就地編碼，此方法應該會傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="71e9f-236">If in-place encoding is not supported, this method should return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

<span data-ttu-id="71e9f-237">必須實作為 **IPersistStream：： GetSizeMax** 方法，且必須傳回在後續儲存時寫入之中繼資料內容的確切大小。</span><span class="sxs-lookup"><span data-stu-id="71e9f-237">The **IPersistStream::GetSizeMax** method must be implemented and must return the exact size of the metadata content that would be written in subsequent save.</span></span>

<span data-ttu-id="71e9f-238">如果中繼資料寫入器是透過資料流程初始化，則應實作為 **IPersistStream：： IsDirty** 方法，如此一來，映射就可以可靠地判斷其內容是否已變更。</span><span class="sxs-lookup"><span data-stu-id="71e9f-238">The **IPersistStream::IsDirty** method should be implemented if the metadata writer is initialized through a stream, so that an image can reliably determine whether its content has changed.</span></span>

<span data-ttu-id="71e9f-239">如果您的元資料格式支援嵌套中繼資料區塊，則在儲存至資料流程時，您的中繼資料寫入器應該會將其內容的序列化委派給嵌套中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="71e9f-239">If your metadata format supports nested metadata blocks, your metadata writer should delegate to the nested metadata writers the serializing of its content when saving to a stream.</span></span>

### <a name="iwicstreamprovider-interface"></a><span data-ttu-id="71e9f-240">IWICStreamProvider 介面</span><span class="sxs-lookup"><span data-stu-id="71e9f-240">IWICStreamProvider Interface</span></span>

<span data-ttu-id="71e9f-241">中繼資料寫入器的 [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) 介面實作為中繼資料讀取器的實作為。</span><span class="sxs-lookup"><span data-stu-id="71e9f-241">The implementation of the [**IWICStreamProvider**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicstreamprovider) interface for a metadata writer is the same as that of a metadata reader.</span></span> <span data-ttu-id="71e9f-242">如需詳細資訊，請參閱本檔中的建立中繼資料讀取器一節。</span><span class="sxs-lookup"><span data-stu-id="71e9f-242">For more information, see Creating a Metadata Reader section in this document.</span></span>

## <a name="installing-and-registering-a-metadata-handler"></a><span data-ttu-id="71e9f-243">安裝和註冊元資料處理程式</span><span class="sxs-lookup"><span data-stu-id="71e9f-243">Installing and Registering a Metadata Handler</span></span>

<span data-ttu-id="71e9f-244">若要安裝元資料處理程式，您必須提供處理常式元件，並在系統登錄中註冊它。</span><span class="sxs-lookup"><span data-stu-id="71e9f-244">To install a metadata handler, you must provide the handler assembly and register it in the system registry.</span></span> <span data-ttu-id="71e9f-245">您可以決定如何及何時填入登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="71e9f-245">You can decide how and when the registry keys are populated.</span></span>

> [!Note]  
> <span data-ttu-id="71e9f-246">為了方便閱讀，在本檔的下列各節所示的登錄機碼中，不會顯示實際的十六進位 Guid。</span><span class="sxs-lookup"><span data-stu-id="71e9f-246">For readability, the actual hexadecimal GUIDs are not shown in the registry keys shown in the following sections of this document.</span></span> <span data-ttu-id="71e9f-247">若要找出指定之易記名稱的十六進位值，請參閱 wincodec .idl 和 wincodecsdk .idl 檔。</span><span class="sxs-lookup"><span data-stu-id="71e9f-247">To find the hexadecimal value for a specified friendly name, see the wincodec.idl and wincodecsdk.idl files.</span></span>

 

### <a name="metadata-handler-registry-keys"></a><span data-ttu-id="71e9f-248">元資料處理程式登錄機碼</span><span class="sxs-lookup"><span data-stu-id="71e9f-248">Metadata Handler Registry Keys</span></span>

<span data-ttu-id="71e9f-249">每個元資料處理程式都是以唯一 CLSID 來識別，而每個處理常式都需要在元資料處理程式的類別識別碼 GUID 下註冊其 CLSID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-249">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="71e9f-250">每個處理常式類型的類別目錄識別碼都定義于 wincodec 中;讀者的分類識別碼名稱是 CATID \_ WICMetadataReader，而寫入器的類別識別碼名稱是 catid \_ WICMetadataWriter。</span><span class="sxs-lookup"><span data-stu-id="71e9f-250">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

<span data-ttu-id="71e9f-251">每個元資料處理程式都是以唯一 CLSID 來識別，而每個處理常式都需要在元資料處理程式的類別識別碼 GUID 下註冊其 CLSID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-251">Each metadata handler is identified by a unique CLSID, and each handler is required to register its CLSID under the metadata handler's category ID GUID.</span></span> <span data-ttu-id="71e9f-252">每個處理常式類型的類別目錄識別碼都定義于 wincodec 中;讀者的分類識別碼名稱是 CATID \_ WICMetadataReader，而寫入器的類別識別碼名稱是 catid \_ WICMetadataWriter。</span><span class="sxs-lookup"><span data-stu-id="71e9f-252">Each handler type's category ID is defined in the wincodec.idl; the category ID name for readers is CATID\_WICMetadataReader, and the category ID name for writers is CATID\_WICMetadataWriter.</span></span>

> [!Note]  
> <span data-ttu-id="71e9f-253">在下列登錄機碼清單中，{Reader CLSID} 是指您為中繼資料讀取器提供的唯一 CLSID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-253">In the following registry key listings, {Reader CLSID} refers to the unique CLSID that you provide for your metadata reader.</span></span> <span data-ttu-id="71e9f-254">{Writer CLSID} 是指您為中繼資料寫入器提供的唯一 CLSID。</span><span class="sxs-lookup"><span data-stu-id="71e9f-254">{Writer CLSID} refers to the unique CLSID that you provide for your metadata writer.</span></span> <span data-ttu-id="71e9f-255">{處理常式 CLSID} 是指讀取器的 CLSID、寫入器的 CLSID，或兩者都是根據您所提供的處理常式而定。</span><span class="sxs-lookup"><span data-stu-id="71e9f-255">{Handler CLSID} refers to the reader's CLSID, the writer's CLSID, or both, depending on which handlers you are providing.</span></span> <span data-ttu-id="71e9f-256">{容器 GUID} 是指容器物件 (映射格式或元資料格式) 可包含中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-256">{Container GUID} refers to the container object (image format or metadata format) that can contain the metadata block.</span></span>

 

<span data-ttu-id="71e9f-257">下列登錄機碼會使用其他可用的元資料處理程式來註冊您的元資料處理程式：</span><span class="sxs-lookup"><span data-stu-id="71e9f-257">The following registry keys register your metadata handler with the other metadata handlers available:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CATID_WICMetadataReaders}\Instance\{Reader CLSID}]
CLSID={Reader CLSID}
Friendly Name="Reader Name"

[HKEY_CLASSES_ROOT\CLSID\{CATID_ WICMetadataWriters}\Instance\{Writer CLSID}]
CLSID={Writer CLSID}
Friendly Name="Writer Name"
```

<span data-ttu-id="71e9f-258">除了在各自的類別中註冊處理常式之外，您還必須註冊額外的索引鍵，以提供處理常式的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-258">In addition to registering your handlers in their respective categories, you must also register additional keys that provide information specific to the handler.</span></span> <span data-ttu-id="71e9f-259">讀取器和寫入器共用類似的登錄機碼需求。</span><span class="sxs-lookup"><span data-stu-id="71e9f-259">Readers and writers share similar registry key requirements.</span></span> <span data-ttu-id="71e9f-260">下列語法顯示如何註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-260">The following syntax shows how to register a handler.</span></span> <span data-ttu-id="71e9f-261">讀取器處理常式和寫入器處理常式都必須使用其各自的 Clsid 以這種方式註冊：</span><span class="sxs-lookup"><span data-stu-id="71e9f-261">Both the reader handler and writer handler must be registered in this way, using their respective CLSIDs:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{CLSID}]
"Vendor"={VendorGUID}
"Date"="yyyy-mm-dd"
"Version"="Major.Minor.Build.Number"
"SpecVersion"="Major.Minor.Build.Number"
"MetadataFormat"={MetadataFormatGUID}
"RequiresFullStream"=dword:1|0
"SupportsPadding"= dword:1|0
"FixedSize"=0

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\InProcServer32]
@="drive:\path\yourdll.dll"
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\CLSID\{CLSID}\{LCID}]
Author="Author's Name"
Description = " Metadata Description"
DeviceManufacturer ="Manufacturer Name"
DeviceModels="Device,Device"
FriendlyName="Friendly Name"
```

### <a name="metadata-readers"></a><span data-ttu-id="71e9f-262">中繼資料讀取器</span><span class="sxs-lookup"><span data-stu-id="71e9f-262">Metadata Readers</span></span>

<span data-ttu-id="71e9f-263">中繼資料讀取器註冊也會包含描述如何以容器格式內嵌讀取器的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="71e9f-263">The metadata reader registration also includes keys that describe how the reader can be embedded in a container format.</span></span> <span data-ttu-id="71e9f-264">容器格式可以是影像格式，例如 TIFF 或 JPEG;它也可以是另一個元資料格式，例如 IFD 中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-264">A container format can be an image format such as TIFF or JPEG; it can also be another metadata format such as an IFD metadata block.</span></span> <span data-ttu-id="71e9f-265">原生支援的映射容器格式會列在 wincodec 中;每個影像容器格式都會定義為名稱以 GUID ContainerFormat 開頭的 GUID \_ 。</span><span class="sxs-lookup"><span data-stu-id="71e9f-265">Natively supported image container formats are listed in wincodec.idl; each image container format is defined as a GUID with a name that begins with GUID\_ContainerFormat.</span></span> <span data-ttu-id="71e9f-266">原生支援的中繼資料容器格式會列在 wincodecsdk 中;每個中繼資料容器格式都會定義為名稱以 GUID MetadataFormat 開頭的 GUID \_ 。</span><span class="sxs-lookup"><span data-stu-id="71e9f-266">Natively supported metadata container formats are listed in wincodecsdk.idl; each metadata container format is defined as a GUID with a name that begins with GUID\_MetadataFormat.</span></span>

<span data-ttu-id="71e9f-267">下列索引鍵會註冊中繼資料讀取器所支援的容器，以及要從該容器讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-267">The following keys register a container that the metadata reader supports, and the data needed to read from that container.</span></span> <span data-ttu-id="71e9f-268">讀取器所支援的每個容器都必須以這種方式註冊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-268">Each container supported by the reader must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Reader CLSID}\Containers\{Container GUID}\0]
"Position"=dword:00000000
"Pattern"=hex:ff,ff,ff,...
"Mask"=hex:ff,ff,ff,...
"DataOffset"=dword:00000006
```

<span data-ttu-id="71e9f-269">模式索引鍵描述用來比對中繼資料區塊與讀取器的二進位模式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-269">The Pattern key describes the binary pattern that is used to match the metadata block to the reader.</span></span> <span data-ttu-id="71e9f-270">為您的中繼資料讀取器定義模式時，應該夠可靠，因為正相符表示中繼資料讀取器可以瞭解中繼資料區塊中處理的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-270">When defining a pattern for your metadata reader, it should be reliable enough that a positive match means the metadata reader can understand the metadata in the metadata block being processed.</span></span>

<span data-ttu-id="71e9f-271">DataOffset 索引鍵會描述區塊標頭中中繼資料的固定位移。</span><span class="sxs-lookup"><span data-stu-id="71e9f-271">The DataOffset key describes the fixed offset of the metadata from the block header.</span></span> <span data-ttu-id="71e9f-272">此索引鍵是選擇性的，如果未指定，則表示無法使用來自區塊標頭的固定位移找出實際的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-272">This key is optional and, if not specified, means that the actual metadata cannot be located using a fixed offset from the block header.</span></span>

### <a name="metadata-writers"></a><span data-ttu-id="71e9f-273">中繼資料寫入器</span><span class="sxs-lookup"><span data-stu-id="71e9f-273">Metadata Writers</span></span>

<span data-ttu-id="71e9f-274">中繼資料寫入器註冊也包含索引鍵，以描述如何寫出以容器格式內嵌之中繼資料內容前面的標頭。</span><span class="sxs-lookup"><span data-stu-id="71e9f-274">The metadata writer registration also includes keys that describe how to write out the header preceding the metadata content embedded in a container format.</span></span> <span data-ttu-id="71e9f-275">如同讀取器，容器格式可以是影像格式或另一個中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-275">As with the reader, a container format can be an image format or another metadata block.</span></span>

<span data-ttu-id="71e9f-276">下列索引鍵會註冊中繼資料寫入器支援的容器，以及寫入標頭和中繼資料所需的資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-276">The following keys register a container that the metadata writer supports, and the data needed to write the header and metadata.</span></span> <span data-ttu-id="71e9f-277">寫入器支援的每個容器都必須以這種方式註冊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-277">Each container supported by the writer must be registered in this way.</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{Writer CLSID}\Containers\{Container GUID}]
"WritePosition"=dword:00000000
"WriteHeader"=hex:ff,ff,ff,...
"WriteOffset"=dword:00000000
```

<span data-ttu-id="71e9f-278">WriteHeader 索引鍵描述要寫入之中繼資料區塊標頭的二進位模式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-278">The WriteHeader key describes the binary pattern of the metadata block header to be written.</span></span> <span data-ttu-id="71e9f-279">此二進位模式與元資料格式的讀取器模式索引鍵一致。</span><span class="sxs-lookup"><span data-stu-id="71e9f-279">This binary pattern coincides with the metadata format's reader Pattern key.</span></span>

<span data-ttu-id="71e9f-280">WriteOffset 索引鍵會描述應寫入中繼資料之區塊標頭中的固定位移。</span><span class="sxs-lookup"><span data-stu-id="71e9f-280">The WriteOffset key describes the fixed offset from the block header at which the metadata should be written.</span></span> <span data-ttu-id="71e9f-281">此索引鍵是選擇性的，如果未指定，則表示不應使用標頭來寫出實際的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-281">This key is optional and, if not specified, means that the actual metadata should not be written out with the header.</span></span>

### <a name="signing-a-metadata-handler"></a><span data-ttu-id="71e9f-282">簽署元資料處理程式</span><span class="sxs-lookup"><span data-stu-id="71e9f-282">Signing a Metadata Handler</span></span>

<span data-ttu-id="71e9f-283">所有元資料處理程式都必須經過數位簽署，才能參與 WIC 探索進程。</span><span class="sxs-lookup"><span data-stu-id="71e9f-283">All metadata handlers must be digitally signed to participate in the WIC discovery process.</span></span> <span data-ttu-id="71e9f-284">WIC 不會載入任何未由受信任的憑證授權單位單位簽署的處理常式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-284">WIC will not load any handler that is not signed by a trusted certificate authority.</span></span> <span data-ttu-id="71e9f-285">如需有關數位簽章的詳細資訊，請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="71e9f-285">For more information on digital signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="special-considerations"></a><span data-ttu-id="71e9f-286">特殊考慮</span><span class="sxs-lookup"><span data-stu-id="71e9f-286">Special Considerations</span></span>

<span data-ttu-id="71e9f-287">下列各節包含您在建立自己的元資料處理程式時，必須考慮的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-287">The following sections include additional information you must consider when creating your own metadata handlers.</span></span>

### <a name="propvariants"></a><span data-ttu-id="71e9f-288">PROPVARIANTS</span><span class="sxs-lookup"><span data-stu-id="71e9f-288">PROPVARIANTS</span></span>

<span data-ttu-id="71e9f-289">WIC 使用 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 來代表讀取和寫入的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="71e9f-289">WIC uses a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) to represent a metadata item for both reading and writing.</span></span> <span data-ttu-id="71e9f-290">PROPVARIANT 會針對元資料格式內使用的中繼資料專案，提供資料類型和資料值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-290">A PROPVARIANT provides a data type and data value for a metadata item used within a metadata format.</span></span> <span data-ttu-id="71e9f-291">做為元資料處理程式的寫入器，您有很大的彈性，可讓您以元資料格式儲存資料，以及如何在中繼資料區塊內表示資料。</span><span class="sxs-lookup"><span data-stu-id="71e9f-291">As the writer of a metadata handler, you have a lot of flexibility on how data is stored in the metadata format and how data is represented within a metadata block.</span></span> <span data-ttu-id="71e9f-292">下表提供的指導方針可協助您決定要在不同情況下使用的適當 PROPVARIANT 型別。</span><span class="sxs-lookup"><span data-stu-id="71e9f-292">The following table provides guidelines to help you decide on the appropriate PROPVARIANT type to use in different situations.</span></span>



| <span data-ttu-id="71e9f-293">元資料類型為 .。。</span><span class="sxs-lookup"><span data-stu-id="71e9f-293">Metadata type is...</span></span>          | <span data-ttu-id="71e9f-294">使用 PROPVARIANT 類型</span><span class="sxs-lookup"><span data-stu-id="71e9f-294">Use PROPVARIANT type</span></span>      | <span data-ttu-id="71e9f-295">PROPVARIANT 屬性</span><span class="sxs-lookup"><span data-stu-id="71e9f-295">PROPVARIANT Property</span></span>                                                                                                                                                                                                                                                           |
|------------------------------|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e9f-296">空白或不存在。</span><span class="sxs-lookup"><span data-stu-id="71e9f-296">Empty or non-existent.</span></span>       | <span data-ttu-id="71e9f-297">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="71e9f-297">VT\_EMPTY</span></span>                 | <span data-ttu-id="71e9f-298">不適用。</span><span class="sxs-lookup"><span data-stu-id="71e9f-298">Not applicable.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="71e9f-299">未定義。</span><span class="sxs-lookup"><span data-stu-id="71e9f-299">Undefined.</span></span>                   | <span data-ttu-id="71e9f-300">VT \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="71e9f-300">VT\_BLOB</span></span>                  | <span data-ttu-id="71e9f-301">使用 blob 屬性來設定使用 CoTaskMemAlloc 配置之 BLOB 物件的大小和指標。</span><span class="sxs-lookup"><span data-stu-id="71e9f-301">Use the blob property to set the size and pointer to the BLOB object allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="71e9f-302">中繼資料區塊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-302">A metadata block.</span></span>            | <span data-ttu-id="71e9f-303">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="71e9f-303">VT\_UNKNOWN</span></span>               | <span data-ttu-id="71e9f-304">此類型使用 punkVal 屬性。</span><span class="sxs-lookup"><span data-stu-id="71e9f-304">This type uses the punkVal property.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="71e9f-305">型別的陣列。</span><span class="sxs-lookup"><span data-stu-id="71e9f-305">An array of types.</span></span>           | <span data-ttu-id="71e9f-306">VT \_ 向量 \| VT \_ {type}</span><span class="sxs-lookup"><span data-stu-id="71e9f-306">VT\_VECTOR \| VT\_{type}</span></span>  | <span data-ttu-id="71e9f-307">使用 ca {type} 屬性來設定使用 CoTaskMemAlloc 配置之陣列的計數和指標。</span><span class="sxs-lookup"><span data-stu-id="71e9f-307">Use the ca{type} property to set the count and pointer to the array allocated using CoTaskMemAlloc.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="71e9f-308">中繼資料區塊的陣列。</span><span class="sxs-lookup"><span data-stu-id="71e9f-308">An array of metadata blocks.</span></span> | <span data-ttu-id="71e9f-309">VT \_ 向量 \| VT \_ 變異</span><span class="sxs-lookup"><span data-stu-id="71e9f-309">VT\_VECTOR \| VT\_VARIANT</span></span> | <span data-ttu-id="71e9f-310">您可以使用 capropvar 屬性來設定 variant 的陣列。</span><span class="sxs-lookup"><span data-stu-id="71e9f-310">Use the capropvar property to set the array of variants.</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="71e9f-311">帶正負號的有理數值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-311">A signed rational value.</span></span>     | <span data-ttu-id="71e9f-312">VT \_ I8</span><span class="sxs-lookup"><span data-stu-id="71e9f-312">VT\_I8</span></span>                    | <span data-ttu-id="71e9f-313">使用 hVal 屬性來設定值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-313">Use the hVal property to set the value.</span></span> <span data-ttu-id="71e9f-314">將 [高] 字組設為分母，然後將 [低] 字組設為分子。</span><span class="sxs-lookup"><span data-stu-id="71e9f-314">Set the high word to the denominator and the low word to the numerator.</span></span>                                                                                                                                                                |
| <span data-ttu-id="71e9f-315">有理數值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-315">A rational value.</span></span>            | <span data-ttu-id="71e9f-316">VT \_ UI8</span><span class="sxs-lookup"><span data-stu-id="71e9f-316">VT\_UI8</span></span>                   | <span data-ttu-id="71e9f-317">使用 uhVal 屬性來設定值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-317">Use the uhVal property to set the value.</span></span> <span data-ttu-id="71e9f-318">將 HighPart 設定為分母，並將 LowPart 設定為分子。</span><span class="sxs-lookup"><span data-stu-id="71e9f-318">Set the HighPart to the denominator and the LowPart to the numerator.</span></span> <span data-ttu-id="71e9f-319">請注意，LowPart 是不帶正負號的整數。分子應從不帶正負號的 int 轉換成 int，以確保會保留正負號位（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="71e9f-319">Note that the LowPart is an unsigned int. The numerator should be converted from an unsigned int to an int to ensure that the sign bit is preserved if present.</span></span> |



 

<span data-ttu-id="71e9f-320">若要避免代表陣列專案的重複專案，請不要使用安全陣列;只使用簡單的陣列。</span><span class="sxs-lookup"><span data-stu-id="71e9f-320">To avoid redundancy in representing array items, do not use safe arrays; use only simple arrays.</span></span> <span data-ttu-id="71e9f-321">這可減少應用程式在解讀 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 類型時需要執行的工作。</span><span class="sxs-lookup"><span data-stu-id="71e9f-321">This reduces the work an application needs to perform when interpreting [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) types.</span></span>

<span data-ttu-id="71e9f-322">請盡可能避免使用 `VT_BYREF` 和儲存值。</span><span class="sxs-lookup"><span data-stu-id="71e9f-322">Avoid using `VT_BYREF` and store values inline whenever possible.</span></span> <span data-ttu-id="71e9f-323">`VT_BYREF` 適用于小型類型 (常見的中繼資料專案) ，而且不提供大小資訊。</span><span class="sxs-lookup"><span data-stu-id="71e9f-323">`VT_BYREF` is inefficient for small types (common for metadata items) and does not provide size information.</span></span>

<span data-ttu-id="71e9f-324">在使用 [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)之前，請一律呼叫 **PropVariantInit** 來將值初始化。</span><span class="sxs-lookup"><span data-stu-id="71e9f-324">Before using a [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), always call **PropVariantInit** to initialize the value.</span></span> <span data-ttu-id="71e9f-325">當您完成 PROPVARIANT 時，請一律呼叫 **PropVariantClear** 來釋放配置給變數的任何記憶體。</span><span class="sxs-lookup"><span data-stu-id="71e9f-325">When you are finished with the PROPVARIANT, always call **PropVariantClear** to release any memory allocated for the variable.</span></span>

### <a name="8bim-handlers"></a><span data-ttu-id="71e9f-326">8BIM 處理常式</span><span class="sxs-lookup"><span data-stu-id="71e9f-326">8BIM Handlers</span></span>

<span data-ttu-id="71e9f-327">撰寫8BIM 中繼資料區塊的元資料處理程式時，您必須使用同時封裝8BIM 簽章和識別碼的簽章。</span><span class="sxs-lookup"><span data-stu-id="71e9f-327">When writing a metadata handler for an 8BIM metadata block, you must use a signature that encapsulates both the 8BIM signature and the ID.</span></span> <span data-ttu-id="71e9f-328">例如，原生8BIMIPTC 中繼資料讀取器會提供下列讀取器探索的登錄資訊：</span><span class="sxs-lookup"><span data-stu-id="71e9f-328">For example, the native 8BIMIPTC metadata reader provides the following registry information for reader discovery:</span></span>

``` syntax
[HKEY_CLASSES_ROOT\CLSID\{0010668C-0801-4DA6-A4A4-826522B6D28F}\Containers\{16100D66-8570-4BB9-B92D-FDA4B23ECE67}\0]
"Position"=dword:00000000
"Pattern"=hex:38,42,49,4d,04,04
"Mask"=hex:ff,ff,ff,ff,ff,ff
"DataOffset"=dword:00000006
```

<span data-ttu-id="71e9f-329">8BIMIPTC 讀取器具有已註冊的0x38、0x42、0x49、0x4D、0x04、0x04 模式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-329">The 8BIMIPTC reader has a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x04, 0x04.</span></span> <span data-ttu-id="71e9f-330">前四個位元組 (0x38、0x42、0x49、0x4D) 是8BIM 簽章，而最後兩個位元組 (0x04，0x04) 是 IPTC 記錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="71e9f-330">The first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature, and the last two bytes (0x04, 0x04) are the ID for the IPTC record.</span></span>

<span data-ttu-id="71e9f-331">因此，若要撰寫8BIM 中繼資料讀取器來取得解析資訊，您需要已註冊的0x38、0x42、0x49、0x4D、0x03、0xED 模式。</span><span class="sxs-lookup"><span data-stu-id="71e9f-331">So, to write an 8BIM metadata reader for resolution information, you would need a registered pattern of 0x38, 0x42, 0x49, 0x4D, 0x03, 0xED.</span></span> <span data-ttu-id="71e9f-332">同樣地，前四個位元組 (0x38、0x42、0x49、0x4D) 是8BIM 簽章。</span><span class="sxs-lookup"><span data-stu-id="71e9f-332">Again, the first four bytes (0x38, 0x42, 0x49, 0x4D) are the 8BIM signature.</span></span> <span data-ttu-id="71e9f-333">不過，最後兩個位元組 (0x03，0xED) ，則是由 PSD 格式所定義的解析資訊識別碼。</span><span class="sxs-lookup"><span data-stu-id="71e9f-333">The last two bytes (0x03, 0xED), however, are the resolution information ID as defined by the PSD format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71e9f-334">相關主題</span><span class="sxs-lookup"><span data-stu-id="71e9f-334">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="71e9f-335">**概念**</span><span class="sxs-lookup"><span data-stu-id="71e9f-335">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="71e9f-336">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="71e9f-336">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="71e9f-337">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="71e9f-337">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="71e9f-338">中繼資料查詢語言總覽</span><span class="sxs-lookup"><span data-stu-id="71e9f-338">Metadata Query Language Overview</span></span>](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[<span data-ttu-id="71e9f-339">讀取和寫入影像中繼資料的總覽</span><span class="sxs-lookup"><span data-stu-id="71e9f-339">Overview of Reading and Writing Image Metadata</span></span>](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[<span data-ttu-id="71e9f-340">How to：使用中繼資料重新編碼 JPEG 影像</span><span class="sxs-lookup"><span data-stu-id="71e9f-340">How-to: Re-encode a JPEG Image with Metadata</span></span>](-wic-codec-jpegmetadataencoding.md)
</dt> <dt>

<span data-ttu-id="71e9f-341">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="71e9f-341">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="71e9f-342">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="71e9f-342">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
