---
description: 執行 IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: 執行 IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026819"
---
# <a name="implementing-iwicbitmapdecoder"></a><span data-ttu-id="6d752-103">執行 IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="6d752-103">Implementing IWICBitmapDecoder</span></span>

## <a name="iwicbitmapdecoder"></a><span data-ttu-id="6d752-104">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="6d752-104">IWICBitmapDecoder</span></span>

<span data-ttu-id="6d752-105">當應用程式要求解碼器時，與編解碼器的第一個互動點是透過 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面。</span><span class="sxs-lookup"><span data-stu-id="6d752-105">When an application requests a decoder, the first point of interaction with the codec is through the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface.</span></span> <span data-ttu-id="6d752-106">這是容器層級介面，可讓您存取容器的最上層屬性，最重要的是它所包含的框架。</span><span class="sxs-lookup"><span data-stu-id="6d752-106">This is the container-level interface that provides access to the top-level properties of the container and, most importantly, the frames it contains.</span></span> <span data-ttu-id="6d752-107">這是容器層級的解碼器類別上的主要介面。</span><span class="sxs-lookup"><span data-stu-id="6d752-107">This is the primary interface on your container-level decoder class.</span></span>

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

<span data-ttu-id="6d752-108">某些影像格式具有全域縮圖、色彩內容或中繼資料，而許多影像格式都只針對每個畫面提供這些格式。</span><span class="sxs-lookup"><span data-stu-id="6d752-108">Some image formats have global thumbnails, color contexts, or metadata, while many image formats provide these only on a per-frame basis.</span></span> <span data-ttu-id="6d752-109">存取這些專案的方法在 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)上是選擇性的，但在 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)上是必要的。</span><span class="sxs-lookup"><span data-stu-id="6d752-109">The methods for accessing these items are optional on [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), but are required on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode).</span></span> <span data-ttu-id="6d752-110">同樣地，某些編解碼器不會使用索引像素格式，因此不需要在任何介面上執行 [CopyPalette](-wic-imp-iwicbitmapframedecode.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6d752-110">Likewise, some codecs do not use indexed pixel formats and so do not need to implement the [CopyPalette](-wic-imp-iwicbitmapframedecode.md) methods on either interface.</span></span> <span data-ttu-id="6d752-111">如需選擇性 **IWICBitmapDecoder** 方法的詳細資訊，請參閱實 [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)，其中最常見的方法是執行。</span><span class="sxs-lookup"><span data-stu-id="6d752-111">For more information on the optional **IWICBitmapDecoder** methods, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), where they are most commonly implemented.</span></span>

### <a name="querycapability"></a><span data-ttu-id="6d752-112">QueryCapability</span><span class="sxs-lookup"><span data-stu-id="6d752-112">QueryCapability</span></span>

<span data-ttu-id="6d752-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) 是用於編解碼器仲裁的方法。</span><span class="sxs-lookup"><span data-stu-id="6d752-113">[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is the method used for codec arbitration.</span></span> <span data-ttu-id="6d752-114"> (請參閱[Windows 影像處理元件運作方式](-wic-howwicworks.md)主題中的[探索和仲裁](-wic-howwicworks.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6d752-114">(See [Discovery and Arbitration](-wic-howwicworks.md) in the [How The Windows Imaging Component Works](-wic-howwicworks.md) topic).</span></span> <span data-ttu-id="6d752-115">如果兩個編解碼器能夠解碼相同的影像格式，或如果發生模式衝突，且兩個編解碼器使用相同的識別模式，則這個方法可讓您選取最能處理任何特定映射的編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6d752-115">If two codecs are capable of decoding the same image format, or if a pattern collision occurs in which two codecs use the same identifying pattern, this method allows you to select the codec that can best handle any specific image.</span></span>

<span data-ttu-id="6d752-116">叫用這個方法時，Windows 影像處理元件 (WIC) 會將包含影像的實際串流傳遞給您。</span><span class="sxs-lookup"><span data-stu-id="6d752-116">When invoking this method, Windows Imaging Component (WIC) passes you the actual stream containing the image.</span></span> <span data-ttu-id="6d752-117">您必須確認是否可以解碼影像內的每個畫面格，並列舉中繼資料區塊，以精確地宣告此解碼器對傳遞給它的特定檔案資料流程有哪些功能。</span><span class="sxs-lookup"><span data-stu-id="6d752-117">You must verify whether you can decode each frame within the image and enumerate through the metadata blocks, to accurately declare what capabilities this decoder has with respect to the specific file stream passed to it.</span></span> <span data-ttu-id="6d752-118">這對所有的解碼器而言很重要，但對於以標記的影像檔案格式為基礎的影像格式， (TIFF) 容器特別重要。</span><span class="sxs-lookup"><span data-stu-id="6d752-118">This is important for all decoders, but particularly important for image formats based on Tagged Image File Format (TIFF) containers.</span></span> <span data-ttu-id="6d752-119">探索進程的運作方式是將與登錄中的解碼器相關聯的模式比對實際影像檔案中的模式。</span><span class="sxs-lookup"><span data-stu-id="6d752-119">The discovery process works by matching patterns associated with decoders in the registry to patterns in the actual image file.</span></span> <span data-ttu-id="6d752-120">在登錄中宣告您的識別模式，可確保一律會針對影像格式的影像來偵測到您的解碼器。</span><span class="sxs-lookup"><span data-stu-id="6d752-120">Declaring your identifying pattern in the registry guarantees that your decoder will always be detected for images in your image format.</span></span> <span data-ttu-id="6d752-121">不過，您仍然可以針對其他格式的影像來偵測到您的解碼器。</span><span class="sxs-lookup"><span data-stu-id="6d752-121">However, your decoder could still be detected for images in other formats.</span></span> <span data-ttu-id="6d752-122">例如，所有 TIFF 容器都包含 TIFF 模式，這是 TIFF 影像格式的有效識別模式。</span><span class="sxs-lookup"><span data-stu-id="6d752-122">For example, all TIFF containers include the TIFF pattern, which is a valid identifying pattern for the TIFF image format.</span></span> <span data-ttu-id="6d752-123">這表示在探索期間，會在影像檔案中找到至少兩個識別模式，而影像格式是以 TIFF 樣式的容器為基礎。</span><span class="sxs-lookup"><span data-stu-id="6d752-123">This means that, during discovery, at least two identifying patterns will be found in image files for any image format that’s based on a TIFF-style container.</span></span> <span data-ttu-id="6d752-124">其中一個會是 TIFF 模式，另一個則是實際影像格式模式。</span><span class="sxs-lookup"><span data-stu-id="6d752-124">One will be the TIFF pattern and the other will be the actual image format pattern.</span></span> <span data-ttu-id="6d752-125">雖然不太可能，但其他不相關的影像格式也可能發生模式衝突。</span><span class="sxs-lookup"><span data-stu-id="6d752-125">While less likely, there could be pattern collisions between other unrelated image formats as well.</span></span> <span data-ttu-id="6d752-126">這就是為什麼探索和仲裁是兩階段的流程。</span><span class="sxs-lookup"><span data-stu-id="6d752-126">This is why discovery and arbitration is a two-stage process.</span></span> <span data-ttu-id="6d752-127">一律確認傳遞給 [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) 的影像資料流程實際上是您自己影像格式的有效實例。</span><span class="sxs-lookup"><span data-stu-id="6d752-127">Always verify that the image stream passed to [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) is actually a valid instance of your own image format.</span></span> <span data-ttu-id="6d752-128">此外，如果您的編解碼器解碼的影像格式不是您所擁有的規格，則您的 **QueryCapability** 執行應該檢查是否有任何可能在您的編解碼器未實行的影像格式規格下有效的功能。</span><span class="sxs-lookup"><span data-stu-id="6d752-128">Also, if your codec decodes an image format for which you don’t own the specification, your **QueryCapability** implementation should check for the presence of any feature that may be valid under the image format specification that your codec doesn’t implement.</span></span> <span data-ttu-id="6d752-129">這樣可確保使用者不會遇到不必要的解碼失敗，或使用您的編解碼器取得未預期的結果。</span><span class="sxs-lookup"><span data-stu-id="6d752-129">This will ensure that users do not experience unnecessary decoding failures or get unexpected results with your codec.</span></span>

<span data-ttu-id="6d752-130">在對影像執行任何作業之前，您必須先儲存資料流程的目前位置，以便您可以將它還原到其原始位置，然後再從方法返回。</span><span class="sxs-lookup"><span data-stu-id="6d752-130">Before performing any operation on the image, you must save the current position of the stream, so you can restore it to its original position before returning from the method.</span></span> <span data-ttu-id="6d752-131">指定功能的 [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) 列舉定義如下：</span><span class="sxs-lookup"><span data-stu-id="6d752-131">The [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) enumeration that specifies the capabilities is defined as follows:</span></span>

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

<span data-ttu-id="6d752-132">只有當您的編碼器是編碼影像的編碼器時，才應該宣告 **WICBitmapDecoderCapabilitySameEncoder** 。</span><span class="sxs-lookup"><span data-stu-id="6d752-132">You should declare **WICBitmapDecoderCapabilitySameEncoder** only if your encoder was the one that encoded the image.</span></span> <span data-ttu-id="6d752-133">在確認您是否可以解碼容器中的每個畫面格之後，如果您可以將部分（而非全部的框架）解碼，請 **WICBitmapDecoderCapabilityCanDecodeAllImages** **WICBitmapDecoderCapabilityCanDecodeSomeImages** 如果您可以解碼所有的框架，或不能將其解碼。</span><span class="sxs-lookup"><span data-stu-id="6d752-133">After verifying whether you can decode each frame in the container, declare either **WICBitmapDecoderCapabilityCanDecodeSomeImages** if you can decode some but not all of the frames, **WICBitmapDecoderCapabilityCanDecodeAllImages** if you can decode all of the frames, or neither if you cannot decode any of them.</span></span> <span data-ttu-id="6d752-134"> (這兩個列舉是互斥的;如果您傳回 **WICBitmapDecoderCapabilityCanDecodeAllImages**，則會忽略 **WICBitmapDecoderCapabilityCanDecodeSomeImages** 。在確認您可以列舉映射容器中的中繼資料區塊之後，) 宣告 **WICBitmapDecoderCapabilityCanEnumerateMetadata** 。</span><span class="sxs-lookup"><span data-stu-id="6d752-134">(These two enums are mutually exclusive; if you return **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** will be ignored.) Declare **WICBitmapDecoderCapabilityCanEnumerateMetadata** after verifying that you can enumerate through the metadata blocks in the image container.</span></span> <span data-ttu-id="6d752-135">您不必在每個畫面格中檢查縮圖。</span><span class="sxs-lookup"><span data-stu-id="6d752-135">You don’t have to check for a thumbnail in every frame.</span></span> <span data-ttu-id="6d752-136">如果有全域縮圖，而您可以將它解碼，則可以宣告 **WICBitmapDecoderCapabilityCanDecodeThumbnail**。</span><span class="sxs-lookup"><span data-stu-id="6d752-136">If there is a global thumbnail and you can decode it, you can declare **WICBitmapDecoderCapabilityCanDecodeThumbnail**.</span></span> <span data-ttu-id="6d752-137">如果沒有全域縮圖，則會嘗試將畫面格0的縮圖解碼。</span><span class="sxs-lookup"><span data-stu-id="6d752-137">If there is no global thumbnail, then attempt to decode the thumbnail for Frame 0.</span></span> <span data-ttu-id="6d752-138">如果其中一個位置沒有任何縮圖，請不要宣告這項功能。</span><span class="sxs-lookup"><span data-stu-id="6d752-138">If there is no thumbnail in either of these places, do not declare this capability.</span></span>

<span data-ttu-id="6d752-139">在判斷與傳遞給這個方法的影像資料流程相關的解碼器功能之後，請使用您已確認此解碼器可在此映射上執行的 [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) 來執行或作業，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="6d752-139">After determining the capabilities of the decoder with respect to the image stream passed to this method, perform an OR operation with the [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) you have verified that this decoder can perform on this image, and return the result.</span></span> <span data-ttu-id="6d752-140">請記得將資料流程還原至其原始位置，然後再返回。</span><span class="sxs-lookup"><span data-stu-id="6d752-140">Remember to restore the stream to its original position before returning.</span></span>

### <a name="initialize"></a><span data-ttu-id="6d752-141">初始化</span><span class="sxs-lookup"><span data-stu-id="6d752-141">Initialize</span></span>

<span data-ttu-id="6d752-142">在選取解碼器以解碼特定映射之後，應用程式會叫用 [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) 。</span><span class="sxs-lookup"><span data-stu-id="6d752-142">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) is invoked by an application after a decoder has been selected to decode a specific image.</span></span> <span data-ttu-id="6d752-143">影像資料流程會傳遞至解碼器，而且呼叫端可以選擇性地指定 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 快取選項來處理檔案中的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6d752-143">The image stream is passed to the decoder, and a caller may optionally specify the [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) cache option for dealing with the metadata in the file.</span></span>

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

