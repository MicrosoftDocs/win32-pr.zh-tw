---
description: 下列一組主題提供有關如何實行可在 Windows 影像處理元件 (WIC) framework 中運作之相機原始影像格式的指引。
ms.assetid: 145459fe-8ef4-41ba-b062-00f435c982e5
title: 相機原始影像格式的 WIC 指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09405f0f57aaa075678127d5d08bafcd28ecc6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193553"
---
# <a name="wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="53372-103">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="53372-103">WIC Guidelines for Camera RAW Image Formats</span></span>

<span data-ttu-id="53372-104">下列一組主題提供有關如何實行可在 Windows 影像處理元件 (WIC) framework 中運作之相機原始影像格式的指引。</span><span class="sxs-lookup"><span data-stu-id="53372-104">The following set of topics provide guidance on how to implement camera RAW image formats that will function within the Windows Imaging Component (WIC) framework.</span></span>

<dl>

[<span data-ttu-id="53372-105">簡介</span><span class="sxs-lookup"><span data-stu-id="53372-105">Introduction</span></span>](-wic-rawguidelines-intro.md)  
<dl>

[<span data-ttu-id="53372-106">Windows Vista 中的原始影像格式</span><span class="sxs-lookup"><span data-stu-id="53372-106">RAW Image Formats in Windows Vista</span></span>](-wic-rawguidelines-intro-vista.md)  
[<span data-ttu-id="53372-107">執行原始編解碼器的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="53372-107">General Guidelines for Implementing RAW Codecs</span></span>](-wic-rawguidelines-intro-implement.md)  
<span data-ttu-id="53372-108"></dl> </dd> <a href="-wic-rawguidelines-feature-complete.md">功能完整性：建議的介面</a>[介面方法需求](-wic-rawguidelines-iface-reqs.md)</span><span class="sxs-lookup"><span data-stu-id="53372-108"></dl> </dd> <a href="-wic-rawguidelines-feature-complete.md">Feature Completeness: Recommended Interfaces</a> [Interface Method Requirements](-wic-rawguidelines-iface-reqs.md)</span></span>  
<span data-ttu-id="53372-109">[中繼資料支援](-wic-rawguidelines-metadata.md)  
</span><span class="sxs-lookup"><span data-stu-id="53372-109">[Metadata Support](-wic-rawguidelines-metadata.md)  
</span></span><dl>

[<span data-ttu-id="53372-110">解碼</span><span class="sxs-lookup"><span data-stu-id="53372-110">Decoding</span></span>](-wic-rawguidelines-metadata-decoding.md)  
[<span data-ttu-id="53372-111">編碼方式</span><span class="sxs-lookup"><span data-stu-id="53372-111">Encoding</span></span>](-wic-rawguidelines-metadata-encoding.md)  
<span data-ttu-id="53372-112"></dl> </dd> <a href="/windows/desktop/wic/-wic-rawguidelines-iwicdevelopraw">支援 IWICDevelopRaw</a> [實施序列化 IWICDevelopRaw 設定的指導方針](-wic-rawguidelines-iwicdevelopraw-serializing.md)</span><span class="sxs-lookup"><span data-stu-id="53372-112"></dl> </dd> <a href="/windows/desktop/wic/-wic-rawguidelines-iwicdevelopraw">Support for IWICDevelopRaw</a> [Implementing Guidelines for Serializing IWICDevelopRaw Settings](-wic-rawguidelines-iwicdevelopraw-serializing.md)</span></span>  
[<span data-ttu-id="53372-113">效能</span><span class="sxs-lookup"><span data-stu-id="53372-113">Performance</span></span>](-wic-rawguidelines-performance.md)  
[<span data-ttu-id="53372-114">高動態範圍像素格式</span><span class="sxs-lookup"><span data-stu-id="53372-114">High Dynamic Range Pixel Formats</span></span>](-wic-rawguidelines-hdr-formats.md)  
[<span data-ttu-id="53372-115">縮圖和預覽</span><span class="sxs-lookup"><span data-stu-id="53372-115">Thumbnails and Previews</span></span>](-wic-rawguidelines-thumbnail-previews.md)  
[<span data-ttu-id="53372-116">可靠性和安全性</span><span class="sxs-lookup"><span data-stu-id="53372-116">Reliability and Security</span></span>](-wic-rawguidelines-reliability-security.md)  
<span data-ttu-id="53372-117">[編解碼器可用性和平臺支援](-wic-rawguidelines-availability.md)  
</span><span class="sxs-lookup"><span data-stu-id="53372-117">[Codec Availability and Platform Support](-wic-rawguidelines-availability.md)  
</span></span><dl>

[<span data-ttu-id="53372-118">編解碼器探索</span><span class="sxs-lookup"><span data-stu-id="53372-118">Codec Discovery</span></span>](-wic-rawguidelines-availability.md)  
[<span data-ttu-id="53372-119">Windows XP 平臺支援</span><span class="sxs-lookup"><span data-stu-id="53372-119">Windows XP Platform Support</span></span>](-wic-rawguidelines-availability.md)  
<span data-ttu-id="53372-120">適用于</dl> </dd> <a href="-wic-rawguidelines-win7.md">Windows 7 的原始編解碼器需求</a> [（如需詳細資訊](-wic-rawguidelines-moreinfo.md)）  
</span><span class="sxs-lookup"><span data-stu-id="53372-120"></dl> </dd> <a href="-wic-rawguidelines-win7.md">RAW Codec Requirements for Windows 7</a> [For More Information](-wic-rawguidelines-moreinfo.md)  
</span></span></dl>

## <a name="related-topics"></a><span data-ttu-id="53372-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="53372-121">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="53372-122">**概念**</span><span class="sxs-lookup"><span data-stu-id="53372-122">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53372-123">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="53372-123">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="53372-124">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="53372-124">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="53372-125">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="53372-125">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
