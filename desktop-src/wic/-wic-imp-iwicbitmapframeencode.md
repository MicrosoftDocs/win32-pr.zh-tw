---
description: 執行 IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: 執行 IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194128"
---
# <a name="implementing-iwicbitmapframeencode"></a><span data-ttu-id="4be33-103">執行 IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="4be33-103">Implementing IWICBitmapFrameEncode</span></span>

## <a name="iwicbitmapframeencode"></a><span data-ttu-id="4be33-104">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="4be33-104">IWICBitmapFrameEncode</span></span>

<span data-ttu-id="4be33-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 是 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 介面的編碼器對應項。</span><span class="sxs-lookup"><span data-stu-id="4be33-105">[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) is the encoder’s counterpart to the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span> <span data-ttu-id="4be33-106">您可以在框架層級編碼類別上執行這個介面，這是針對每個框架執行影像位實際編碼的類別。</span><span class="sxs-lookup"><span data-stu-id="4be33-106">You can implement this interface on your frame-level encoding class, which is the class that does the actual encoding of the image bits for each frame.</span></span>


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [<span data-ttu-id="4be33-107">初始化</span><span class="sxs-lookup"><span data-stu-id="4be33-107">Initialize</span></span>](#initialize)
-   [<span data-ttu-id="4be33-108">SetSize 和 SetResolution</span><span class="sxs-lookup"><span data-stu-id="4be33-108">SetSize and SetResolution</span></span>](#setsize-and-setresolution)
-   [<span data-ttu-id="4be33-109">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="4be33-109">SetPixelFormat</span></span>](#setpixelformat)
-   [<span data-ttu-id="4be33-110">SetColorCoNtexts</span><span class="sxs-lookup"><span data-stu-id="4be33-110">SetColorContexts</span></span>](#setcolorcontexts)
-   [<span data-ttu-id="4be33-111">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="4be33-111">GetMetadataQueryWriter</span></span>](#getmetadataquerywriter)
-   [<span data-ttu-id="4be33-112">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="4be33-112">SetThumbnail</span></span>](#setthumbnail)
-   [<span data-ttu-id="4be33-113">WritePixels</span><span class="sxs-lookup"><span data-stu-id="4be33-113">WritePixels</span></span>](#writepixels)
-   [<span data-ttu-id="4be33-114">WriteSource</span><span class="sxs-lookup"><span data-stu-id="4be33-114">WriteSource</span></span>](#writesource)
-   [<span data-ttu-id="4be33-115">認可</span><span class="sxs-lookup"><span data-stu-id="4be33-115">Commit</span></span>](#commit)
-   [<span data-ttu-id="4be33-116">SetPalette</span><span class="sxs-lookup"><span data-stu-id="4be33-116">SetPalette</span></span>](#setpalette)

### <a name="initialize"></a><span data-ttu-id="4be33-117">初始化</span><span class="sxs-lookup"><span data-stu-id="4be33-117">Initialize</span></span>

<span data-ttu-id="4be33-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) 是在 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件具現化之後，在該物件上叫用的第一個方法。</span><span class="sxs-lookup"><span data-stu-id="4be33-118">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) is the first method invoked on an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object after it has been instantiated.</span></span> <span data-ttu-id="4be33-119">這個方法有一個參數，可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4be33-119">This method has one parameter, which may be set to **NULL**.</span></span> <span data-ttu-id="4be33-120">此參數代表編碼器選項，和您在容器層級解碼器的 [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)方法中建立的相同 [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))實例，並在該方法的 pIEncoderOptions 參數中傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="4be33-120">This parameter represents the encoder options, and is the same [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) instance that you created in the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method on the container-level decoder, and passed back to the caller in the pIEncoderOptions parameter of that method.</span></span> <span data-ttu-id="4be33-121">屆時，您已填入 IPropertyBag2 結構，其中包含的屬性代表您的框架層級編碼器所支援的編碼選項。</span><span class="sxs-lookup"><span data-stu-id="4be33-121">At that time, you populated the IPropertyBag2 struct with properties that represent the encoding options supported by your frame-level encoder.</span></span> <span data-ttu-id="4be33-122">呼叫端現在已提供這些屬性的值，以指出特定編碼選項參數，並將相同的物件傳回給您，以初始化 **IWICBitmapFrameEncode** 物件。</span><span class="sxs-lookup"><span data-stu-id="4be33-122">The caller has now provided values for those properties to indicate certain encoding option parameters, and is passing the same object back to you to initialize the **IWICBitmapFrameEncode** object.</span></span> <span data-ttu-id="4be33-123">編碼影像位時，您應該套用指定的選項。</span><span class="sxs-lookup"><span data-stu-id="4be33-123">You should apply the specified options when encoding the image bits.</span></span>

### <a name="setsize-and-setresolution"></a><span data-ttu-id="4be33-124">SetSize 和 SetResolution</span><span class="sxs-lookup"><span data-stu-id="4be33-124">SetSize and SetResolution</span></span>

<span data-ttu-id="4be33-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) 和 [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) 很容易理解。</span><span class="sxs-lookup"><span data-stu-id="4be33-125">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) and [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) are self-explanatory.</span></span> <span data-ttu-id="4be33-126">呼叫端會使用這些方法來指定編碼影像的大小和解析度。</span><span class="sxs-lookup"><span data-stu-id="4be33-126">The caller uses these methods to specify the size and resolution for the encoded image.</span></span>

### <a name="setpixelformat"></a><span data-ttu-id="4be33-127">SetPixelFormat</span><span class="sxs-lookup"><span data-stu-id="4be33-127">SetPixelFormat</span></span>

<span data-ttu-id="4be33-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) 是用來要求用來將影像編碼的像素格式。</span><span class="sxs-lookup"><span data-stu-id="4be33-128">[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) is used to request a pixel format in which to encode the image.</span></span> <span data-ttu-id="4be33-129">如果要求的像素格式不受支援，您應該傳回 *pPixelFormat* 所支援的最接近像素格式的 GUID，也就是 in/out 參數。</span><span class="sxs-lookup"><span data-stu-id="4be33-129">If the requested pixel format is not supported, you should return the GUID of the closest pixel format that is supported in *pPixelFormat*, which is an in/out parameter.</span></span>

### <a name="setcolorcontexts"></a><span data-ttu-id="4be33-130">SetColorCoNtexts</span><span class="sxs-lookup"><span data-stu-id="4be33-130">SetColorContexts</span></span>

<span data-ttu-id="4be33-131">[**SetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) 可用來指定一個或多個有效的色彩內容 (也稱為色彩設定檔) 用於此影像。</span><span class="sxs-lookup"><span data-stu-id="4be33-131">[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) is used to specify one or more valid color contexts (also known as color profiles) for this image.</span></span> <span data-ttu-id="4be33-132">請務必指定色彩內容，如此一來，稍後再將影像解碼的應用程式就可以從來源色彩設定檔轉換成用來顯示或列印影像之裝置的目的地設定檔。</span><span class="sxs-lookup"><span data-stu-id="4be33-132">It’s important to specify the color contexts, so an application that decodes the image at a later time can convert from the source color profile to the destination profile of the device being used to display or print the image.</span></span> <span data-ttu-id="4be33-133">如果沒有色彩設定檔，就無法在不同的裝置上取得一致的色彩。</span><span class="sxs-lookup"><span data-stu-id="4be33-133">Without a color profile, it is not possible to get consistent colors across different devices.</span></span> <span data-ttu-id="4be33-134">當使用者的相片在不同的監視器上看起來不同時，這可能會讓使用者感到沮喪，而且他們無法取得列印來比對畫面上顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="4be33-134">This can be frustrating for end users when their photos look different on different monitors, and they can’t get the prints to match what they see on screen.</span></span>

### <a name="getmetadataquerywriter"></a><span data-ttu-id="4be33-135">GetMetadataQueryWriter</span><span class="sxs-lookup"><span data-stu-id="4be33-135">GetMetadataQueryWriter</span></span>

<span data-ttu-id="4be33-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 會傳回 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) ，讓應用程式用來在影像框架的中繼資料區塊中插入或編輯特定的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="4be33-136">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) returns an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) that an application can use to insert or edit specific metadata properties in a metadata block on the image frame.</span></span>

<span data-ttu-id="4be33-137">您可以透過數種方式從 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)具現化 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 。</span><span class="sxs-lookup"><span data-stu-id="4be33-137">You can instantiate an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) from the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in several ways.</span></span> <span data-ttu-id="4be33-138">您可以從 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)建立它，就像 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)是從 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)介面上 [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)方法中的 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)建立的相同方式。</span><span class="sxs-lookup"><span data-stu-id="4be33-138">You can either create it from your [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), the same way [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) was created from an [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) in the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) method on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interface.</span></span>


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



<span data-ttu-id="4be33-139">您也可以從現有的 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)建立它，例如使用先前的方法所取得的。</span><span class="sxs-lookup"><span data-stu-id="4be33-139">You can also create it from an existing [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), such as the one obtained using the previous method.</span></span>


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



<span data-ttu-id="4be33-140">*PguidVendor* 參數可讓您指定查詢寫入器在具現化中繼資料寫入器時所要使用的特定廠商。</span><span class="sxs-lookup"><span data-stu-id="4be33-140">The *pguidVendor* parameter allows you to specify a particular vendor for the query writer to use when instantiating a metadata writer.</span></span> <span data-ttu-id="4be33-141">例如，如果您提供自己的中繼資料寫入器，您可能會想要指定自己的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="4be33-141">For example, if you provide your own metadata writers, you may want to specify your own vendor GUID.</span></span> <span data-ttu-id="4be33-142">如果您沒有喜好設定，則可以將 **Null** 傳遞給這個參數。</span><span class="sxs-lookup"><span data-stu-id="4be33-142">You can pass **NULL** to this parameter if you don’t have a preference.</span></span>

### <a name="setthumbnail"></a><span data-ttu-id="4be33-143">SetThumbnail</span><span class="sxs-lookup"><span data-stu-id="4be33-143">SetThumbnail</span></span>

<span data-ttu-id="4be33-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) 可用來提供縮圖。</span><span class="sxs-lookup"><span data-stu-id="4be33-144">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is used to provide a thumbnail.</span></span> <span data-ttu-id="4be33-145">所有影像都應該在全域、每個畫面上或兩者提供縮圖。</span><span class="sxs-lookup"><span data-stu-id="4be33-145">All images should provide a thumbnail either globally, on each frame, or both.</span></span> <span data-ttu-id="4be33-146">**GetThumbnail** 和 **SetThumbnail** 方法在容器層級是選擇性的，但如果編解碼器 \_ \_ 從 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)方法傳回 WINCODEC ERR CODECNOTHUMBNAIL，Windows 影像處理元件 (WIC) 將會叫用框架0的 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)方法。</span><span class="sxs-lookup"><span data-stu-id="4be33-146">The **GetThumbnail** and **SetThumbnail** methods are optional at the container-level but, if a codec returns WINCODEC\_ERR\_CODECNOTHUMBNAIL from the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method, Windows Imaging Component (WIC) will invoke the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method for Frame 0.</span></span> <span data-ttu-id="4be33-147">如果在任何地方都找不到縮圖，WIC 必須將完整的影像解碼，並將其調整為縮圖大小，這可能會對較大的影像產生較大的效能影響。</span><span class="sxs-lookup"><span data-stu-id="4be33-147">If no thumbnail is found in either place, WIC must decode the full image and scale it to thumbnail size, which could incur a large performance penalty for larger images.</span></span>

<span data-ttu-id="4be33-148">縮圖的大小和解析度應可讓您快速解碼和顯示。</span><span class="sxs-lookup"><span data-stu-id="4be33-148">The thumbnail should be of a size and resolution that makes it quick to decode and display.</span></span> <span data-ttu-id="4be33-149">基於這個理由，縮圖是最常見的 JPEG 影像。</span><span class="sxs-lookup"><span data-stu-id="4be33-149">For this reason, thumbnails are most commonly JPEG images.</span></span> <span data-ttu-id="4be33-150">請注意，如果您將 JPEG 用於縮圖，就不需要撰寫 JPEG 編碼程式來將其編碼，或使用 JPEG 解碼來將其解碼。</span><span class="sxs-lookup"><span data-stu-id="4be33-150">Note that, if you use JPEG for your thumbnails, you don’t have to write a JPEG encoder to encode them, or a JPEG decoder to decode them.</span></span> <span data-ttu-id="4be33-151">您應一律委派給 WIC 平臺隨附的 JPEG 編解碼器，以便編碼和解碼縮圖。</span><span class="sxs-lookup"><span data-stu-id="4be33-151">You should always delegate to the JPEG codec that ships with the WIC platform for encoding and decoding thumbnails.</span></span>

### <a name="writepixels"></a><span data-ttu-id="4be33-152">WritePixels</span><span class="sxs-lookup"><span data-stu-id="4be33-152">WritePixels</span></span>

<span data-ttu-id="4be33-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) 是一種方法，用來從記憶體中的點陣圖傳入掃描行以進行編碼。</span><span class="sxs-lookup"><span data-stu-id="4be33-153">[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) is the method used to pass in scan lines from a bitmap in memory for encoding.</span></span> <span data-ttu-id="4be33-154">方法會重複呼叫，直到傳入所有掃描行為止。</span><span class="sxs-lookup"><span data-stu-id="4be33-154">The method will be called repeatedly until all of the scan lines have been passed in.</span></span> <span data-ttu-id="4be33-155">*LineCount* 參數會指出要在此呼叫中寫入多少掃描行。</span><span class="sxs-lookup"><span data-stu-id="4be33-155">The *lineCount* parameter indicates how many scan lines are to be written in this call.</span></span> <span data-ttu-id="4be33-156">*CbStride* 參數會指出每個掃描行的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4be33-156">The *cbStride* parameter indicates the number of bytes per scan line.</span></span> <span data-ttu-id="4be33-157">*cbBufferSize* 指出 pbPixels 參數中所傳遞的緩衝區大小，其中包含要編碼的實際影像位。</span><span class="sxs-lookup"><span data-stu-id="4be33-157">*cbBufferSize* indicates the size of the buffer passed in the pbPixels parameter, which contains the actual image bits to be encoded.</span></span> <span data-ttu-id="4be33-158">如果累計呼叫中掃描行的總高度大於 [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) 方法中指定的高度，則傳回 WINCODEC \_ ERR \_ TOOMANYSCANLINES。</span><span class="sxs-lookup"><span data-stu-id="4be33-158">If the combined height of the scan lines from cumulative calls is greater than the height specified in [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="4be33-159">當 [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) 是 **WICBitmapEncoderCacheInMemory** 時，掃描行應該在記憶體中快取，直到傳入所有掃描行為止。</span><span class="sxs-lookup"><span data-stu-id="4be33-159">When the [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) is **WICBitmapEncoderCacheInMemory**, the scan lines should be cached in memory until all scan lines have been passed in.</span></span> <span data-ttu-id="4be33-160">如果編碼器快取選項是 **WICBitmapEncoderCacheTempFile**，則應該將掃描行快取在初始化物件時所建立的暫存檔案中。</span><span class="sxs-lookup"><span data-stu-id="4be33-160">If the encoder cache option is **WICBitmapEncoderCacheTempFile**, the scan lines should be cached in a temporary file, created when initializing the object.</span></span> <span data-ttu-id="4be33-161">在上述任一情況下，除非呼叫者呼叫 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit)，否則不應將映射編碼。</span><span class="sxs-lookup"><span data-stu-id="4be33-161">In either of these cases, the image should not be encoded until the caller calls [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).</span></span> <span data-ttu-id="4be33-162">在 **WICBitmapEncoderNoCache** 快取選項的情況下，編碼器應該盡可能編碼收到的掃描行。</span><span class="sxs-lookup"><span data-stu-id="4be33-162">In the case where the cache option is **WICBitmapEncoderNoCache**, the encoder should encode the scan lines as they’re received, if possible.</span></span> <span data-ttu-id="4be33-163"> (在某些格式中，這是不可能的，而且必須在呼叫 Commit 之前快取掃描行。 ) </span><span class="sxs-lookup"><span data-stu-id="4be33-163">(In some formats, this is not possible, and the scan lines must be cached until Commit is called.)</span></span>

<span data-ttu-id="4be33-164">大部分的原始編解碼器都不會執行 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)，因為它們不支援改變原始檔案中的影像位。</span><span class="sxs-lookup"><span data-stu-id="4be33-164">Most raw codecs will not implement [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), because they don’t support altering the image bits in the raw file.</span></span> <span data-ttu-id="4be33-165">不過，原始編解碼器仍應採用 **WritePixels**，因為新增中繼資料時，可能會增加檔案的大小，需要在磁片上重寫檔案。</span><span class="sxs-lookup"><span data-stu-id="4be33-165">Raw codecs should still implement **WritePixels**, however, because when metadata is added, it may increase the size of the file, requiring the file to be rewritten on the disk.</span></span> <span data-ttu-id="4be33-166">在這種情況下，您必須能夠複製現有的映射位，也就是 **WritePixels** 方法的用途。</span><span class="sxs-lookup"><span data-stu-id="4be33-166">In that case, it’s necessary to be able to copy the existing image bits, which is what the **WritePixels** method does.</span></span>

