---
description: Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows 影像處理元件總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193140"
---
# <a name="windows-imaging-component-overview"></a><span data-ttu-id="6b7df-103">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="6b7df-103">Windows Imaging Component Overview</span></span>

<span data-ttu-id="6b7df-104">Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6b7df-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="6b7df-105">WIC 可讓獨立軟體廠商 (Isv) 和獨立硬體廠商 (Ihv) 開發自己的映射編解碼器，並取得與標準影像格式相同的平臺支援，例如 TIFF、JPEG、PNG、GIF、BMP 和 HDPhoto (。</span><span class="sxs-lookup"><span data-stu-id="6b7df-105">WIC makes it possible for independent software vendors (ISVs) and independent hardware vendors (IHVs) to develop their own image codecs and get the same platform support as standard image formats (for example, TIFF, JPEG, PNG, GIF, BMP, and HDPhoto).</span></span> <span data-ttu-id="6b7df-106">不論影像格式為何，都使用單一、一致的介面集來處理所有圖像，因此任何使用 WIC 的應用程式都會在安裝編解碼器時，自動支援新的映射格式。</span><span class="sxs-lookup"><span data-stu-id="6b7df-106">A single, consistent set of interfaces is used for all image processing, regardless of image format, so any application using the WIC gets automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="6b7df-107">可延伸的中繼資料架構可讓應用程式將自己的專屬中繼資料直接讀取和寫入影像檔案，因此中繼資料永遠不會遺失或與影像分開。</span><span class="sxs-lookup"><span data-stu-id="6b7df-107">The extensible metadata framework makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata never gets lost or separated from the image.</span></span>

<span data-ttu-id="6b7df-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6b7df-108">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="6b7df-109">Windows 影像處理元件功能</span><span class="sxs-lookup"><span data-stu-id="6b7df-109">Windows Imaging Component Features</span></span>](#windows-imaging-component-features)
-   [<span data-ttu-id="6b7df-110">原生編解碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-110">Native Codecs</span></span>](#native-codecs)
-   [<span data-ttu-id="6b7df-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b7df-111">Related topics</span></span>](#related-topics)

## <a name="windows-imaging-component-features"></a><span data-ttu-id="6b7df-112">Windows 影像處理元件功能</span><span class="sxs-lookup"><span data-stu-id="6b7df-112">Windows Imaging Component Features</span></span>

<span data-ttu-id="6b7df-113">WIC 的主要功能包括：</span><span class="sxs-lookup"><span data-stu-id="6b7df-113">The primary features of WIC are:</span></span>

-   <span data-ttu-id="6b7df-114">可讓應用程式開發人員透過單一、一致的通用介面集，以任何影像格式執行影像處理作業，而不需要事先知道特定影像格式。</span><span class="sxs-lookup"><span data-stu-id="6b7df-114">Enables application developers to perform image processing operations on any image format through a single, consistent set of common interfaces, without requiring prior knowledge of specific image formats.</span></span>
-   <span data-ttu-id="6b7df-115">為影像編解碼器、像素格式和中繼資料提供可延伸的「隨插即用」架構，並自動執行新格式的執行時間探索。</span><span class="sxs-lookup"><span data-stu-id="6b7df-115">Provides an extensible "plug and play" architecture for image codecs, pixel formats, and metadata, with automatic run-time discovery of new formats.</span></span>
-   <span data-ttu-id="6b7df-116">支援在影像檔案中讀取和寫入任意中繼資料，並能夠在編輯期間保留無法辨識的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6b7df-116">Supports reading and writing of arbitrary metadata in image files, with the ability to preserve unrecognized metadata during editing.</span></span>
-   <span data-ttu-id="6b7df-117">在整個影像處理管線中保留高位深度的影像資料，最多可達32位的每個通道。</span><span class="sxs-lookup"><span data-stu-id="6b7df-117">Preserves high bit depth image data, up to 32 bits per channel, throughout the image processing pipeline.</span></span>
-   <span data-ttu-id="6b7df-118">針對最熱門的影像格式、像素格式和中繼資料架構，提供內建支援。</span><span class="sxs-lookup"><span data-stu-id="6b7df-118">Provides built-in support for most popular image formats, pixel formats, and metadata schemas.</span></span>

## <a name="native-codecs"></a><span data-ttu-id="6b7df-119">原生編解碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-119">Native Codecs</span></span>

<span data-ttu-id="6b7df-120">WIC 包含數個內建編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6b7df-120">WIC includes several built-in codecs.</span></span> <span data-ttu-id="6b7df-121">平臺提供下列標準編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6b7df-121">The following standard codecs are provided with the platform.</span></span> 

| <span data-ttu-id="6b7df-122">轉碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-122">Codec</span></span>                                                                                             | <span data-ttu-id="6b7df-123">Mime 類型</span><span class="sxs-lookup"><span data-stu-id="6b7df-123">Mime Types</span></span>                       | <span data-ttu-id="6b7df-124">解碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-124">Decoders</span></span> | <span data-ttu-id="6b7df-125">編碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-125">Encoders</span></span> |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| <span data-ttu-id="6b7df-126">BMP (Windows 點陣圖格式) 、BMP 規格 v5。</span><span class="sxs-lookup"><span data-stu-id="6b7df-126">BMP (Windows Bitmap Format), BMP Specification v5.</span></span>                                                | <span data-ttu-id="6b7df-127">image/bmp</span><span class="sxs-lookup"><span data-stu-id="6b7df-127">image/bmp</span></span>                        | <span data-ttu-id="6b7df-128">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-128">Yes</span></span>      | <span data-ttu-id="6b7df-129">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-129">Yes</span></span>      |
| <span data-ttu-id="6b7df-130">GIF (圖形交換格式 89a) 、GIF 規格 89a/89m</span><span class="sxs-lookup"><span data-stu-id="6b7df-130">GIF (Graphics Interchange Format 89a), GIF Specification 89a/89m</span></span>                                  | <span data-ttu-id="6b7df-131">image/gif</span><span class="sxs-lookup"><span data-stu-id="6b7df-131">image/gif</span></span>                        | <span data-ttu-id="6b7df-132">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-132">Yes</span></span>      | <span data-ttu-id="6b7df-133">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-133">Yes</span></span>      |
| <span data-ttu-id="6b7df-134">.ICO (圖示格式) </span><span class="sxs-lookup"><span data-stu-id="6b7df-134">ICO (Icon Format)</span></span>                                                                                 | <span data-ttu-id="6b7df-135">影像/.ico</span><span class="sxs-lookup"><span data-stu-id="6b7df-135">image/ico</span></span>                        | <span data-ttu-id="6b7df-136">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-136">Yes</span></span>      | <span data-ttu-id="6b7df-137">否</span><span class="sxs-lookup"><span data-stu-id="6b7df-137">No</span></span>       |
| <span data-ttu-id="6b7df-138">JPEG (聯合攝影專家群組) 、JFIF 規格1.02</span><span class="sxs-lookup"><span data-stu-id="6b7df-138">JPEG (Joint Photographic Experts Group), JFIF Specification 1.02</span></span>                                  | <span data-ttu-id="6b7df-139">image/jpeg、image/jpe、image/jpg</span><span class="sxs-lookup"><span data-stu-id="6b7df-139">image/jpeg, image/jpe, image/jpg</span></span> | <span data-ttu-id="6b7df-140">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-140">Yes</span></span>      | <span data-ttu-id="6b7df-141">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-141">Yes</span></span>      |
| <span data-ttu-id="6b7df-142">PNG (可攜的網狀圖形) ，PNG 規格1。2</span><span class="sxs-lookup"><span data-stu-id="6b7df-142">PNG (Portable Network Graphics), PNG Specification 1.2</span></span>                                            | <span data-ttu-id="6b7df-143">image/png</span><span class="sxs-lookup"><span data-stu-id="6b7df-143">image/png</span></span>                        | <span data-ttu-id="6b7df-144">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-144">Yes</span></span>      | <span data-ttu-id="6b7df-145">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-145">Yes</span></span>      |
| <span data-ttu-id="6b7df-146">TIFF (標記的影像檔案格式) ，TIFF 規格6。0</span><span class="sxs-lookup"><span data-stu-id="6b7df-146">TIFF (Tagged Image File Format), TIFF Specification 6.0</span></span>                                           | <span data-ttu-id="6b7df-147">影像/tiff、影像/.tif</span><span class="sxs-lookup"><span data-stu-id="6b7df-147">image/tiff, image/tif</span></span>            | <span data-ttu-id="6b7df-148">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-148">Yes</span></span>      | <span data-ttu-id="6b7df-149">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-149">Yes</span></span>      |
| <span data-ttu-id="6b7df-150">Windows Media 相片、 [HD 相片規格 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span><span class="sxs-lookup"><span data-stu-id="6b7df-150">Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)</span></span> | <span data-ttu-id="6b7df-151">image/vnd.openxmlformats-officedocument.spreadsheetml.sheet. ms-phot</span><span class="sxs-lookup"><span data-stu-id="6b7df-151">image/vnd.ms-phot</span></span>                | <span data-ttu-id="6b7df-152">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-152">Yes</span></span>      | <span data-ttu-id="6b7df-153">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-153">Yes</span></span>      |
| <span data-ttu-id="6b7df-154">DDS (DirectDraw 介面) </span><span class="sxs-lookup"><span data-stu-id="6b7df-154">DDS (DirectDraw Surface)</span></span>                                                                          | <span data-ttu-id="6b7df-155">image/vnd.openxmlformats-officedocument.spreadsheetml.sheet. ms-dds</span><span class="sxs-lookup"><span data-stu-id="6b7df-155">image/vnd.ms-dds</span></span>                 | <span data-ttu-id="6b7df-156">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-156">Yes</span></span>      | <span data-ttu-id="6b7df-157">是</span><span class="sxs-lookup"><span data-stu-id="6b7df-157">Yes</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="6b7df-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b7df-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6b7df-159">**概念**</span><span class="sxs-lookup"><span data-stu-id="6b7df-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7df-160">WIC 中繼資料總覽</span><span class="sxs-lookup"><span data-stu-id="6b7df-160">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

<span data-ttu-id="6b7df-161">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="6b7df-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6b7df-162">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="6b7df-162">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

<span data-ttu-id="6b7df-163">[AITCodec 範例編解碼器](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7df-163">[AITCodec Sample CODEC](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))</span></span>
</dt> </dl>

 

 
