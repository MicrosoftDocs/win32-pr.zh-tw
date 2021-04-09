---
description: 本主題將為開發人員提供有關如何執行可在 Windows 影像處理元件 (WIC) framework 中運作之圖像檔案格式編解碼器的指引。
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: 如何撰寫 WIC-Enabled 編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849507"
---
# <a name="how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="7bc34-103">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="7bc34-103">How to Write a WIC-Enabled Codec</span></span>

<span data-ttu-id="7bc34-104">本主題將為開發人員提供有關如何執行可在 Windows 影像處理元件 (WIC) framework 中運作之圖像檔案格式編解碼器的指引。</span><span class="sxs-lookup"><span data-stu-id="7bc34-104">This section of topics provide developers with guidance on how to implement image file format codecs that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="7bc34-105">簡介</span><span class="sxs-lookup"><span data-stu-id="7bc34-105">Introduction</span></span>](-wic-howtowriteacodec-intro.md)  
[<span data-ttu-id="7bc34-106">Windows 影像處理元件 (WIC) 的運作方式</span><span class="sxs-lookup"><span data-stu-id="7bc34-106">How The Windows Imaging Component (WIC) Works</span></span>](-wic-howwicworks.md)  
<dl>

[<span data-ttu-id="7bc34-107">探索和仲裁</span><span class="sxs-lookup"><span data-stu-id="7bc34-107">Discovery and Arbitration</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="7bc34-108">解碼</span><span class="sxs-lookup"><span data-stu-id="7bc34-108">Decoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="7bc34-109">編碼方式</span><span class="sxs-lookup"><span data-stu-id="7bc34-109">Encoding</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="7bc34-110">編解碼器的存留期</span><span class="sxs-lookup"><span data-stu-id="7bc34-110">The Lifetime of a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="7bc34-111">如何 WIC-啟用編解碼器</span><span class="sxs-lookup"><span data-stu-id="7bc34-111">How to WIC-enable a Codec</span></span>](-wic-howwicworks.md)  
[<span data-ttu-id="7bc34-112">WIC 中的多執行緒單元支援</span><span class="sxs-lookup"><span data-stu-id="7bc34-112">Multi-Threaded Apartment Support in WIC</span></span>](-wic-howwicworks.md)  
<span data-ttu-id="7bc34-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">執行 WIC-Enabled 的解碼器</a></span><span class="sxs-lookup"><span data-stu-id="7bc34-113"></dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementing a WIC-Enabled Decoder</a></span></span><dl>

[<span data-ttu-id="7bc34-114">解碼器介面</span><span class="sxs-lookup"><span data-stu-id="7bc34-114">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)<dl>

[<span data-ttu-id="7bc34-115">IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="7bc34-115">IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)  
[<span data-ttu-id="7bc34-116">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="7bc34-116">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[<span data-ttu-id="7bc34-117">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="7bc34-117">IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)  
[<span data-ttu-id="7bc34-118">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="7bc34-118">IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)  
[<span data-ttu-id="7bc34-119">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="7bc34-119">IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)  
[<span data-ttu-id="7bc34-120">IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="7bc34-120">IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)  
[<span data-ttu-id="7bc34-121">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="7bc34-121">IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)  
<span data-ttu-id="7bc34-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">執行 WIC-Enabled 編碼器</a>  
</span><span class="sxs-lookup"><span data-stu-id="7bc34-122"></dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementing a WIC-Enabled Encoder</a>  
</span></span><dl>

[<span data-ttu-id="7bc34-123">編碼器介面</span><span class="sxs-lookup"><span data-stu-id="7bc34-123">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)  
<dl>

[<span data-ttu-id="7bc34-124">IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="7bc34-124">IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)  
[<span data-ttu-id="7bc34-125">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="7bc34-125">IWICBitmapCodecProgressNotification</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[<span data-ttu-id="7bc34-126">IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="7bc34-126">IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)  
[<span data-ttu-id="7bc34-127">IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="7bc34-127">IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)  
<span data-ttu-id="7bc34-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">編解碼器安裝和註冊</a>  
</span><span class="sxs-lookup"><span data-stu-id="7bc34-128"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Codec Installation and Registration</a>  
</span></span><dl>

[<span data-ttu-id="7bc34-129">註冊編解碼器</span><span class="sxs-lookup"><span data-stu-id="7bc34-129">Registering a Codec</span></span>](-wic-codecinstallandreg.md)  
<dl>

[<span data-ttu-id="7bc34-130">一般註冊專案</span><span class="sxs-lookup"><span data-stu-id="7bc34-130">General Register Entries</span></span>](-wic-generalregentries.md)  
[<span data-ttu-id="7bc34-131">編碼器特定的登錄專案</span><span class="sxs-lookup"><span data-stu-id="7bc34-131">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)  
<dl>

[<span data-ttu-id="7bc34-132">使用中繼資料寫入器註冊容器格式</span><span class="sxs-lookup"><span data-stu-id="7bc34-132">Registering a Container Format with Metadata Writers</span></span>](-wic-encoderregentries.md)  
<span data-ttu-id="7bc34-133"></dl> </dd> <a href="-wic-decoderregentries.md">編碼器特定的登錄專案</a>  
</span><span class="sxs-lookup"><span data-stu-id="7bc34-133"></dl> </dd> <a href="-wic-decoderregentries.md">Encoder-Specific Registry Entries</a>  
</span></span><dl>

[<span data-ttu-id="7bc34-134">使用中繼資料讀取器註冊新的容器格式</span><span class="sxs-lookup"><span data-stu-id="7bc34-134">Registering a New Container Format with Metadata Readers</span></span>](-wic-decoderregentries.md)  
<span data-ttu-id="7bc34-135"></dl> </dd> <a href="-wic-integrationregentries.md">與 Windows Vista PhotoGallery 和 Explorer 整合</a>  
</span><span class="sxs-lookup"><span data-stu-id="7bc34-135"></dl> </dd> <a href="-wic-integrationregentries.md">Integration with Windows Vista PhotoGallery and Explorer</a>  
</span></span><dl>

[<span data-ttu-id="7bc34-136">Windows 屬性儲存區</span><span class="sxs-lookup"><span data-stu-id="7bc34-136">Windows Property Store</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="7bc34-137">Windows Vista 影像中心</span><span class="sxs-lookup"><span data-stu-id="7bc34-137">Windows Vista Photo Gallery</span></span>](-wic-integrationregentries.md)  
[<span data-ttu-id="7bc34-138">Windows Vista 縮圖快取</span><span class="sxs-lookup"><span data-stu-id="7bc34-138">Windows Vista Thumbnail Cache</span></span>](-wic-integrationregentries.md)  
<span data-ttu-id="7bc34-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">安裝編解碼器時，更新縮圖</a>快取，[讓使用者可以使用 WIC-Enabled 編解碼器的](-wic-codecinstallandreg.md)</dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">結論</a>  
</span><span class="sxs-lookup"><span data-stu-id="7bc34-139"></dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Updating the Thumbnail Cache when Installing a Codec</a> [Making Your WIC-Enabled Codec Available to Users](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">Conclusion</a>  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="7bc34-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bc34-140">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7bc34-141">**概念**</span><span class="sxs-lookup"><span data-stu-id="7bc34-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7bc34-142">簡介 (如何撰寫 WIC-Enabled 編解碼器) </span><span class="sxs-lookup"><span data-stu-id="7bc34-142">Introduction (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[<span data-ttu-id="7bc34-143">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="7bc34-143">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