### <a name="writesource"></a><span data-ttu-id="4be33-167">WriteSource</span><span class="sxs-lookup"><span data-stu-id="4be33-167">WriteSource</span></span>

<span data-ttu-id="4be33-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) 用來編碼 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 物件。</span><span class="sxs-lookup"><span data-stu-id="4be33-168">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) is used to encode an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span> <span data-ttu-id="4be33-169">第一個參數是 **IWICBitmapSource** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4be33-169">The first parameter is a pointer to an **IWICBitmapSource** object.</span></span> <span data-ttu-id="4be33-170">第二個參數是指定要編碼之區域的 WICRect。</span><span class="sxs-lookup"><span data-stu-id="4be33-170">The second parameter is a WICRect that specifies the region of interest to encode.</span></span> <span data-ttu-id="4be33-171">只要每個矩形的寬度與要編碼的最終影像寬度相同，就可以連續多次呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4be33-171">This method may be called multiple times in succession, as long as the width of each rectangle is the same width of the final image to be encoded.</span></span> <span data-ttu-id="4be33-172">如果以 prc 參數傳遞的矩形寬度與 SetSize 方法中指定的寬度不同，則會傳回 WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS。</span><span class="sxs-lookup"><span data-stu-id="4be33-172">If the width of the rectangle passed in the prc parameter is different than the width specified in the SetSize method, return WINCODEC\_ERR\_SOURCERECTDOESNOTMATCHDIMENSIONS.</span></span> <span data-ttu-id="4be33-173">如果累計呼叫中掃描行的總高度大於 SetSize 方法中指定的高度，則傳回 WINCODEC \_ ERR \_ TOOMANYSCANLINES。</span><span class="sxs-lookup"><span data-stu-id="4be33-173">If the combined height of the scan lines from cumulative calls is greater than the height specified in SetSize method, return WINCODEC\_ERR\_TOOMANYSCANLINES.</span></span>

