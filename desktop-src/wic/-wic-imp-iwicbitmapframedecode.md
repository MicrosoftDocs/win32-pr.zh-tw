---
description: 執行 IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: 執行 IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694176"
---
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="ff270-103">執行 IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="ff270-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="ff270-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="ff270-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="ff270-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 是提供實際影像位存取權的框架層級介面。</span><span class="sxs-lookup"><span data-stu-id="ff270-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="ff270-106">您可以在框架層級的解碼類別上執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="ff270-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="ff270-107">因為它衍生自 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)，所以您的 **IWICBitmapFrameDecode** 執行將包含 **IWICBitmapSource** 方法的執行。</span><span class="sxs-lookup"><span data-stu-id="ff270-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="ff270-108">**IWICBitmapFrameDecode** 上的其他方法可讓您存取框架層級的縮圖、影像的任何色彩內容，以及框架的中繼資料查詢讀取器。</span><span class="sxs-lookup"><span data-stu-id="ff270-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [<span data-ttu-id="ff270-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ff270-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="ff270-110">GetColorCoNtexts</span><span class="sxs-lookup"><span data-stu-id="ff270-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="ff270-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="ff270-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="ff270-112">GetSize、GetPixelFormat 和 GetResolution</span><span class="sxs-lookup"><span data-stu-id="ff270-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="ff270-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="ff270-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="ff270-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="ff270-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="ff270-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="ff270-115">GetThumbnail</span></span>

<span data-ttu-id="ff270-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) 會傳回目前畫面格的縮圖。</span><span class="sxs-lookup"><span data-stu-id="ff270-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="ff270-117">基於效能考慮，縮圖最常以 JPEG 格式編碼。</span><span class="sxs-lookup"><span data-stu-id="ff270-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="ff270-118">就像在解碼器上的預覽一樣，您不需要或建議您為縮圖提供自己的 JPEG 解碼器。</span><span class="sxs-lookup"><span data-stu-id="ff270-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="ff270-119">相反地，您應該委派給 Windows 影像處理元件 (WIC) 所提供的 JPEG 解碼器。</span><span class="sxs-lookup"><span data-stu-id="ff270-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="ff270-120">如需縮圖的詳細資訊，請參閱[執行 IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)的[SetThumbnail](-wic-imp-iwicbitmapframeencode.md)方法。</span><span class="sxs-lookup"><span data-stu-id="ff270-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="ff270-121">GetColorCoNtexts</span><span class="sxs-lookup"><span data-stu-id="ff270-121">GetColorContexts</span></span>

<span data-ttu-id="ff270-122">[**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) 會傳回有效的色彩內容 (也稱為色彩設定檔) 與此框架中的影像相關聯。</span><span class="sxs-lookup"><span data-stu-id="ff270-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="ff270-123">在大部分的情況下，這只是其中一種，但可能會有兩個或更少的情況。</span><span class="sxs-lookup"><span data-stu-id="ff270-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="ff270-124">呼叫端會傳入一或多個 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 物件，並將 *帳戶 c)* 參數設定為指出傳入的數目。</span><span class="sxs-lookup"><span data-stu-id="ff270-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="ff270-125">這個方法會在 **IWICColorCoNtext** 物件中填入與影像相關聯之色彩設定檔的實際色彩內容資料。</span><span class="sxs-lookup"><span data-stu-id="ff270-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="ff270-126">將 *pcActualCount* 參數設定為與影像相關聯的實際色彩內容數目，即使該值大於您可以傳回的數目。</span><span class="sxs-lookup"><span data-stu-id="ff270-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="ff270-127"> (如果有更多的色彩內容可供呼叫端傳入的 **IWICColorCoNtext** 物件數目使用，這會告知呼叫者有一或多個其他可用的物件。 ) </span><span class="sxs-lookup"><span data-stu-id="ff270-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="ff270-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="ff270-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="ff270-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) 會傳回 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ，讓應用程式用來從影像框架取出中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ff270-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="ff270-130">這個介面是由元資料處理程式所執行，並可讓應用程式查詢屬於特定元資料格式的特定中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="ff270-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="ff270-131">如需詳細資訊，請參閱 [執行 IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)。</span><span class="sxs-lookup"><span data-stu-id="ff270-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="ff270-132">若要具現化 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)，請在 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)上呼叫 [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) 。</span><span class="sxs-lookup"><span data-stu-id="ff270-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="ff270-133">GetSize、GetPixelFormat 和 GetResolution</span><span class="sxs-lookup"><span data-stu-id="ff270-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="ff270-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)、 [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)和 [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) 是一目了然的，並會傳回所要求的影像屬性。</span><span class="sxs-lookup"><span data-stu-id="ff270-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="ff270-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="ff270-135">CopyPixels</span></span>

<span data-ttu-id="ff270-136">當應用程式想要在記憶體中建立可轉譯成顯示或印表機的點陣圖時， [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)是應用程式所呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="ff270-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="ff270-137">這是執行影像位實際解碼的方法。</span><span class="sxs-lookup"><span data-stu-id="ff270-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="ff270-138">這些參數是一個矩形，代表要複製到記憶體的來源影像中的相關區域;跨距，指定一個掃描行中的位元組數目;應用程式已配置之記憶體中的緩衝區大小;以及要將要求的影像位複製到其中的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="ff270-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="ff270-139"> (若要防止潛在的緩衝區溢位產生安全性弱點，請務必將最多的影像資料複製到緩衝區中，因為 *cbBufferSize* 參數指定。 ) </span><span class="sxs-lookup"><span data-stu-id="ff270-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="ff270-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="ff270-140">CopyPalette</span></span>

<span data-ttu-id="ff270-141">只有具有索引像素格式的編解碼器必須執行 [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff270-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="ff270-142">如果影像使用已編制索引的格式，請使用這個方法來傳回影像中所使用之色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="ff270-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="ff270-143">如果您的編解碼器沒有已編制索引的格式，則傳回 WINCODEC \_ ERR \_ PALETTEUNAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="ff270-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff270-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff270-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff270-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="ff270-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff270-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="ff270-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="ff270-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="ff270-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="ff270-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="ff270-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="ff270-149">**概念**</span><span class="sxs-lookup"><span data-stu-id="ff270-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff270-150">執行 IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="ff270-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="ff270-151">執行 IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="ff270-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="ff270-152">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ff270-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ff270-153">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ff270-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



