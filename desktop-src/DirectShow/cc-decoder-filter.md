---
description: CC 解碼篩選
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: CC 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935696"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="1f76e-103">CC 解碼篩選</span><span class="sxs-lookup"><span data-stu-id="1f76e-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f76e-104">此元件已從 Windows Vista 和更新版本的作業系統中移除。</span><span class="sxs-lookup"><span data-stu-id="1f76e-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="1f76e-105">它可在 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="1f76e-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="1f76e-106">CC VBI 解碼器是核心模式資料流程類別篩選。</span><span class="sxs-lookup"><span data-stu-id="1f76e-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="1f76e-107">它會顯示在 GraphEdit 的 [WDM 串流 VBI 編解碼器] 類別之下。</span><span class="sxs-lookup"><span data-stu-id="1f76e-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="1f76e-108">它接受 capture 篩選器所提供的範例波形，並將解碼的封閉字幕資料傳遞到 [第21行的解碼器](line-21-decoder-filter.md) 和/或感興趣的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1f76e-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="1f76e-109">此篩選器有兩個輸入圖釘： VBI 和 HWCC。</span><span class="sxs-lookup"><span data-stu-id="1f76e-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="1f76e-110">VBI 的 pin 會用於原始的 VBI 資料，而 HWCC 的 pin 會在使用 capture 篩選器在硬體中執行 VBI 解碼時使用。</span><span class="sxs-lookup"><span data-stu-id="1f76e-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="1f76e-111">在 HWCC 的 pin 上收到資料時，CC 解碼會以「通過」模式運作，並將資料直接傳送到第21行的解碼器，而不需要以任何方式處理。</span><span class="sxs-lookup"><span data-stu-id="1f76e-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="1f76e-112">如果捕捉篩選器公開 HWCC 的 pin，則必須直接連接到 CC 解碼器上的對應 pin。</span><span class="sxs-lookup"><span data-stu-id="1f76e-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="1f76e-113">Pin 類別為 **PINNAME \_ VIDEO \_ CC \_ CAPTURE**。</span><span class="sxs-lookup"><span data-stu-id="1f76e-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="1f76e-114">CC 解碼最多可有八個輸出圖釘，每個輸出都可以選取自己的行和子串流。</span><span class="sxs-lookup"><span data-stu-id="1f76e-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="1f76e-115">第一個輸出連接會連接到第21行的解碼器。</span><span class="sxs-lookup"><span data-stu-id="1f76e-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="1f76e-116">CC 編碼器篩選器會出現在 [WDM 串流 VBI 編解碼器] 篩選類別中， (**AM \_ KSCATEGORY \_ VBICODEC**) 。</span><span class="sxs-lookup"><span data-stu-id="1f76e-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="1f76e-117">由於這是核心模式篩選器，因此應用程式無法直接使用 **CoCreateInstance** 來建立它。</span><span class="sxs-lookup"><span data-stu-id="1f76e-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="1f76e-118">相反地，請使用 [系統裝置枚舉器](system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="1f76e-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="1f76e-119">如需詳細資訊，請參閱 [建立 Kernel-Mode 篩選](creating-kernel-mode-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="1f76e-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f76e-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f76e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f76e-121">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1f76e-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="1f76e-122">查看隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="1f76e-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



