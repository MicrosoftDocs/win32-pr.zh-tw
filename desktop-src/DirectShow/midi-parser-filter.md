---
description: MIDI 剖析器篩選
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: MIDI 剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935641"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="571fe-103">MIDI 剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="571fe-103">MIDI Parser Filter</span></span>

<span data-ttu-id="571fe-104">MIDI 剖析器篩選器會讀取中找到的 MIDI 資料。中間和。RMI 檔。</span><span class="sxs-lookup"><span data-stu-id="571fe-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="571fe-105">篩選器會接受來自非同步檔案 [來源](file-source--async--filter.md) 或 URL 檔案 [來源](file-source--url--filter.md) 篩選的資料流程，並將 Midi 範例輸出至 [**midi**](midi-renderer-filter.md) 轉譯器以供播放。</span><span class="sxs-lookup"><span data-stu-id="571fe-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="571fe-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="571fe-106">Filter Interfaces</span></span>                        | <span data-ttu-id="571fe-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="571fe-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="571fe-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="571fe-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="571fe-109">媒體媒體 \_ 、MEDIASUBTYPE \_ Midi</span><span class="sxs-lookup"><span data-stu-id="571fe-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="571fe-110">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="571fe-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="571fe-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="571fe-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="571fe-112">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="571fe-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="571fe-113">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="571fe-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="571fe-114">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="571fe-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="571fe-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="571fe-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="571fe-116">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="571fe-116">Filter CLSID</span></span>                             | <span data-ttu-id="571fe-117">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="571fe-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="571fe-118">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="571fe-118">Property Page CLSID</span></span>                      | <span data-ttu-id="571fe-119">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="571fe-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="571fe-120">可執行檔</span><span class="sxs-lookup"><span data-stu-id="571fe-120">Executable</span></span>                               | <span data-ttu-id="571fe-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="571fe-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="571fe-122">優點</span><span class="sxs-lookup"><span data-stu-id="571fe-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="571fe-123">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="571fe-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="571fe-124">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="571fe-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="571fe-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="571fe-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="571fe-126">備註</span><span class="sxs-lookup"><span data-stu-id="571fe-126">Remarks</span></span>

<span data-ttu-id="571fe-127">如需詳細資訊，請參閱 [**MIDI**](midi-renderer-filter.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="571fe-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="571fe-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="571fe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571fe-129">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="571fe-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



