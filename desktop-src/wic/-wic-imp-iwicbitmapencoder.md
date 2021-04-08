---
description: 執行 IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: 執行 IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590dffcf762d22155a89a8143994d9a4d8bcab02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851219"
---
# <a name="implementing-iwicbitmapencoder"></a><span data-ttu-id="5c733-103">執行 IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="5c733-103">Implementing IWICBitmapEncoder</span></span>

-   [<span data-ttu-id="5c733-104">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="5c733-104">IWICBitmapEncoder</span></span>](#implementing-iwicbitmapencoder)
    -   [<span data-ttu-id="5c733-105">初始化</span><span class="sxs-lookup"><span data-stu-id="5c733-105">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="5c733-106">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="5c733-106">GetContainerFormat</span></span>](#getcontainerformat)
    -   [<span data-ttu-id="5c733-107">GetEncoderInfo</span><span class="sxs-lookup"><span data-stu-id="5c733-107">GetEncoderInfo</span></span>](#getencoderinfo)
    -   [<span data-ttu-id="5c733-108">CreateNewFrame</span><span class="sxs-lookup"><span data-stu-id="5c733-108">CreateNewFrame</span></span>](#createnewframe)
    -   [<span data-ttu-id="5c733-109">認可</span><span class="sxs-lookup"><span data-stu-id="5c733-109">Commit</span></span>](#commit)
    -   [<span data-ttu-id="5c733-110">SetPreview</span><span class="sxs-lookup"><span data-stu-id="5c733-110">SetPreview</span></span>](#setpreview)
-   [<span data-ttu-id="5c733-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c733-111">Related topics</span></span>](#related-topics)

## <a name="iwicbitmapencoder"></a><span data-ttu-id="5c733-112">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="5c733-112">IWICBitmapEncoder</span></span>

-   [<span data-ttu-id="5c733-113">初始化</span><span class="sxs-lookup"><span data-stu-id="5c733-113">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="5c733-114">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="5c733-114">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="5c733-115">GetEncoderInfo</span><span class="sxs-lookup"><span data-stu-id="5c733-115">GetEncoderInfo</span></span>](#getencoderinfo)
-   [<span data-ttu-id="5c733-116">CreateNewFrame</span><span class="sxs-lookup"><span data-stu-id="5c733-116">CreateNewFrame</span></span>](#createnewframe)
-   [<span data-ttu-id="5c733-117">認可</span><span class="sxs-lookup"><span data-stu-id="5c733-117">Commit</span></span>](#commit)
-   [<span data-ttu-id="5c733-118">SetPreview</span><span class="sxs-lookup"><span data-stu-id="5c733-118">SetPreview</span></span>](#setpreview)

<span data-ttu-id="5c733-119">這個介面是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面的對應項，而且是用來編碼影像檔案的起點。</span><span class="sxs-lookup"><span data-stu-id="5c733-119">This interface is the counterpart to the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface and is the starting point for encoding an image file.</span></span> <span data-ttu-id="5c733-120">如同 **IWICBitmapDecoder** 是用來從映射容器取得容器層級的屬性和個別的框架， [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 是用來設定容器層級的屬性，並將個別的影像框架序列化到容器中。</span><span class="sxs-lookup"><span data-stu-id="5c733-120">Just as **IWICBitmapDecoder** is used for retrieving container-level properties and individual frames from the image container, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) is used for setting container-level properties and serializing individual image frames into the container.</span></span> <span data-ttu-id="5c733-121">您可以在容器層級編碼器類別上執行此介面。</span><span class="sxs-lookup"><span data-stu-id="5c733-121">You implement this interface on your container-level encoder class.</span></span>

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

<span data-ttu-id="5c733-122">如同在實 [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)中所討論，某些影像格式具有全域縮圖、色彩內容或中繼資料，而許多影像格式都只會以每個畫面為基礎提供這些格式。</span><span class="sxs-lookup"><span data-stu-id="5c733-122">As discussed in [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="5c733-123">因此，設定這些方法的方法在 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上是選擇性的，但在 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)上是必要的。</span><span class="sxs-lookup"><span data-stu-id="5c733-123">Therefore, the methods for setting these are optional on [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), but are required on [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span> <span data-ttu-id="5c733-124">我們將在 **IWICBitmapFrameEncode** 上的 **IWICBitmapEncoder** 一節中討論選擇性的方法，這些方法是最常實作為的。</span><span class="sxs-lookup"><span data-stu-id="5c733-124">We’ll discuss the methods that are optional on **IWICBitmapEncoder** in the section on **IWICBitmapFrameEncode**, where they’re most commonly implemented.</span></span>

<span data-ttu-id="5c733-125">如果您不支援全域縮圖，請 \_ \_ 從 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上的 SetThumbnail 方法傳回 WINCODEC ERR CODECNOTHUMBNAIL。</span><span class="sxs-lookup"><span data-stu-id="5c733-125">If you don’t support global thumbnails, return WINCODEC\_ERR\_CODECNOTHUMBNAIL from the SetThumbnail method on [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="5c733-126">如果您不支援容器層級的選擇區，或您正在編碼的影像沒有已編制索引的格式，請 \_ \_ 從 SetPalette 方法傳回 WINCODEC ERR PALETTEUNAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="5c733-126">If you don’t support a container-level palette, or if the image you are encoding doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from the SetPalette method.</span></span> <span data-ttu-id="5c733-127">若為任何其他不支援的方法，則傳回 WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION。</span><span class="sxs-lookup"><span data-stu-id="5c733-127">For any other unsupported methods, return WINCODEC\_ERR\_UNSUPPORTEDOPERATION.</span></span>

### <a name="initialize"></a><span data-ttu-id="5c733-128">初始化</span><span class="sxs-lookup"><span data-stu-id="5c733-128">Initialize</span></span>

<span data-ttu-id="5c733-129">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) 是在 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) 具現化之後，在其上叫用的第一個方法。</span><span class="sxs-lookup"><span data-stu-id="5c733-129">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) is the first method invoked on an [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) after it has been instantiated.</span></span> <span data-ttu-id="5c733-130">影像串流會傳遞至編碼器，而呼叫端可以選擇性地指定快取選項。</span><span class="sxs-lookup"><span data-stu-id="5c733-130">An image stream is passed to the encoder, and a caller may optionally specify a cache option.</span></span> <span data-ttu-id="5c733-131">在解碼器的案例中，資料流程是唯讀的，但傳遞給編碼器的資料流程是可寫入的資料流程，編碼器會在其中序列化所有的影像資料和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="5c733-131">In the case of the decoder, the stream is read-only, but the stream passed to an encoder is a writeable stream, into which the encoder will serialize all of the image data and metadata.</span></span> <span data-ttu-id="5c733-132">編碼器上的快取選項也不同。</span><span class="sxs-lookup"><span data-stu-id="5c733-132">The cache options on the encoder are different as well.</span></span>

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

<span data-ttu-id="5c733-133">應用程式可選擇要求編碼器快取記憶體中的影像資料、將其快取到暫存檔案中，或直接寫入磁片檔案，而不需要快取。</span><span class="sxs-lookup"><span data-stu-id="5c733-133">The application has a choice of requesting the encoder to cache the image data in memory, cache it in a temporary file, or to write it directly into the disk file with no caching.</span></span> <span data-ttu-id="5c733-134">當系統要求您在暫存檔案中快取資料時，編碼器應該在磁片上建立暫存檔案，並直接寫入該檔案，而不在記憶體中快取。</span><span class="sxs-lookup"><span data-stu-id="5c733-134">When asked to cache the data in a temporary file, the encoder should create a temporary file on disk and write directly to that file without caching in memory.</span></span> <span data-ttu-id="5c733-135">當呼叫端選取 [無快取] 選項時，每個畫面格都必須依序認可，才能建立下一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="5c733-135">When the caller selects the no cache option, each frame must be committed in order before the next frame can be created.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="5c733-136">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="5c733-136">GetContainerFormat</span></span>

<span data-ttu-id="5c733-137">[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)的執行方式與 [執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)中的 [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md)方法相同。</span><span class="sxs-lookup"><span data-stu-id="5c733-137">[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) is implemented the same way as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method in [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getencoderinfo"></a><span data-ttu-id="5c733-138">GetEncoderInfo</span><span class="sxs-lookup"><span data-stu-id="5c733-138">GetEncoderInfo</span></span>

<span data-ttu-id="5c733-139">[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) 會傳回 [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) 物件。</span><span class="sxs-lookup"><span data-stu-id="5c733-139">[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) returns an [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) object.</span></span> <span data-ttu-id="5c733-140">若要取得 **IWICBitmapEncoderInfo** 物件，只需將您的編碼器 GUID 傳遞至 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上的 [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)方法，然後在其上要求 **IWICBitmapEncoderInfo** 介面。</span><span class="sxs-lookup"><span data-stu-id="5c733-140">To get the **IWICBitmapEncoderInfo** object, just pass the GUID of your encoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapEncoderInfo** interface on it.</span></span>

<span data-ttu-id="5c733-141">請參閱在[GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md)下[執行 IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)的範例。</span><span class="sxs-lookup"><span data-stu-id="5c733-141">See the example in [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) under [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="createnewframe"></a><span data-ttu-id="5c733-142">CreateNewFrame</span><span class="sxs-lookup"><span data-stu-id="5c733-142">CreateNewFrame</span></span>

<span data-ttu-id="5c733-143">[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)上 [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)的編碼器對應項。</span><span class="sxs-lookup"><span data-stu-id="5c733-143">[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) is the encoder counterpart of [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span> <span data-ttu-id="5c733-144">這個方法會傳回 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件，也就是實際序列化容器內特定框架之影像資料的物件。</span><span class="sxs-lookup"><span data-stu-id="5c733-144">This method returns an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object, which is the object that actually serializes the image data for a specific frame within the container.</span></span>

<span data-ttu-id="5c733-145">Windows 影像處理元件 (WIC) 的其中一個優點是，它為應用程式提供一個抽象層，讓它們以相同方式使用所有影像格式。</span><span class="sxs-lookup"><span data-stu-id="5c733-145">One of the benefits of Windows Imaging Component (WIC) is that it provides a layer of abstraction for applications that enables them to work with all image formats in the same way.</span></span> <span data-ttu-id="5c733-146">不過，並非所有的影像格式都完全相同。</span><span class="sxs-lookup"><span data-stu-id="5c733-146">However, not all image formats are exactly the same.</span></span> <span data-ttu-id="5c733-147">某些影像格式具有其他人沒有的功能。</span><span class="sxs-lookup"><span data-stu-id="5c733-147">Some image formats have capabilities that others don’t have.</span></span> <span data-ttu-id="5c733-148">為了讓應用程式能夠利用這些獨特的功能，必須提供方法讓編解碼器公開。</span><span class="sxs-lookup"><span data-stu-id="5c733-148">For applications to be able to take advantage of those unique capabilities, it’s necessary to provide a way for the codec to expose them.</span></span> <span data-ttu-id="5c733-149">這是編碼器選項的用途。</span><span class="sxs-lookup"><span data-stu-id="5c733-149">This is the purpose of encoder options.</span></span> <span data-ttu-id="5c733-150">如果您的編解碼器支援任何編碼器選項，您應該建立一個 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 物件來公開您支援的編碼器選項，然後在此方法的 *ppIEncoderOptions* 參數中傳回該物件。</span><span class="sxs-lookup"><span data-stu-id="5c733-150">If your codec supports any encoder options, you should create an [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) object that exposes the encoder options you support, and return it in the *ppIEncoderOptions* parameter of this method.</span></span> <span data-ttu-id="5c733-151">接著，呼叫者可以使用這個 IPropertyBag2 物件來判斷編解碼器支援的編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="5c733-151">The caller can then use this IPropertyBag2 object to determine what encoder options your codec supports.</span></span> <span data-ttu-id="5c733-152">如果呼叫端想要為任何支援的編碼器選項指定值，則會將值指派給 IPropertyBag2 物件中的相關屬性，並在其 Initialize 方法中將其傳遞至新建立的 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件。</span><span class="sxs-lookup"><span data-stu-id="5c733-152">If the caller wants to specify values for any of the supported encoder options, they will assign the value to the relevant property in the IPropertyBag2 object and pass it to the newly created [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object in its Initialize method.</span></span>

<span data-ttu-id="5c733-153">若要具現化 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) 物件，您必須先建立 PROPBAG2 結構來指定編碼器支援的每個編碼器選項，以及每個屬性的資料類型。</span><span class="sxs-lookup"><span data-stu-id="5c733-153">To instantiate an [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) object, you first need to create a PROPBAG2 struct to specify each encoder option your encoder supports and its data type for each property.</span></span> <span data-ttu-id="5c733-154">然後，您必須執行 IPropertyBag2 物件，以在寫入時強制執行每個屬性的值範圍，並調解任何衝突或重迭的值。</span><span class="sxs-lookup"><span data-stu-id="5c733-154">Then you must implement an IPropertyBag2 object that enforces the value ranges for each property on write, and reconciles any conflicting or overlapping values.</span></span> <span data-ttu-id="5c733-155">針對簡單的非衝突編碼器選項組，您可以叫用 [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) 方法，它會使用您在 PROPBAG2 結構中指定的屬性來建立簡單的 IPropertyBag2 物件。</span><span class="sxs-lookup"><span data-stu-id="5c733-155">For simple sets of non-conflicting encoder options, you can invoke the [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) method, which will create a simple IPropertyBag2 object using the properties you specify in your PROPBAG2 struct.</span></span> <span data-ttu-id="5c733-156">您仍然必須強制執行值範圍。</span><span class="sxs-lookup"><span data-stu-id="5c733-156">You must still enforce the value ranges.</span></span> <span data-ttu-id="5c733-157">如需更高階的編碼器選項，或如果您需要協調衝突的值，您應該撰寫自己的 IPropertyBag2 執行。</span><span class="sxs-lookup"><span data-stu-id="5c733-157">For more advanced encoder options, or if you need to reconcile conflicting values, you should write your own IPropertyBag2 implementation.</span></span>


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



<span data-ttu-id="5c733-158">WIC 提供一些常用影像格式所使用的一組標準編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="5c733-158">WIC provides a small set of canonical encoder options that are used by some of the common image formats.</span></span> <span data-ttu-id="5c733-159">所有標準編碼器選項都是選擇性的，且不需要編解碼器就能支援它們。</span><span class="sxs-lookup"><span data-stu-id="5c733-159">All of the canonical encoder options are optional, and codecs are not required to support any of them.</span></span> <span data-ttu-id="5c733-160">提供這些標準選項的原因是因為許多應用程式會公開使用者介面，讓使用者在以支援這些選項的格式儲存影像檔時指定這些選項。</span><span class="sxs-lookup"><span data-stu-id="5c733-160">The reason they are provided as canonical options is because many applications expose the user interface for users to specify these options when saving an image file in a format that supports them.</span></span> <span data-ttu-id="5c733-161">提供標準方式來指定這些選項，可讓應用程式輕鬆地以一致的方式將它們傳達給編碼器。</span><span class="sxs-lookup"><span data-stu-id="5c733-161">Providing a canonical way to specify these options makes it easy for applications to communicate them to encoders in a consistent way.</span></span> <span data-ttu-id="5c733-162">標準編碼器選項列于下表。</span><span class="sxs-lookup"><span data-stu-id="5c733-162">The canonical encoder options are listed in the following table.</span></span>



| <span data-ttu-id="5c733-163">編碼器選項</span><span class="sxs-lookup"><span data-stu-id="5c733-163">Encoder Option</span></span>     | <span data-ttu-id="5c733-164">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5c733-164">VARTYPE</span></span>  | <span data-ttu-id="5c733-165">值範圍</span><span class="sxs-lookup"><span data-stu-id="5c733-165">Value Range</span></span>               |
|--------------------|----------|---------------------------|
| <span data-ttu-id="5c733-166">Lossless</span><span class="sxs-lookup"><span data-stu-id="5c733-166">Lossless</span></span>           | <span data-ttu-id="5c733-167">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="5c733-167">VT\_BOOL</span></span> | <span data-ttu-id="5c733-168">True/False</span><span class="sxs-lookup"><span data-stu-id="5c733-168">True/False</span></span>                |
| <span data-ttu-id="5c733-169">ImageQuality</span><span class="sxs-lookup"><span data-stu-id="5c733-169">ImageQuality</span></span>       | <span data-ttu-id="5c733-170">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5c733-170">VT\_R4</span></span>   | <span data-ttu-id="5c733-171">0.0-1。0</span><span class="sxs-lookup"><span data-stu-id="5c733-171">0.0-1.0</span></span>                   |
| <span data-ttu-id="5c733-172">CompressionQuality</span><span class="sxs-lookup"><span data-stu-id="5c733-172">CompressionQuality</span></span> | <span data-ttu-id="5c733-173">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5c733-173">VT\_R4</span></span>   | <span data-ttu-id="5c733-174">0.0-1。0</span><span class="sxs-lookup"><span data-stu-id="5c733-174">0.0-1.0</span></span>                   |
| <span data-ttu-id="5c733-175">BitmapTransform</span><span class="sxs-lookup"><span data-stu-id="5c733-175">BitmapTransform</span></span>    | <span data-ttu-id="5c733-176">VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5c733-176">VT\_UI1</span></span>  | <span data-ttu-id="5c733-177">WICBitmapTransformOptions</span><span class="sxs-lookup"><span data-stu-id="5c733-177">WICBitmapTransformOptions</span></span> |



 

<span data-ttu-id="5c733-178">如果您的編解碼器支援不失真編碼，您應該公開不失真編碼器選項，讓應用程式要求以 losslessly 編碼的影像。</span><span class="sxs-lookup"><span data-stu-id="5c733-178">If your codec supports lossless encoding, you should expose the Lossless encoder option as a way for applications to request that an image be losslessly encoded.</span></span> <span data-ttu-id="5c733-179">如果呼叫端將此屬性設定為 True，您應該忽略 ImageQuality 選項，並將影像 losslessly 編碼。</span><span class="sxs-lookup"><span data-stu-id="5c733-179">If a caller sets this property to True, you should ignore the ImageQuality option and encode the image losslessly.</span></span>

<span data-ttu-id="5c733-180">ImageQuality 選項可讓應用程式指定用來編碼影像的精確度程度。</span><span class="sxs-lookup"><span data-stu-id="5c733-180">The ImageQuality option allows an application to specify the degree of fidelity with which to encode the image.</span></span> <span data-ttu-id="5c733-181">此選項可讓使用者在影像品質與速度及/或檔案大小之間進行取捨。</span><span class="sxs-lookup"><span data-stu-id="5c733-181">This option lets a user make a tradeoff between image quality versus speed and/or file size.</span></span> <span data-ttu-id="5c733-182">JPEG 是支援此取捨的影像格式範例。</span><span class="sxs-lookup"><span data-stu-id="5c733-182">JPEG is an example of an image format that supports this tradeoff.</span></span> <span data-ttu-id="5c733-183">值為0.0 表示精確度為低重要性，而且編碼器應使用其最大量的演算法。</span><span class="sxs-lookup"><span data-stu-id="5c733-183">A value of 0.0 indicates that fidelity is of low importance and the encoder should use its most lossy algorithm.</span></span> <span data-ttu-id="5c733-184">值為1.0 表示精確度是最重要的，而且編碼器應該盡可能保留最高的精確度。</span><span class="sxs-lookup"><span data-stu-id="5c733-184">A value of 1.0 indicates that fidelity is the most important and the encoder should preserve the highest fidelity possible.</span></span> <span data-ttu-id="5c733-185">根據您的編解碼器 (，這可能與不失真選項同義。</span><span class="sxs-lookup"><span data-stu-id="5c733-185">(Depending on your codec, this may be synonymous with the Lossless option.</span></span> <span data-ttu-id="5c733-186">但是，如果您的編解碼器支援不失真編碼，而且不失真選項設定為 True，則應忽略 ImageQuality 選項。 ) </span><span class="sxs-lookup"><span data-stu-id="5c733-186">However, if your codec supports lossless encoding, and if the Lossless option is set to True, the ImageQuality option should be ignored.)</span></span>

<span data-ttu-id="5c733-187">CompressionQuality 選項可讓應用程式指定將影像編碼時所要使用的壓縮效率。</span><span class="sxs-lookup"><span data-stu-id="5c733-187">The CompressionQuality option allows an application to specify the efficiency of compression to use when encoding the image.</span></span> <span data-ttu-id="5c733-188">非常有效率的演算法可能會產生較小的影像檔案品質與較低效率的壓縮演算法相同，但編碼可能需要較長的時間。</span><span class="sxs-lookup"><span data-stu-id="5c733-188">A very efficient algorithm may produce a smaller image file with the same quality as a less efficient compression algorithm, but may take longer to encode.</span></span> <span data-ttu-id="5c733-189">此選項可讓使用者指定檔案大小與編碼速度之間的取捨，同時保留相同等級的品質。</span><span class="sxs-lookup"><span data-stu-id="5c733-189">This option lets a user specify a tradeoff between file size versus speed of encoding, while preserving the same level of quality.</span></span> <span data-ttu-id="5c733-190">TIFF 是支援此取捨的影像格式範例。</span><span class="sxs-lookup"><span data-stu-id="5c733-190">TIFF is an example of an image format that supports this tradeoff.</span></span> <span data-ttu-id="5c733-191"> (請注意，JPEG 之類的格式支援不同層級的壓縮，但較高的壓縮率會產生較低的影像品質。</span><span class="sxs-lookup"><span data-stu-id="5c733-191">(Note that a format such as JPEG supports different levels of compression, but a higher rate of compression results in lower image quality.</span></span> <span data-ttu-id="5c733-192">因此，JPEG 影像格式會公開 ImageQuality 選項，而不是 CompressionQuality 選項。針對此選項 ) 0.0 的值，表示您應該儘快壓縮影像，而不會降低精確度，因為較大的檔案大小。</span><span class="sxs-lookup"><span data-stu-id="5c733-192">Therefore, a JPEG image format would expose the ImageQuality option rather than the CompressionQuality option.) A value of 0.0 for this option indicates that you should compress the image as quickly as possible, without reducing fidelity, at the expense of a larger file size.</span></span> <span data-ttu-id="5c733-193">值為1.0 時，表示您應該在相同的品質) 層級上建立最小的可能檔案大小 (，而不論其編碼所需的時間長度為何。</span><span class="sxs-lookup"><span data-stu-id="5c733-193">A value of 1.0 indicates that you should create the smallest possible file size (at the same level of quality), regardless of how long it may take to encode it.</span></span> <span data-ttu-id="5c733-194">編解碼器可以同時支援 ImageQuality 選項和 CompressionQuality 選項，其中 ImageQuality 選項會指定 lossiness 的可接受程度，而 CompressionQuality 選項則會在指定的品質層級提供大小/速度的取捨。</span><span class="sxs-lookup"><span data-stu-id="5c733-194">A codec can support both the ImageQuality option and the CompressionQuality option, where the ImageQuality option specifies the acceptable degree of lossiness, and the CompressionQuality option offers a size/speed tradeoff at the specified quality level.</span></span>

<span data-ttu-id="5c733-195">BitmapTransform 選項提供一個方法，讓呼叫端在編碼時指定旋轉角度或垂直或水準翻轉方向。</span><span class="sxs-lookup"><span data-stu-id="5c733-195">The BitmapTransform option provides a way for the caller to specify a rotation angle or vertical or horizontal flip orientation when encoding.</span></span> <span data-ttu-id="5c733-196">用來指定所要求之轉換的 WICBitmapTransformOptions 列舉，與透過 IWICBitmapSourceTransform 介面進行解碼期間要求轉換時所用的列舉相同。</span><span class="sxs-lookup"><span data-stu-id="5c733-196">The WICBitmapTransformOptions enum used to specify the requested transform is the same enum used when requesting a transform during decoding through the IWICBitmapSourceTransform interface.</span></span>

<span data-ttu-id="5c733-197">請注意，編碼器不限於標準編碼器選項。</span><span class="sxs-lookup"><span data-stu-id="5c733-197">Note that encoders are not limited to the canonical encoder options.</span></span> <span data-ttu-id="5c733-198">編碼器選項的目的是要讓編碼器公開其功能，而且您可以公開的功能類型沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="5c733-198">The purpose of encoder options is to enable encoders to expose their capabilities, and there is no limit to the types of capabilities you can expose.</span></span> <span data-ttu-id="5c733-199">請確定您的編碼器選項有妥善記載。</span><span class="sxs-lookup"><span data-stu-id="5c733-199">Make sure your encoder options are well-documented.</span></span> <span data-ttu-id="5c733-200">雖然應用程式可以使用您從這個方法傳回的屬性包，來探索您支援之選項的名稱、類型和值範圍，但它們的唯一方法是從您的檔中找出其意義，或如何在使用者介面中加以公開。</span><span class="sxs-lookup"><span data-stu-id="5c733-200">Even though an application can use the property bag you return from this method to discover the names, types, and value ranges for the options you support, the only way for them to find out their meanings, or how to expose them in the user interface, is from your documentation.</span></span>

### <a name="commit"></a><span data-ttu-id="5c733-201">Commit</span><span class="sxs-lookup"><span data-stu-id="5c733-201">Commit</span></span>

<span data-ttu-id="5c733-202">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) 是在所有的影像資料和中繼資料都已序列化為數據流之後，您所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="5c733-202">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) is the method you call after all the image data and metadata have been serialized into the stream.</span></span> <span data-ttu-id="5c733-203">您應使用此方法將預覽影像資料序列化為數據流，以及任何全域縮圖、中繼資料、調色板或其他專案（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="5c733-203">You should use this method to serialize the Preview image data into the stream, and any global thumbnails, metadata, palette, or other items, if applicable.</span></span> <span data-ttu-id="5c733-204">這個方法不應該關閉檔案資料流程，因為開啟資料流程的應用程式應該會關閉它。</span><span class="sxs-lookup"><span data-stu-id="5c733-204">This method should not close the file stream, because the application that opened the stream is expected to close it.</span></span>

<span data-ttu-id="5c733-205">IWICBitmapFrameEncode： Commit 方法的區段有 IWICBitmapEncoderCacheOptions 如何影響此方法行為的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5c733-205">The section on the IWICBitmapFrameEncode:Commit method has details on how the IWICBitmapEncoderCacheOptions affect the behavior of this method.</span></span>

### <a name="setpreview"></a><span data-ttu-id="5c733-206">SetPreview</span><span class="sxs-lookup"><span data-stu-id="5c733-206">SetPreview</span></span>

<span data-ttu-id="5c733-207">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) 用來建立映射的預覽。</span><span class="sxs-lookup"><span data-stu-id="5c733-207">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is used to create a preview of the image.</span></span> <span data-ttu-id="5c733-208">雖然並非絕對要求每個影像都有預覽，但強烈建議您這麼做。</span><span class="sxs-lookup"><span data-stu-id="5c733-208">While it is not strictly required that every image have a preview, it is highly recommended.</span></span> <span data-ttu-id="5c733-209">新式數位攝影機和掃描器會產生非常高的解析度影像，通常很大，因此需要大量的處理時間來進行解碼。</span><span class="sxs-lookup"><span data-stu-id="5c733-209">Modern digital cameras and scanners generate very high resolution images, which tend to be very large and, consequently, take significant processing time to decode.</span></span> <span data-ttu-id="5c733-210">下一代攝影機的影像會更大。</span><span class="sxs-lookup"><span data-stu-id="5c733-210">Images from the next generation of cameras will be even larger.</span></span> <span data-ttu-id="5c733-211">最好提供較小、較低解析度的影像版本（通常是 JPEG 格式），當使用者要求它時，可以快速解碼並「立即」顯示。</span><span class="sxs-lookup"><span data-stu-id="5c733-211">It’s a good idea to provide a smaller, lower resolution version of an image, typically in JPEG format, that can be quickly decoded and displayed “instantly” when a user requests it.</span></span> <span data-ttu-id="5c733-212">應用程式可能會在要求實際影像進行解碼之前要求預覽，以提供更好的使用者體驗，並在 theyare 等候解碼實際影像時顯示影像的螢幕大小表示。</span><span class="sxs-lookup"><span data-stu-id="5c733-212">An application may request a preview before requesting the actual image to be decoded to provide a better experience for users, and show them a screen-size representation of the image while theyare waiting to decode the actual image.</span></span> <span data-ttu-id="5c733-213">雖然編解碼器應該提供預覽，但不支援 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 的編解碼器絕對應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="5c733-213">Although codecs should provide previews, codecs that do not support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) should definitely do so.</span></span>

<span data-ttu-id="5c733-214">如果您提供 JPEG 預覽，就不需要撰寫 JPEG 編碼器來編碼。</span><span class="sxs-lookup"><span data-stu-id="5c733-214">If you provide a JPEG preview, you don’t have to write a JPEG encoder to encode it.</span></span> <span data-ttu-id="5c733-215">您應委派給 WIC 平臺隨附的 JPEG 編碼器，以將預覽和縮圖編碼。</span><span class="sxs-lookup"><span data-stu-id="5c733-215">You should delegate to the JPEG encoder that ships with the WIC platform for encoding both previews and thumbnails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c733-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c733-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c733-217">**參考**</span><span class="sxs-lookup"><span data-stu-id="5c733-217">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c733-218">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="5c733-218">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[<span data-ttu-id="5c733-219">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="5c733-219">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

<span data-ttu-id="5c733-220">**概念**</span><span class="sxs-lookup"><span data-stu-id="5c733-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c733-221">編碼器介面</span><span class="sxs-lookup"><span data-stu-id="5c733-221">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="5c733-222">執行 IWICBitmapCodecProgressNotification (編碼器) </span><span class="sxs-lookup"><span data-stu-id="5c733-222">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="5c733-223">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="5c733-223">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5c733-224">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="5c733-224">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
