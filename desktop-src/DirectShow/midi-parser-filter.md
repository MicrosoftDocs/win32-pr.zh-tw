---
description: MIDI 剖析器篩選
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: MIDI 剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908426"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="34bf7-103">MIDI 剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="34bf7-103">MIDI Parser Filter</span></span>

<span data-ttu-id="34bf7-104">MIDI 剖析器篩選器會讀取中找到的 MIDI 資料。中間和。RMI 檔。</span><span class="sxs-lookup"><span data-stu-id="34bf7-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="34bf7-105">篩選器會接受來自非同步檔案 [來源](file-source--async--filter.md) 或 URL 檔案 [來源](file-source--url--filter.md) 篩選的資料流程，並將 Midi 範例輸出至 [**midi**](midi-renderer-filter.md) 轉譯器以供播放。</span><span class="sxs-lookup"><span data-stu-id="34bf7-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="34bf7-106">標籤</span><span class="sxs-lookup"><span data-stu-id="34bf7-106">Label</span></span> | <span data-ttu-id="34bf7-107">值</span><span class="sxs-lookup"><span data-stu-id="34bf7-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bf7-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="34bf7-108">Filter Interfaces</span></span>                        | <span data-ttu-id="34bf7-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="34bf7-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="34bf7-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="34bf7-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="34bf7-111">媒體媒體 \_ 、MEDIASUBTYPE \_ Midi</span><span class="sxs-lookup"><span data-stu-id="34bf7-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="34bf7-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="34bf7-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="34bf7-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="34bf7-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="34bf7-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="34bf7-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="34bf7-115">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="34bf7-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="34bf7-116">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="34bf7-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="34bf7-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="34bf7-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="34bf7-118">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="34bf7-118">Filter CLSID</span></span>                             | <span data-ttu-id="34bf7-119">CLSID \_ MIDIParser</span><span class="sxs-lookup"><span data-stu-id="34bf7-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="34bf7-120">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="34bf7-120">Property Page CLSID</span></span>                      | <span data-ttu-id="34bf7-121">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="34bf7-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="34bf7-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="34bf7-122">Executable</span></span>                               | <span data-ttu-id="34bf7-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="34bf7-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="34bf7-124">優點</span><span class="sxs-lookup"><span data-stu-id="34bf7-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="34bf7-125">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="34bf7-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="34bf7-126">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="34bf7-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="34bf7-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="34bf7-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="34bf7-128">備註</span><span class="sxs-lookup"><span data-stu-id="34bf7-128">Remarks</span></span>

<span data-ttu-id="34bf7-129">如需詳細資訊，請參閱 [**MIDI**](midi-renderer-filter.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="34bf7-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34bf7-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="34bf7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34bf7-131">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="34bf7-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



