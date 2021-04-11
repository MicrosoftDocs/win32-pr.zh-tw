---
description: 執行 IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: 執行 IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849506"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="9e857-103">執行 IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="9e857-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="9e857-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="9e857-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="9e857-105">多個中繼資料區塊通常存在於影像中，每個區塊都會以不同的格式公開不同類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="9e857-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="9e857-106">在 Windows 影像處理元件 (WIC) 模型中，元資料處理程式是在執行時間可搜尋的相異元件，例如，其為解碼器。</span><span class="sxs-lookup"><span data-stu-id="9e857-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="9e857-107">每個元資料格式都有個別的處理常式，而且每個元資料處理程式都可以搭配任何支援它所處理之元資料格式的影像格式使用。</span><span class="sxs-lookup"><span data-stu-id="9e857-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="9e857-108">因此，如果您的影像格式支援 EXIF、XMP、IPTC 或其他格式，您可以利用 WIC 隨附的這些格式的標準元資料處理程式，而不需要自行撰寫。</span><span class="sxs-lookup"><span data-stu-id="9e857-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="9e857-109">當然，如果您建立新的元資料格式，就必須撰寫它的元資料處理程式，它會在執行時間探索並叫用，就像標準的格式一樣。</span><span class="sxs-lookup"><span data-stu-id="9e857-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="9e857-110">如果您的影像格式是根據標記的影像檔案格式 (TIFF) 或 JPEG 容器，除非您) 建立新的或專屬的元資料格式，否則您不需要撰寫任何元資料處理程式 (。</span><span class="sxs-lookup"><span data-stu-id="9e857-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="9e857-111">在 TIFF 和 JPEG 容器中，中繼資料的區塊位於 IFDs 內，而每個容器都有不同的 IFD 結構。</span><span class="sxs-lookup"><span data-stu-id="9e857-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="9e857-112">WIC 提供這兩種容器格式的 IFD 處理常式，可流覽 IFD 結構並委派給標準元資料處理程式來存取它們內的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9e857-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="9e857-113">因此，如果您的映射格式是以其中一個容器為基礎，您就可以自動利用 WIC IFD 處理常式。</span><span class="sxs-lookup"><span data-stu-id="9e857-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="9e857-114">但是，如果您擁有專屬的容器格式，且其擁有專屬的最上層元資料結構，則必須撰寫可流覽該最上層結構並委派給適當元資料處理程式的處理常式，就像 IFD 處理常式一樣 ) </span><span class="sxs-lookup"><span data-stu-id="9e857-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="9e857-115">同樣地，WIC 也為應用程式提供了一層抽象概念，讓它們能夠透過一組一致的介面，以相同的方式處理所有影像格式，WIC 為編解碼器作者提供了元資料格式的抽象層。</span><span class="sxs-lookup"><span data-stu-id="9e857-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="9e857-116">如先前所述，編解碼器作者通常不需要直接使用影像中可能存在的各種元資料格式。</span><span class="sxs-lookup"><span data-stu-id="9e857-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="9e857-117">不過，每個編解碼器作者都必須負責提供方法來列舉中繼資料的區塊，以便探索並針對每個區塊來具現化適當的元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="9e857-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="9e857-118">您必須在您的框架層級解碼類別上執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="9e857-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="9e857-119">如果您的影像格式在任何個別影像框架之外公開全域中繼資料，您可能也需要在容器層級的解碼器類別上執行它。</span><span class="sxs-lookup"><span data-stu-id="9e857-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="9e857-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9e857-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="9e857-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="9e857-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="9e857-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="9e857-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="9e857-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="9e857-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="9e857-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="9e857-124">GetContainerFormat</span></span>

<span data-ttu-id="9e857-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)與 [執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)的 [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md)方法相同。</span><span class="sxs-lookup"><span data-stu-id="9e857-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="9e857-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="9e857-126">GetCount</span></span>

<span data-ttu-id="9e857-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) 會傳回與框架相關聯的最上層中繼資料區塊數目。</span><span class="sxs-lookup"><span data-stu-id="9e857-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="9e857-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="9e857-128">GetEnumerator</span></span>