<span data-ttu-id="4be33-174">使用先前所述的 [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) 方法，快取選項的運作方式與此方法相同。</span><span class="sxs-lookup"><span data-stu-id="4be33-174">The cache options work the same way with this method as with the [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) method described previously.</span></span>

### <a name="commit"></a><span data-ttu-id="4be33-175">Commit</span><span class="sxs-lookup"><span data-stu-id="4be33-175">Commit</span></span>

<span data-ttu-id="4be33-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 是將編碼的影像位序列化為檔案資料流程的方法，並逐一查看框架的所有中繼資料寫入器，要求他們將其中繼資料序列化為數據流。</span><span class="sxs-lookup"><span data-stu-id="4be33-176">[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) is the method that serializes the encoded image bits to the file stream, and iterates through all the metadata writers for the frame requesting them to serialize their metadata to the stream.</span></span> <span data-ttu-id="4be33-177">在編碼器快取選項為 WICBitmapEncoderCacheInMemory 或 WICBitmapEncoderCacheTempFile 的情況下，此方法也會負責編碼影像，而且當快取選項為 WICBitmapEncoderCacheTempFile 時， **Commit** 方法也應該在編碼之前，先刪除用來快取影像資料的暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="4be33-177">In the case where the encoder cache option is WICBitmapEncoderCacheInMemory or WICBitmapEncoderCacheTempFile, this method is also responsible for encoding the image, and when the cache option is WICBitmapEncoderCacheTempFile, the **Commit** method should also delete the temporary file used to cache the image data before encoding.</span></span>

