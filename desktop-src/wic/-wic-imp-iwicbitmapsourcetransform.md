---
description: 執行 IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: 執行 IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319851"
---
# <a name="implementing-iwicbitmapsourcetransform"></a><span data-ttu-id="bdf95-103">執行 IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="bdf95-103">Implementing IWICBitmapSourceTransform</span></span>

## <a name="iwicbitmapsourcetransform"></a><span data-ttu-id="bdf95-104">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="bdf95-104">IWICBitmapSourceTransform</span></span>

<span data-ttu-id="bdf95-105">雖然是選擇性的，但強烈建議每個解碼器在您的框架層級解碼類別上執行這個介面，因為它可以提供主要的效能優勢。</span><span class="sxs-lookup"><span data-stu-id="bdf95-105">Though optional, we highly recommend that every decoder implement this interface on your frame-level decoding class, because it can provide major performance benefits.</span></span> <span data-ttu-id="bdf95-106">當應用程式要求感興趣的特定區域、大小、方向或像素格式，而不是只在完整解析度解碼整個影像，然後套用要求的轉換時，Windows 影像處理元件 (WIC) 會針對 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)物件上的這個介面呼叫 [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="bdf95-106">When an application requests a specific region of interest, size, orientation, or pixel format, instead of just decoding the whole image at full resolution and then applying the requested transforms, Windows Imaging Component (WIC) calls [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for this interface on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span> <span data-ttu-id="bdf95-107">如果框架解碼支援它，WIC 會呼叫適當的方法或方法，以判斷畫面格解碼器是否可以執行要求的轉換，或決定可提供給所要求之的最接近大小或像素格式。</span><span class="sxs-lookup"><span data-stu-id="bdf95-107">If the frame decoder supports it, WIC calls the appropriate method or methods to determine whether the frame decoder can perform the requested transform or determine the closest size or pixel format the decoder can provide to the one requested.</span></span> <span data-ttu-id="bdf95-108">如果此解碼器可以執行要求的轉換或轉換，WIC 會使用適當的參數來叫用 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 。</span><span class="sxs-lookup"><span data-stu-id="bdf95-108">If the decoder can perform the requested transform or transforms, WIC invokes [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the appropriate parameters.</span></span> <span data-ttu-id="bdf95-109">如果此解碼器可以執行部分（但不是所有要求的轉換），WIC 會要求該解碼器執行其所能執行的轉換，並使用 WIC 轉換物件 ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)、 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)、 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)和 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) ，以執行在 **CopyPixels** 呼叫的結果上無法由框架解碼執行的其餘轉換。</span><span class="sxs-lookup"><span data-stu-id="bdf95-109">If the decoder can perform some, but not all of the requested transforms, WIC asks the decoder to perform those that it can, and uses the WIC transform objects ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) to perform the remaining transforms that could not be performed by the frame decoder on the result of the **CopyPixels** call.</span></span> <span data-ttu-id="bdf95-110">如果此解碼器不支援 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)，則 WIC 必須使用轉換物件來執行所有轉換。</span><span class="sxs-lookup"><span data-stu-id="bdf95-110">If the decoder doesn’t support [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), then WIC must use the transform objects to perform all of the transforms.</span></span> <span data-ttu-id="bdf95-111">比起將整個映射解碼，然後執行轉換，讓解碼器在解碼程式期間執行轉換，通常會更有效率。</span><span class="sxs-lookup"><span data-stu-id="bdf95-111">It’s usually much more efficient for the decoder to perform transforms during the decoding process than it is to decode the entire image and then perform the transforms.</span></span> <span data-ttu-id="bdf95-112">這特別適用于調整規模較小或像素格式轉換等作業。</span><span class="sxs-lookup"><span data-stu-id="bdf95-112">This is especially true for operations such as scaling to a much smaller size or pixel format conversions.</span></span>


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [<span data-ttu-id="bdf95-113">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="bdf95-113">DoesSupportTransform</span></span>](#doessupporttransform)
-   [<span data-ttu-id="bdf95-114">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="bdf95-114">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="bdf95-115">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="bdf95-115">GetClosestSize</span></span>](#getclosestsize)
-   [<span data-ttu-id="bdf95-116">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="bdf95-116">GetClosestPixelFormat</span></span>](#getclosestpixelformat)

### <a name="doessupporttransform"></a><span data-ttu-id="bdf95-117">DoesSupportTransform</span><span class="sxs-lookup"><span data-stu-id="bdf95-117">DoesSupportTransform</span></span>

<span data-ttu-id="bdf95-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) 會詢問此解碼器是否支援要求的旋轉或翻轉操作。</span><span class="sxs-lookup"><span data-stu-id="bdf95-118">[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) asks whether the decoder supports the requested rotation or flipping operation.</span></span> <span data-ttu-id="bdf95-119">可能要求的 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 為：</span><span class="sxs-lookup"><span data-stu-id="bdf95-119">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) that may be requested are:</span></span>


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a><span data-ttu-id="bdf95-120">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="bdf95-120">CopyPixels</span></span>

<span data-ttu-id="bdf95-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)會執行解碼影像位的實際工作（例如 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)介面上的 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)方法），但 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)上的 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)方法更強大，而且可以大幅改善影像處理效能。</span><span class="sxs-lookup"><span data-stu-id="bdf95-121">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) performs the actual work of decoding the image bits, such as the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) interface, but the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method on [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) is much more powerful, and can improve image processing performance significantly.</span></span>

<span data-ttu-id="bdf95-122">當要求多個轉換作業時，結果會取決於執行作業的順序。</span><span class="sxs-lookup"><span data-stu-id="bdf95-122">When multiple transform operations are requested, the result is dependent on the order in which the operations are performed.</span></span> <span data-ttu-id="bdf95-123">為了確保編解碼器之間的可預測性和一致性，所有編解碼器都必須以相同的循序執行這些作業。</span><span class="sxs-lookup"><span data-stu-id="bdf95-123">To ensure predictability and consistency across codecs, it’s important that all codecs perform these operations in the same order.</span></span> <span data-ttu-id="bdf95-124">這是執行這些作業的標準順序。</span><span class="sxs-lookup"><span data-stu-id="bdf95-124">This is the canonical order for performing these operations.</span></span>

1.  <span data-ttu-id="bdf95-125">調整</span><span class="sxs-lookup"><span data-stu-id="bdf95-125">Scale</span></span>
2.  <span data-ttu-id="bdf95-126">Crop</span><span class="sxs-lookup"><span data-stu-id="bdf95-126">Crop</span></span>
3.  <span data-ttu-id="bdf95-127">Rotate</span><span class="sxs-lookup"><span data-stu-id="bdf95-127">Rotate</span></span>

<span data-ttu-id="bdf95-128">您可以隨時執行像素格式轉換，因為它不會影響其他轉換。</span><span class="sxs-lookup"><span data-stu-id="bdf95-128">Pixel format conversion can be performed at any time, because it has no effect on the other transforms.</span></span>

<span data-ttu-id="bdf95-129">第一個參數（ *prcSrc*）是用來指定裁剪影像的相關區域。</span><span class="sxs-lookup"><span data-stu-id="bdf95-129">The first parameter, *prcSrc*, is used to specify the region of interest for clipping the image.</span></span> <span data-ttu-id="bdf95-130">由於調整是在依慣例裁剪之前執行，因此如果要縮放影像並進行裁剪，則應該在調整影像之後，判斷感興趣的區域。</span><span class="sxs-lookup"><span data-stu-id="bdf95-130">Because scaling is performed before clipping by convention, if the image is to be scaled as well as clipped, the region of interest should be determined after the image has been scaled.</span></span>

<span data-ttu-id="bdf95-131">第二個和第三個參數指出調整影像的大小。</span><span class="sxs-lookup"><span data-stu-id="bdf95-131">The second and third parameters indicate the size to which to scale the image.</span></span>

<span data-ttu-id="bdf95-132">*PguidDstFormat* 參數會指出已解碼影像所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="bdf95-132">The *pguidDstFormat* parameter indicates the requested pixel format for the decoded image.</span></span> <span data-ttu-id="bdf95-133">因為 WIC 已經呼叫 [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)，所以這應該是解碼器指出它所支援的像素格式。</span><span class="sxs-lookup"><span data-stu-id="bdf95-133">Because WIC has already called [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), this should be a pixel format that the decoder has indicated that it supports.</span></span>

<span data-ttu-id="bdf95-134">*DstTransform* 參數表示要求的旋轉角度，以及是否要垂直、水準或兩者翻轉影像。</span><span class="sxs-lookup"><span data-stu-id="bdf95-134">The *dstTransform* parameter indicates the requested rotation angle, and whether to flip the image vertically, horizontally, or both.</span></span> <span data-ttu-id="bdf95-135">同樣地，因為 WIC 已經呼叫 [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)，所以要求的轉換應該是該解碼器已指出它所支援的轉換。</span><span class="sxs-lookup"><span data-stu-id="bdf95-135">Again, because WIC will have already called [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), the requested transform should be one that the decoder has already indicated that it supports.</span></span> <span data-ttu-id="bdf95-136">請記住，在縮放和裁剪之後，應該一律執行旋轉。</span><span class="sxs-lookup"><span data-stu-id="bdf95-136">Remember that rotation should always be performed after scaling and clipping.</span></span>

### <a name="getclosestsize"></a><span data-ttu-id="bdf95-137">GetClosestSize</span><span class="sxs-lookup"><span data-stu-id="bdf95-137">GetClosestSize</span></span>

<span data-ttu-id="bdf95-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) 接受兩個 in/out 參數。</span><span class="sxs-lookup"><span data-stu-id="bdf95-138">[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) takes two in/out parameters.</span></span> <span data-ttu-id="bdf95-139">呼叫端會使用 *puiWidth* 和 *puiHeight* 參數來指定呼叫者偏好要解碼影像的大小。</span><span class="sxs-lookup"><span data-stu-id="bdf95-139">The caller uses the *puiWidth* and *puiHeight* parameters to specify the size at which that the caller prefers the image to be decoded.</span></span> <span data-ttu-id="bdf95-140">不過，解碼器只能將影像解碼為其 DCT 大小的倍數，且不同的影像格式可以有不同的 DCT 大小。</span><span class="sxs-lookup"><span data-stu-id="bdf95-140">However, a decoder can decode an image only to a size that’s a multiple of its DCT size, and different image formats can have different DCT sizes.</span></span> <span data-ttu-id="bdf95-141">此解碼器應該根據其本身的 DCT 大小來決定，最接近的是它可以進入所要求的大小，然後將 *puiWidth* 和 *puiHeight* 設定為傳回的維度。</span><span class="sxs-lookup"><span data-stu-id="bdf95-141">The decoder should determine, based on its own DCT size, the closest it can come to the requested size, and set the *puiWidth* and *puiHeight* to those dimensions on return.</span></span> <span data-ttu-id="bdf95-142">如果要求較大的大小，但編解碼器不支援消除倍增，則應該傳回原始。</span><span class="sxs-lookup"><span data-stu-id="bdf95-142">If a larger size is requested, but the codec doesn’t support upscaling, the original should be returned.</span></span>

### <a name="getclosestpixelformat"></a><span data-ttu-id="bdf95-143">GetClosestPixelFormat</span><span class="sxs-lookup"><span data-stu-id="bdf95-143">GetClosestPixelFormat</span></span>

<span data-ttu-id="bdf95-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) 可用來決定最接近所要求像素格式的像素格式，此格式可讓您在不遺失資料的情況下提供要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="bdf95-144">[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) is used to determine the closest pixel format to the requested pixel format that the decoder can provide without loss of data.</span></span> <span data-ttu-id="bdf95-145">最好的方式是轉換成較窄的像素格式，即使它會增加影像的大小，也是如此，因為它可以在必要時 reconverted 成更嚴格的格式。</span><span class="sxs-lookup"><span data-stu-id="bdf95-145">It’s always preferable to convert to a wider pixel format than a narrower one, even though it will increase the size of the image, because it can always be reconverted to a more restrictive format if necessary.</span></span> <span data-ttu-id="bdf95-146">不過，資料遺失之後，就無法復原。</span><span class="sxs-lookup"><span data-stu-id="bdf95-146">However, after the data is lost, it can’t be recovered.</span></span>

## <a name="continued-reading"></a><span data-ttu-id="bdf95-147">繼續閱讀</span><span class="sxs-lookup"><span data-stu-id="bdf95-147">Continued Reading</span></span>

<span data-ttu-id="bdf95-148">若要深入瞭解如何建立已啟用 WIC 的編解碼器，請參閱 [執行 IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)。</span><span class="sxs-lookup"><span data-stu-id="bdf95-148">To learn more about how to create a WIC-enabled codec, see [Implementing IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdf95-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdf95-149">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bdf95-150">**參考**</span><span class="sxs-lookup"><span data-stu-id="bdf95-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bdf95-151">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="bdf95-151">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[<span data-ttu-id="bdf95-152">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="bdf95-152">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="bdf95-153">**概念**</span><span class="sxs-lookup"><span data-stu-id="bdf95-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bdf95-154">執行 IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="bdf95-154">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="bdf95-155">執行 IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="bdf95-155">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="bdf95-156">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="bdf95-156">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="bdf95-157">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="bdf95-157">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
