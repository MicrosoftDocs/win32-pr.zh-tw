---
description: 中繼資料支援
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: 中繼資料支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988341"
---
# <a name="metadata-support"></a><span data-ttu-id="56015-103">中繼資料支援</span><span class="sxs-lookup"><span data-stu-id="56015-103">Metadata Support</span></span>

<span data-ttu-id="56015-104">未經處理的格式也應該支援 Windows 中映射的一般中繼資料讀取和寫入案例。</span><span class="sxs-lookup"><span data-stu-id="56015-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="56015-105">Microsoft 開發了一組原生中繼資料提供者來交換影像檔案 (的 EXIF) 、國際新聞電訊委員會 (IPTC) ，以及可延伸的中繼資料平臺 (目前僅針對 TIFF 和 JPEG 容器叫用的 XMP) 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="56015-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="56015-106">如果原始影像儲存為這些容器格式的其中一種，建議使用 Windows 內建的中繼資料提供者。</span><span class="sxs-lookup"><span data-stu-id="56015-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="56015-107">不過，編解碼器作者必須負責正確設定。</span><span class="sxs-lookup"><span data-stu-id="56015-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="56015-108">對於不是以 TIFF 容器為基礎的原始檔案，可能需要執行 EXIF、IPTC 或 XMP 寫入器，因為內建的讀取器和寫入器預期資料必須符合 EXIF、IPTC 和 XMP 磁片配置規格。</span><span class="sxs-lookup"><span data-stu-id="56015-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="56015-109">編解碼器作者也可以針對任何自訂中繼資料來執行自己的提供者。</span><span class="sxs-lookup"><span data-stu-id="56015-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="56015-110">因為 Windows 影像處理元件 (WIC) 的架構，所以只能透過影像編碼器的實例叫用中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="56015-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="56015-111">因此，原始格式的擁有者應建立至少一個 "stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) 編碼器，即使實際的圖元編碼為未經處理的格式也不會執行。</span><span class="sxs-lookup"><span data-stu-id="56015-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="56015-112">編解碼器作者必須叫用正確的元資料處理程式：</span><span class="sxs-lookup"><span data-stu-id="56015-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="56015-113">視需要在解碼器和框架解碼器上 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 。</span><span class="sxs-lookup"><span data-stu-id="56015-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="56015-114">視需要在編碼器和框架編碼器上 [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) 。</span><span class="sxs-lookup"><span data-stu-id="56015-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="56015-115">若要在 Windows Vista 中支援映射處理應用程式中的所有預期案例，建議使用編解碼器廠商至少支援下列各項：</span><span class="sxs-lookup"><span data-stu-id="56015-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="56015-116">EXIF 讀取</span><span class="sxs-lookup"><span data-stu-id="56015-116">EXIF read</span></span>
-   <span data-ttu-id="56015-117">部分 EXIF 寫入 (，以允許更新來捕捉日期和時間) </span><span class="sxs-lookup"><span data-stu-id="56015-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="56015-118">XMP 讀取和寫入 (包括適用于 XMP 的選擇性 IPTC 核心) </span><span class="sxs-lookup"><span data-stu-id="56015-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="56015-119">IPTC IIMv4 讀取和寫入</span><span class="sxs-lookup"><span data-stu-id="56015-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="56015-120">大部分的中繼資料存取 (Windows Vista 中的讀取和寫入) 都會透過 [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) 或 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) 介面進行。</span><span class="sxs-lookup"><span data-stu-id="56015-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="56015-121">因此，若要參與 Windows Vista 中繼資料的體驗，原始編解碼器作者必須執行 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)：：[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) 和 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)：：[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) 方法。</span><span class="sxs-lookup"><span data-stu-id="56015-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56015-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="56015-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="56015-123">**概念**</span><span class="sxs-lookup"><span data-stu-id="56015-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="56015-124">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="56015-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="56015-125">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="56015-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="56015-126">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="56015-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



