---
description: Windows 7 的原始編解碼器需求
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Windows 7 的原始編解碼器需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980376"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="dacb7-103">Windows 7 的原始編解碼器需求</span><span class="sxs-lookup"><span data-stu-id="dacb7-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="dacb7-104">至少需要下列編解碼器功能：</span><span class="sxs-lookup"><span data-stu-id="dacb7-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="dacb7-105">Windows Vista shell 和影像中心支援所需的所有功能：縮圖、預覽和 (保存) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="dacb7-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="dacb7-106">原始處理應該預設為適當的進行中設定。</span><span class="sxs-lookup"><span data-stu-id="dacb7-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="dacb7-107">支援核心中繼資料 (讀取和寫入) 、非 EXIF 中繼資料以及 EXIF 中繼資料）都必須保存在未經處理的檔案格式中，而不需要使用側車檔。</span><span class="sxs-lookup"><span data-stu-id="dacb7-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="dacb7-108">[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)介面的支援。</span><span class="sxs-lookup"><span data-stu-id="dacb7-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="dacb7-109">在 Windows 7 中，Windows 影像處理元件 (WIC) WIC 需要實 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 所公開的所有參數介面。</span><span class="sxs-lookup"><span data-stu-id="dacb7-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="dacb7-110">方向狀態支援：</span><span class="sxs-lookup"><span data-stu-id="dacb7-110">Orientation state support:</span></span>

-   <span data-ttu-id="dacb7-111">應使用 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) 方法來套用90度階的影像旋轉。</span><span class="sxs-lookup"><span data-stu-id="dacb7-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="dacb7-112">應用程式和 Windows 會使用這個方法，將影像 (和快取的縮圖和預覽) 旋轉。</span><span class="sxs-lookup"><span data-stu-id="dacb7-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="dacb7-113">使用此 API 的旋轉應用程式也應該由編解碼器保存 (請參閱本檔中稍早的) 。</span><span class="sxs-lookup"><span data-stu-id="dacb7-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="dacb7-114">應用程式可以使用 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API 的旋轉功能，但編解碼器不會序列化此 api 上的任何旋轉設定，因此使用 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) 完成的旋轉將不會保存。</span><span class="sxs-lookup"><span data-stu-id="dacb7-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="dacb7-115">高速縮圖和預覽解壓縮支援。</span><span class="sxs-lookup"><span data-stu-id="dacb7-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="dacb7-116">如果最大的圖元尺寸 (寬度或高度) 小於1024圖元，Windows Vista 將會要求螢幕預覽的呈現：</span><span class="sxs-lookup"><span data-stu-id="dacb7-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="dacb7-117">[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)：：[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)方法應該至少支援 [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)和 [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode)模式，以允許更快速地轉譯縮圖和預覽，而非全品質模式。</span><span class="sxs-lookup"><span data-stu-id="dacb7-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="dacb7-118">Windows 會使用要求的螢幕解析度大小來呼叫 [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)：：[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 。</span><span class="sxs-lookup"><span data-stu-id="dacb7-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="dacb7-119">上述 API 必須支援螢幕解析度大小。</span><span class="sxs-lookup"><span data-stu-id="dacb7-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="dacb7-120">需要 [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) 縮圖、預覽和全映射位的一致性影像處理。</span><span class="sxs-lookup"><span data-stu-id="dacb7-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="dacb7-121">高動態範圍 (HDR) 像素格式。</span><span class="sxs-lookup"><span data-stu-id="dacb7-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="dacb7-122">XML 檔規格 (XPS) 列印。</span><span class="sxs-lookup"><span data-stu-id="dacb7-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dacb7-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="dacb7-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dacb7-124">**概念**</span><span class="sxs-lookup"><span data-stu-id="dacb7-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dacb7-125">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="dacb7-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="dacb7-126">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="dacb7-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="dacb7-127">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="dacb7-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



