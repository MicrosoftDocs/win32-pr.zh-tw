---
description: 功能完整性：建議的介面
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 功能完整性：建議的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989972"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="559ef-103">功能完整性：建議的介面</span><span class="sxs-lookup"><span data-stu-id="559ef-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="559ef-104">下表列出 Windows 影像處理元件原始編解碼器應執行的 (WIC) 介面。</span><span class="sxs-lookup"><span data-stu-id="559ef-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="559ef-105">介面</span><span class="sxs-lookup"><span data-stu-id="559ef-105">Interface</span></span></th>
<th><span data-ttu-id="559ef-106">必須用於</span><span class="sxs-lookup"><span data-stu-id="559ef-106">Required for</span></span></th>
<th><span data-ttu-id="559ef-107">Description</span><span class="sxs-lookup"><span data-stu-id="559ef-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="559ef-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="559ef-109">解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-109">Decoders</span></span></td>
<td><span data-ttu-id="559ef-110">表示解碼影像檔案的起點。</span><span class="sxs-lookup"><span data-stu-id="559ef-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="559ef-111">提供容器層級屬性的存取，例如縮圖、框架和調色板。</span><span class="sxs-lookup"><span data-stu-id="559ef-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="559ef-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="559ef-113">解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-113">Decoders</span></span></td>
<td><span data-ttu-id="559ef-114">代表容器內的特定影像框架，可提供框架層級屬性的存取權。</span><span class="sxs-lookup"><span data-stu-id="559ef-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="559ef-115">這是將實際影像位解碼的介面。</span><span class="sxs-lookup"><span data-stu-id="559ef-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="559ef-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="559ef-117">解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-117">Decoders</span></span></td>
<td><span data-ttu-id="559ef-118">從影像檔案讀取時，需要用來列舉中繼資料區塊，並叫用適當的中繼資料讀取器。</span><span class="sxs-lookup"><span data-stu-id="559ef-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="559ef-119">如果原始容器格式與 TIFF 相容，或使用標準 IFDs 或 IRBs 來儲存 EXIF 或 XMP 中繼資料，則編解碼器作者可以選擇叫用內建的中繼資料讀取器，而不是自行撰寫。</span><span class="sxs-lookup"><span data-stu-id="559ef-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="559ef-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="559ef-121">解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-121">Decoders</span></span></td>
<td><span data-ttu-id="559ef-122">允許呼叫者針對已解碼的影像指定所需的縮放、裁剪、旋轉或像素格式，以大幅提升效能。</span><span class="sxs-lookup"><span data-stu-id="559ef-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="559ef-123">例如，Microsoft 的 JPEG 和無線資料包協定 (WDP) 解碼器使用金字塔優化配置，可在目標點陣圖小於來源點陣圖時，更快速地進行解碼。</span><span class="sxs-lookup"><span data-stu-id="559ef-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="559ef-124">&quot; &quot; 當內嵌的預覽遺失或小於其最大維度的1024圖元時，Windows Vista (和更新版本的) 將會嘗試使用此介面從原始影像中解壓縮快速預覽。</span><span class="sxs-lookup"><span data-stu-id="559ef-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="559ef-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="559ef-126">解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-126">Decoders</span></span></td>
<td><span data-ttu-id="559ef-127">RAW 格式的必要參數。</span><span class="sxs-lookup"><span data-stu-id="559ef-127">Required for RAW formats.</span></span> <span data-ttu-id="559ef-128">公開原始影像處理特有的參數。</span><span class="sxs-lookup"><span data-stu-id="559ef-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="559ef-129">原始編解碼器應該支援將這些參數視為套用至編解碼器的許多參數。</span><span class="sxs-lookup"><span data-stu-id="559ef-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="559ef-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="559ef-131">編碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-131">Encoders</span></span></td>
<td><span data-ttu-id="559ef-132">代表編碼影像檔案的起點。</span><span class="sxs-lookup"><span data-stu-id="559ef-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="559ef-133">此介面是用來設定容器層級的屬性，例如縮圖、框架和調色板。</span><span class="sxs-lookup"><span data-stu-id="559ef-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="559ef-134">您也必須叫用中繼資料寫入器，以啟用影像檔的中繼資料持續性。</span><span class="sxs-lookup"><span data-stu-id="559ef-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="559ef-135">基於這些原因，即使不支援將主要點陣圖編碼為原始格式，也需要這個介面。</span><span class="sxs-lookup"><span data-stu-id="559ef-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="559ef-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="559ef-137">編碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-137">Encoders</span></span></td>
<td><span data-ttu-id="559ef-138">代表容器內的特定映射框架。</span><span class="sxs-lookup"><span data-stu-id="559ef-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="559ef-139">此介面是用來將實際的影像位編碼，並設定每個畫面格的中繼資料和屬性。</span><span class="sxs-lookup"><span data-stu-id="559ef-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="559ef-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="559ef-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="559ef-141">編碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-141">Encoders</span></span></td>
<td><span data-ttu-id="559ef-142">當序列化影像檔案時，需要用來逐一查看中繼資料區塊，並叫用適當的中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="559ef-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="559ef-143">如果原始的容器格式與 TIFF 相容，編解碼器作者可以選擇叫用內建的中繼資料寫入器，而不是自行撰寫。</span><span class="sxs-lookup"><span data-stu-id="559ef-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="559ef-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="559ef-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="559ef-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="559ef-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="559ef-146">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="559ef-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="559ef-147">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="559ef-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="559ef-148">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="559ef-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




