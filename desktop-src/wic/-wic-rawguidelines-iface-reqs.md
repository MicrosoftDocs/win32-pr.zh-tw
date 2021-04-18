---
description: 介面方法需求
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: 介面方法需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978079"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="adc2a-103">介面方法需求</span><span class="sxs-lookup"><span data-stu-id="adc2a-103">Interface Method Requirements</span></span>

<span data-ttu-id="adc2a-104">並非每個介面上的每個方法都必須有執行。</span><span class="sxs-lookup"><span data-stu-id="adc2a-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="adc2a-105">例如，某些編解碼器具有全域中繼資料、縮圖或色彩內容，而其他編解碼器只會在每個畫面上提供這些編解碼器。</span><span class="sxs-lookup"><span data-stu-id="adc2a-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="adc2a-106">如果編解碼器作者只針對每個框架提供這些，則只需要執行 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)或 colorcoNtext，或在 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)上執行 [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)或 [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)方法，而不是在 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)和 [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)上。</span><span class="sxs-lookup"><span data-stu-id="adc2a-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="adc2a-107">同樣地，某些編解碼器不會使用索引格式，因此不需要執行 [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) 和 [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) 方法。</span><span class="sxs-lookup"><span data-stu-id="adc2a-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="adc2a-108">因此，這些方法都是選擇性的，並保留給編解碼器建立者的決定。</span><span class="sxs-lookup"><span data-stu-id="adc2a-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="adc2a-109">大部分其他的方法都是必要的。</span><span class="sxs-lookup"><span data-stu-id="adc2a-109">Most other methods are required.</span></span>

<span data-ttu-id="adc2a-110">針對 Windows 7 [**get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)和 [**get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)是必要的，而且必須在包含層級類別或框架層級類別上執行。</span><span class="sxs-lookup"><span data-stu-id="adc2a-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="adc2a-111">如果您的影像檔案格式不支援其中一個位置的預覽或縮圖，您應該修改影像檔案格式以提供這類支援。</span><span class="sxs-lookup"><span data-stu-id="adc2a-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="adc2a-112">當未執行方法時，請務必傳回適當的錯誤，讓呼叫端能夠判斷所要求的功能不受支援。</span><span class="sxs-lookup"><span data-stu-id="adc2a-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="adc2a-113">例如，如果編解碼器作者不支援容器層級縮圖，則當應用程式呼叫 [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)時，它們應該會傳回 [WINCODEC \_ ERR \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) ，如果它們沒有調色板，則應該傳回 [WINCODEC \_ err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="adc2a-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="adc2a-114">如果沒有適當的 [WINCODEC \_ 錯誤](-wic-codec-error-codes.md) 程式碼存在，則編解碼器應該會 \_ 針對未提供的方法傳回 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="adc2a-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="adc2a-115">下表列出每個 Windows 影像處理元件 (WIC) 介面的必要和選擇性方法。</span><span class="sxs-lookup"><span data-stu-id="adc2a-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="adc2a-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="adc2a-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="adc2a-117">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-117">Required</span></span>