<span data-ttu-id="6d752-144">有些應用程式使用的中繼資料比其他應用程式更多。</span><span class="sxs-lookup"><span data-stu-id="6d752-144">Some applications use metadata more than others.</span></span> <span data-ttu-id="6d752-145">大部分的應用程式不需要存取影像檔案中的所有中繼資料，而且會在需要時要求特定的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6d752-145">Most applications don’t need to access all the metadata in an image file, and will request specific metadata as they need it.</span></span> <span data-ttu-id="6d752-146">其他應用程式則會事先快取所有中繼資料，而不是讓檔案資料流程保持開啟，並且在每次需要存取中繼資料時執行磁片 i/o。</span><span class="sxs-lookup"><span data-stu-id="6d752-146">Other applications would rather cache all the metadata up front than keep the file stream open and perform disk I/O every time they need to access metadata.</span></span> <span data-ttu-id="6d752-147">如果呼叫端未指定中繼資料快取選項，預設的快取行為應該是快取的需求。</span><span class="sxs-lookup"><span data-stu-id="6d752-147">If the caller doesn’t specify a metadata cache option, the default caching behavior should be cache on demand.</span></span> <span data-ttu-id="6d752-148">這表示在應用程式對該中繼資料提出特定要求之前，不應該將中繼資料載入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="6d752-148">This means no metadata should be loaded into memory until the application makes a specific request for that metadata.</span></span> <span data-ttu-id="6d752-149">如果應用程式指定 **WICDecodeMetadataCacheOnLoad**，就應該立即在記憶體中載入中繼資料並加以快取。</span><span class="sxs-lookup"><span data-stu-id="6d752-149">If the application specifies **WICDecodeMetadataCacheOnLoad**, the metadata should be loaded in memory immediately and cached.</span></span> <span data-ttu-id="6d752-150">當載入中繼資料時，檔案資料流程可能會在快取中繼資料之後釋放。</span><span class="sxs-lookup"><span data-stu-id="6d752-150">When metadata is cached on load, the file stream may be released after the metadata has been cached.</span></span>

