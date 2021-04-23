---
description: MIDI 轉譯器篩選器會從 MIDI 剖析器篩選器呈現 MIDI 資料。
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: 'MIDI 轉譯器篩選器 (Windows. .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 5fa27ceda0c249f88f4684979382495167cb9238
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909406"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="fbe0c-103">MIDI 轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="fbe0c-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="fbe0c-104">MIDI 轉譯器篩選器會從 [midi](midi-parser-filter.md) 剖析器篩選器呈現 midi 資料。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



| <span data-ttu-id="fbe0c-105">標籤</span><span class="sxs-lookup"><span data-stu-id="fbe0c-105">Label</span></span> | <span data-ttu-id="fbe0c-106">值</span><span class="sxs-lookup"><span data-stu-id="fbe0c-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe0c-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="fbe0c-107">Filter Interfaces</span></span>                        | <span data-ttu-id="fbe0c-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)、 [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)、 [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="fbe0c-108">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="fbe0c-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="fbe0c-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="fbe0c-110">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="fbe0c-110">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="fbe0c-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="fbe0c-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="fbe0c-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="fbe0c-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fbe0c-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="fbe0c-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="fbe0c-114">不適用</span><span class="sxs-lookup"><span data-stu-id="fbe0c-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fbe0c-115">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="fbe0c-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="fbe0c-116">不適用</span><span class="sxs-lookup"><span data-stu-id="fbe0c-116">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fbe0c-117">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="fbe0c-117">Filter CLSID</span></span>                             | <span data-ttu-id="fbe0c-118">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="fbe0c-118">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fbe0c-119">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="fbe0c-119">Property Page CLSID</span></span>                      | <span data-ttu-id="fbe0c-120">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="fbe0c-120">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="fbe0c-121">可執行檔</span><span class="sxs-lookup"><span data-stu-id="fbe0c-121">Executable</span></span>                               | <span data-ttu-id="fbe0c-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="fbe0c-122">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="fbe0c-123">優點</span><span class="sxs-lookup"><span data-stu-id="fbe0c-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="fbe0c-124">\_慣用</span><span class="sxs-lookup"><span data-stu-id="fbe0c-124">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="fbe0c-125">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="fbe0c-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="fbe0c-126">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="fbe0c-126">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="fbe0c-127">備註</span><span class="sxs-lookup"><span data-stu-id="fbe0c-127">Remarks</span></span>

<span data-ttu-id="fbe0c-128">格式類型的 GUID 是 **Null**，但格式區塊包含下列結構：</span><span class="sxs-lookup"><span data-stu-id="fbe0c-128">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="fbe0c-129">**DwDivision** 成員會指定檔案的時間分割。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-129">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="fbe0c-130">在區塊中任何標準 MIDI 檔案 (SMF) 的標頭中會提供時間劃分 `MThd` 。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-130">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="fbe0c-131">MIDI 轉譯器會藉由呼叫 **midiStreamProperty** 函數，在 midi 資料流程上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-131">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="fbe0c-132">來自 MIDI 剖析器篩選器的範例包含一秒的 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-132">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="fbe0c-133">MIDI 轉譯器使用 **midiStreamOut** 函式來呈現 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-133">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="fbe0c-134">每個範例都是同步處理點：緩衝區的開頭包含設定正確狀態以呈現該緩衝區所需的所有命令。</span><span class="sxs-lookup"><span data-stu-id="fbe0c-134">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbe0c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbe0c-135">Requirements</span></span>



| <span data-ttu-id="fbe0c-136">需求</span><span class="sxs-lookup"><span data-stu-id="fbe0c-136">Requirement</span></span> | <span data-ttu-id="fbe0c-137">值</span><span class="sxs-lookup"><span data-stu-id="fbe0c-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe0c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="fbe0c-138">Header</span></span><br/> | <dl> <span data-ttu-id="fbe0c-139"><dt>Windows.。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe0c-139"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe0c-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbe0c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe0c-141">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="fbe0c-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