[<span data-ttu-id="adc2a-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="adc2a-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="adc2a-119">**初始化**</span><span class="sxs-lookup"><span data-stu-id="adc2a-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="adc2a-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="adc2a-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="adc2a-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="adc2a-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="adc2a-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="adc2a-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="adc2a-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="adc2a-124">選擇性</span><span class="sxs-lookup"><span data-stu-id="adc2a-124">Optional</span></span>

<span data-ttu-id="adc2a-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="adc2a-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="adc2a-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="adc2a-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="adc2a-127">**GetColorCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="adc2a-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="adc2a-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="adc2a-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="adc2a-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="adc2a-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="adc2a-130">¹如果您的影像檔案格式支援容器層級預覽，則為必要。</span><span class="sxs-lookup"><span data-stu-id="adc2a-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="adc2a-131">如果不是這種情況，強烈建議您修改影像檔案格式以支援此功能。</span><span class="sxs-lookup"><span data-stu-id="adc2a-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="adc2a-132">如果在這裡執行，則容器層級編碼類別需要對應的 [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) 。</span><span class="sxs-lookup"><span data-stu-id="adc2a-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="adc2a-133">在這裡或在框架層級解碼類別上需要²，視您的圖像檔案格式儲存縮圖的位置而定。</span><span class="sxs-lookup"><span data-stu-id="adc2a-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="adc2a-134">如果在這裡執行，則容器層級編碼類別需要對應的 [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) 。</span><span class="sxs-lookup"><span data-stu-id="adc2a-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="adc2a-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="adc2a-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="adc2a-136">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-136">Required</span></span>

[<span data-ttu-id="adc2a-137">**GetColorCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="adc2a-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="adc2a-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="adc2a-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="adc2a-139">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="adc2a-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="adc2a-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="adc2a-141">**GetResolution**</span><span class="sxs-lookup"><span data-stu-id="adc2a-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="adc2a-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="adc2a-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="adc2a-143">選擇性</span><span class="sxs-lookup"><span data-stu-id="adc2a-143">Optional</span></span>

<span data-ttu-id="adc2a-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="adc2a-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="adc2a-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="adc2a-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="adc2a-146">¹需要或在容器層級的解碼類別上，視您的圖像檔案格式儲存縮圖的位置而定。</span><span class="sxs-lookup"><span data-stu-id="adc2a-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="adc2a-147">如果在這裡執行，則框架層級編碼器類別需要對應的 [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) 。</span><span class="sxs-lookup"><span data-stu-id="adc2a-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="adc2a-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="adc2a-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="adc2a-149">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-149">Required</span></span>

[<span data-ttu-id="adc2a-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="adc2a-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="adc2a-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="adc2a-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="adc2a-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="adc2a-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="adc2a-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="adc2a-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="adc2a-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="adc2a-155">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-155">Required</span></span>

[<span data-ttu-id="adc2a-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="adc2a-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="adc2a-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="adc2a-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="adc2a-158">選擇性</span><span class="sxs-lookup"><span data-stu-id="adc2a-158">Optional</span></span>

[<span data-ttu-id="adc2a-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="adc2a-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="adc2a-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="adc2a-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="adc2a-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="adc2a-162">請參閱本檔稍後 [的 IWICDevelopRaw 支援](./-wic-rawguidelines-iwicdevelopraw.md)。</span><span class="sxs-lookup"><span data-stu-id="adc2a-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="adc2a-163">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="adc2a-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="adc2a-164">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-164">Required</span></span>

[<span data-ttu-id="adc2a-165">**初始化**</span><span class="sxs-lookup"><span data-stu-id="adc2a-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="adc2a-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="adc2a-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="adc2a-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="adc2a-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="adc2a-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="adc2a-169">**Commit**</span><span class="sxs-lookup"><span data-stu-id="adc2a-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="adc2a-170">選擇性</span><span class="sxs-lookup"><span data-stu-id="adc2a-170">Optional</span></span>

<span data-ttu-id="adc2a-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="adc2a-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="adc2a-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="adc2a-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="adc2a-173">**SetColorCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="adc2a-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="adc2a-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="adc2a-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="adc2a-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="adc2a-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="adc2a-176">¹如果您的影像檔案格式支援框架層級預覽，則為必要。</span><span class="sxs-lookup"><span data-stu-id="adc2a-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="adc2a-177">在這裡或在框架層級編碼類別上需要²，視您的圖像檔案格式儲存縮圖的位置而定。</span><span class="sxs-lookup"><span data-stu-id="adc2a-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="adc2a-178">如果在這裡執行，則容器層級解碼類別上需要有對應的 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) 。</span><span class="sxs-lookup"><span data-stu-id="adc2a-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="adc2a-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="adc2a-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="adc2a-180">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-180">Required</span></span>

[<span data-ttu-id="adc2a-181">**初始化**</span><span class="sxs-lookup"><span data-stu-id="adc2a-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="adc2a-182">**SetColorCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="adc2a-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="adc2a-183">**SetColorCoNtexts**</span><span class="sxs-lookup"><span data-stu-id="adc2a-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="adc2a-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="adc2a-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="adc2a-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="adc2a-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="adc2a-186">**SetResolution**</span><span class="sxs-lookup"><span data-stu-id="adc2a-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="adc2a-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="adc2a-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="adc2a-188">**WriteSource**</span><span class="sxs-lookup"><span data-stu-id="adc2a-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="adc2a-189">**Commit**</span><span class="sxs-lookup"><span data-stu-id="adc2a-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="adc2a-190">選擇性</span><span class="sxs-lookup"><span data-stu-id="adc2a-190">Optional</span></span>

<span data-ttu-id="adc2a-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="adc2a-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="adc2a-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="adc2a-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="adc2a-193">¹必須在這裡或在容器層級編碼類別上，視您的圖像檔案格式儲存縮圖的位置而定。</span><span class="sxs-lookup"><span data-stu-id="adc2a-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="adc2a-194">如果在這裡執行，則在框架層級解碼類別上需要對應的 [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) 。</span><span class="sxs-lookup"><span data-stu-id="adc2a-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="adc2a-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="adc2a-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="adc2a-196">必要</span><span class="sxs-lookup"><span data-stu-id="adc2a-196">Required</span></span>

[<span data-ttu-id="adc2a-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="adc2a-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="adc2a-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="adc2a-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="adc2a-199">**GetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="adc2a-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="adc2a-200">**SetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="adc2a-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="adc2a-201">**RemoveWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="adc2a-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="adc2a-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="adc2a-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="adc2a-203">**概念**</span><span class="sxs-lookup"><span data-stu-id="adc2a-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="adc2a-204">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="adc2a-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="adc2a-205">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="adc2a-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="adc2a-206">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="adc2a-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
