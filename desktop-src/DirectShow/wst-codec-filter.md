---
description: WST 編解碼器篩選
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: WST 編解碼器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320895"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="062ab-103">WST 編解碼器篩選</span><span class="sxs-lookup"><span data-stu-id="062ab-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="062ab-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="062ab-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="062ab-105">它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="062ab-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="062ab-106">從 Windows Vista 開始，此篩選器會取代為 Microsoft 電視技術檔中記載的 VBICodec 篩選器。</span><span class="sxs-lookup"><span data-stu-id="062ab-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="062ab-107">全球標準 Teletext (WST) 是使用 VBI 在 PAL 類比電視信號上進行資料傳輸的歐洲標準。</span><span class="sxs-lookup"><span data-stu-id="062ab-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="062ab-108">這兩個字幕和資料服務都是使用這個標準提供的。</span><span class="sxs-lookup"><span data-stu-id="062ab-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="062ab-109">WST 編解碼器是一種核心模式篩選器，它會接收原始 VBI 範例，並選擇性地從 Capture 篩選器篩選器中的 Teletext 範例，透過端 [對端對接收器轉換器](tee-sink-to-sink-converter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="062ab-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="062ab-110">此編解碼器會解碼及/或複製 [WST 解碼](wst-decoder-filter.md) 篩選器的已解碼和向前更正錯誤的 Teletext 資料。</span><span class="sxs-lookup"><span data-stu-id="062ab-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="062ab-111">WST 編解碼器對應于 NTSC 傳輸的 CC 編碼器篩選器。</span><span class="sxs-lookup"><span data-stu-id="062ab-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="062ab-112">WST 解碼器對應于 NTSC 的 [第21行](line-21-decoder-filter.md) ：這些篩選器會建立傳送至重迭混音器或影片混合轉譯器的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="062ab-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="062ab-113">此篩選器有兩個輸入圖釘： VBI 和 HWCC。</span><span class="sxs-lookup"><span data-stu-id="062ab-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="062ab-114">VBI 的 pin 會用於原始的 VBI 資料，而 HWCC 的 pin 會在使用 capture 篩選器在硬體中執行 VBI 解碼時使用。</span><span class="sxs-lookup"><span data-stu-id="062ab-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="062ab-115">在 HWCC 釘選上接收資料時，WST 編解碼器會在「通過」模式中運作，並將資料直接傳送至 WST 的編碼器，而不需要以任何方式進行處理。</span><span class="sxs-lookup"><span data-stu-id="062ab-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="062ab-116">如果捕捉篩選器公開 HWCC 的 pin，則必須直接連線到 WST 編解碼器上的對應 pin。</span><span class="sxs-lookup"><span data-stu-id="062ab-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="062ab-117">WST 編解碼器篩選器會出現在「WDM 串流 VBI 編解碼器」篩選類別中， (**AM \_ KSCATEGORY \_ VBICODEC**) 。</span><span class="sxs-lookup"><span data-stu-id="062ab-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="062ab-118">由於這是核心模式篩選器，因此應用程式無法直接使用 **CoCreateInstance** 來建立它。</span><span class="sxs-lookup"><span data-stu-id="062ab-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="062ab-119">相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="062ab-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="062ab-120">如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="062ab-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="062ab-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="062ab-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="062ab-122">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="062ab-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="062ab-123">觀賞全球標準 Teletext</span><span class="sxs-lookup"><span data-stu-id="062ab-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