<span data-ttu-id="9e857-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) 會傳回一個列舉值，呼叫者可以用來列舉框架中的中繼資料區塊，並讀取其中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9e857-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="9e857-130">若要執行這個方法，您必須為每個中繼資料區塊建立中繼資料讀取器，並執行列舉中繼資料讀取器集合的列舉物件。</span><span class="sxs-lookup"><span data-stu-id="9e857-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="9e857-131">列舉物件必須執行 [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) ，因此當您在 *ppIEnumMetadata* 參數中傳回它時，可以將它轉換成 IEnumUnknown。</span><span class="sxs-lookup"><span data-stu-id="9e857-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="9e857-132">在實作為列舉物件時，您可以在第一次建立 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 物件時或第一次建立列舉物件時建立所有中繼資料讀取器，也可以在 [IEnumUnknown：： Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) 方法的執行中延遲建立。</span><span class="sxs-lookup"><span data-stu-id="9e857-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="9e857-133">在許多情況下，更有效率地建立它們，但在下列範例中，區塊讀取器全都是在用來節省空間的函式中建立的。</span><span class="sxs-lookup"><span data-stu-id="9e857-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="9e857-134">若要建立中繼資料讀取器，請使用 [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) 方法。</span><span class="sxs-lookup"><span data-stu-id="9e857-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="9e857-135">叫用這個方法時，您會在 *guidContainerFormat* 參數中傳入容器格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9e857-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="9e857-136">如果您有針對中繼資料讀取器的廠商喜好設定，就可以在 *pGuidVendor* 參數中傳遞慣用廠商的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9e857-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="9e857-137">例如，如果您的公司寫入元資料處理程式，而您想要使用自己的（如果有的話），您可以傳入廠商的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9e857-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="9e857-138">在大部分的情況下，您只會傳遞 **Null**，讓系統選取適當的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="9e857-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="9e857-139">如果您要求特定廠商，而該廠商已在電腦上安裝中繼資料讀取器，WIC 將會傳回該廠商的讀者。</span><span class="sxs-lookup"><span data-stu-id="9e857-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="9e857-140">但是，如果要求的廠商未在電腦上安裝中繼資料讀取器，而且有適當的中繼資料讀取器可供使用，即使該讀取器不是來自慣用的廠商也會傳回。</span><span class="sxs-lookup"><span data-stu-id="9e857-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="9e857-141">如果電腦上沒有任何中繼資料讀取器可用於區塊中的元資料類型，則元件 factory 會傳回未知的元資料處理程式，此處理程式會將中繼資料的區塊視為二進位大型物件 (BLOB) ，而且會從檔案還原序列化中繼資料的區塊，而不會嘗試進行剖析。</span><span class="sxs-lookup"><span data-stu-id="9e857-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="9e857-142">針對 *>dwoptions* 參數，請使用適當的 [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)，在適當的 [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions)之間執行 OR 運算。</span><span class="sxs-lookup"><span data-stu-id="9e857-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="9e857-143">**WICPersistOptions** 描述容器的配置方式。預設值為位元組由小到大。</span><span class="sxs-lookup"><span data-stu-id="9e857-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="9e857-144">[**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)指定如果在可讀取特定區塊之元資料格式的電腦上找不到任何中繼資料讀取器，是否要取回 UnknownMetadataHandler。</span><span class="sxs-lookup"><span data-stu-id="9e857-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="9e857-145">**WICMetadataCreationAllowUnknown** 是預設值，您應該一律允許建立 UnknownMetadtataHandler。</span><span class="sxs-lookup"><span data-stu-id="9e857-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="9e857-146">UnknownMetadataHandler 會將無法辨識的中繼資料視為 BLOB。</span><span class="sxs-lookup"><span data-stu-id="9e857-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="9e857-147">它無法剖析它，但它會將它寫出到資料流程中做為 BLOB，並在編碼期間將資料寫回至資料流程時保持不變。</span><span class="sxs-lookup"><span data-stu-id="9e857-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="9e857-148">這可讓您安全地針對未隨附于系統的專屬中繼資料或元資料格式建立元資料處理程式。</span><span class="sxs-lookup"><span data-stu-id="9e857-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="9e857-149">因為中繼資料會原封不動地保留，即使電腦上沒有任何處理程式可辨識它，當適當的元資料處理程式稍後安裝時，中繼資料仍會存在且可供讀取。</span><span class="sxs-lookup"><span data-stu-id="9e857-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="9e857-150">如果您不允許建立 UnknownMetadataHandler，替代方法會捨棄或覆寫無法辨識的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9e857-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="9e857-151">這是一種資料遺失的形式。</span><span class="sxs-lookup"><span data-stu-id="9e857-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="9e857-152">如果您為專屬中繼資料撰寫自己的元資料處理程式，您永遠不應該包含中繼資料區塊本身以外的任何參考。</span><span class="sxs-lookup"><span data-stu-id="9e857-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="9e857-153">雖然 UnknownMetadataHandler 會保持中繼資料不變，但在編輯檔案時就會移動中繼資料，而在此情況下，任何對其本身區塊以外之任何參考的參考將不再有效。</span><span class="sxs-lookup"><span data-stu-id="9e857-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="9e857-154">*PIStream* 參數是您正在解碼的實際資料流程。</span><span class="sxs-lookup"><span data-stu-id="9e857-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="9e857-155">傳入串流之前，您應該先搜尋您要要求讀取器的中繼資料區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="9e857-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="9e857-156">在 [IStream](/windows/desktop/api/objidl/nn-objidl-istream) 的目前位置，中繼資料區塊的適當中繼資料讀取器會在 *ppiReader* 參數中傳回。</span><span class="sxs-lookup"><span data-stu-id="9e857-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="9e857-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="9e857-157">GetReaderByIndex</span></span>

<span data-ttu-id="9e857-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) 會傳回集合中要求之索引的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="9e857-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e857-159">相關主題</span><span class="sxs-lookup"><span data-stu-id="9e857-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9e857-160">**參考**</span><span class="sxs-lookup"><span data-stu-id="9e857-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9e857-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="9e857-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="9e857-162">**概念**</span><span class="sxs-lookup"><span data-stu-id="9e857-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9e857-163">執行 IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="9e857-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="9e857-164">執行 IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="9e857-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="9e857-165">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="9e857-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="9e857-166">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="9e857-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