<span data-ttu-id="4be33-178">當所有組成影像的掃描行或矩形都已使用 [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) 或 [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) 方法傳入時，一律會叫用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4be33-178">This method is always invoked after all the scan lines or rectangles that make up the image have been passed in using either the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) or [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span> <span data-ttu-id="4be33-179">透過 WritePixels 或 WriteSource 的累積呼叫所組成的最後矩形大小，必須和 SetSize 方法中指定的大小相同。</span><span class="sxs-lookup"><span data-stu-id="4be33-179">The size of the final rectangle that is composed through the accumulated calls to WritePixels or WriteSource must be the same size as was specified in the SetSize method.</span></span> <span data-ttu-id="4be33-180">如果大小不符合預期的大小，這個方法應該會傳回 WINCODECERROR \_ UNEXPECTEDSIZE。</span><span class="sxs-lookup"><span data-stu-id="4be33-180">If the size does not match the expected size, this method should return WINCODECERROR\_UNEXPECTEDSIZE.</span></span>

<span data-ttu-id="4be33-181">若要逐一查看中繼資料寫入器，並告訴每個中繼資料寫入器將其中繼資料序列化，請移至資料流程、叫用 GetWriterByIndex 逐一查看每個區塊的寫入器，然後在每個中繼資料寫入器上叫用 IWICPersistStream。</span><span class="sxs-lookup"><span data-stu-id="4be33-181">To iterate through the metadata writers and tell each metadata writer to serialize its metadata go the stream, invoke GetWriterByIndex to iterate through the writers for each block, and invoke IWICPersistStream.Save on each metadata writer.</span></span>


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a><span data-ttu-id="4be33-182">SetPalette</span><span class="sxs-lookup"><span data-stu-id="4be33-182">SetPalette</span></span>

<span data-ttu-id="4be33-183">只有具有索引格式的編解碼器才需要執行 [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) 方法。</span><span class="sxs-lookup"><span data-stu-id="4be33-183">Only codecs that have indexed formats need to implement the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) method.</span></span> <span data-ttu-id="4be33-184">如果影像使用已編制索引的格式，請使用這個方法來指定影像中所使用之色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="4be33-184">If an image uses an indexed format, use this method to specify the palette of colors used in the image.</span></span> <span data-ttu-id="4be33-185">如果您的編解碼器沒有已編制索引的格式，請 \_ \_ 從這個方法傳回 WINCODEC ERR PALETTEUNAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="4be33-185">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE from this method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4be33-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="4be33-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4be33-187">**概念**</span><span class="sxs-lookup"><span data-stu-id="4be33-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4be33-188">執行 IWICBitmapCodecProgressNotification (編碼器) </span><span class="sxs-lookup"><span data-stu-id="4be33-188">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[<span data-ttu-id="4be33-189">執行 IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="4be33-189">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="4be33-190">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="4be33-190">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="4be33-191">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="4be33-191">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