### <a name="getcontainerformat"></a><span data-ttu-id="6d752-151">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="6d752-151">GetContainerFormat</span></span>

<span data-ttu-id="6d752-152">若要執行 [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)，只需傳回已具現化之影像的影像格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="6d752-152">To implement [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), just return the GUID of the image format of the image for which the decoder is instantiated.</span></span> <span data-ttu-id="6d752-153">這個方法也會在 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 和 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上執行。</span><span class="sxs-lookup"><span data-stu-id="6d752-153">This method is also implemented on [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span>

### <a name="getdecoderinfo"></a><span data-ttu-id="6d752-154">GetDecoderInfo</span><span class="sxs-lookup"><span data-stu-id="6d752-154">GetDecoderInfo</span></span>

<span data-ttu-id="6d752-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) 會傳回 [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) 物件。</span><span class="sxs-lookup"><span data-stu-id="6d752-155">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) returns an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) object.</span></span> <span data-ttu-id="6d752-156">若要取得 **IWICBitmapDecoderInfo** 物件，只要將您的解碼器 GUID 傳遞至 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上的 [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)方法，然後在其上要求 **IWICBitmapDecoderInfo** 介面，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="6d752-156">To get the **IWICBitmapDecoderInfo** object, just pass the GUID of your decoder to the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method on [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), and then request the **IWICBitmapDecoderInfo** interface on it, as shown in the following example.</span></span>


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a><span data-ttu-id="6d752-157">GetFrameCount</span><span class="sxs-lookup"><span data-stu-id="6d752-157">GetFrameCount</span></span>

<span data-ttu-id="6d752-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) 只會傳回容器中的框架數目。</span><span class="sxs-lookup"><span data-stu-id="6d752-158">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) just returns the number of frames in the container.</span></span> <span data-ttu-id="6d752-159">某些容器格式支援多個框架，而其他則只支援每個容器一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="6d752-159">Some container formats support multiple frames, and others support only one frame per container.</span></span>

### <a name="getframe"></a><span data-ttu-id="6d752-160">GetFrame</span><span class="sxs-lookup"><span data-stu-id="6d752-160">GetFrame</span></span>

<span data-ttu-id="6d752-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) 是 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 介面上的重要方法，因為框架包含實際的影像位，而且從這個方法傳回的框架解碼物件是執行所要求影像之實際解碼的物件。</span><span class="sxs-lookup"><span data-stu-id="6d752-161">[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) is an important method on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) interface because the frame contains the actual image bits, and the frame decoder object returned from this method is the object that does the actual decoding of the requested image.</span></span> <span data-ttu-id="6d752-162">也就是您在撰寫解碼器時必須執行的另一個物件。</span><span class="sxs-lookup"><span data-stu-id="6d752-162">That is the other object you need to implement when writing a decoder.</span></span> <span data-ttu-id="6d752-163">如需框架解碼器的詳細資訊，請參閱 [執行 IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)。</span><span class="sxs-lookup"><span data-stu-id="6d752-163">For more information on frame decoders, see [Implementing IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).</span></span>

### <a name="getpreview"></a><span data-ttu-id="6d752-164">GetPreview</span><span class="sxs-lookup"><span data-stu-id="6d752-164">GetPreview</span></span>

<span data-ttu-id="6d752-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) 會傳回影像的預覽。</span><span class="sxs-lookup"><span data-stu-id="6d752-165">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) returns a preview of the image.</span></span> <span data-ttu-id="6d752-166">如需預覽的詳細討論，請參閱[執行 IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)介面上的實[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)方法。</span><span class="sxs-lookup"><span data-stu-id="6d752-166">For a detailed discussion of previews, see the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) method on the [Implementing IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) interface.</span></span>

<span data-ttu-id="6d752-167">如果您的影像格式包含內嵌的 JPEG 預覽，強烈建議您將其委派給 WIC 平臺隨附的 JPEG 解碼，以解碼預覽和縮圖，而不是撰寫 JPEG 解碼來將它解碼。</span><span class="sxs-lookup"><span data-stu-id="6d752-167">If your image format contains an embedded JPEG preview, it is strongly recommend that, instead of writing a JPEG decoder to decode it, you delegate to the JPEG decoder that ships with the WIC platform for decoding previews and thumbnails.</span></span> <span data-ttu-id="6d752-168">若要這樣做，請搜尋資料流程中的預覽影像資料開始，並在 [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)上叫用 [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法。</span><span class="sxs-lookup"><span data-stu-id="6d752-168">To do this, seek to the beginning of the preview image data in the stream and invoke the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method on the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a><span data-ttu-id="6d752-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d752-169">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d752-170">**參考**</span><span class="sxs-lookup"><span data-stu-id="6d752-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6d752-171">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="6d752-171">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="6d752-172">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="6d752-172">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="6d752-173">**概念**</span><span class="sxs-lookup"><span data-stu-id="6d752-173">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d752-174">解碼器介面</span><span class="sxs-lookup"><span data-stu-id="6d752-174">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="6d752-175">執行 IWICBitmapCodecProgressNotification (解碼器) </span><span class="sxs-lookup"><span data-stu-id="6d752-175">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="6d752-176">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="6d752-176">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="6d752-177">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="6d752-177">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



