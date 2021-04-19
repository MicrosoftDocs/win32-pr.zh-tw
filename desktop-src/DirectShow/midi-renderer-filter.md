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
ms.openlocfilehash: 060bb00629b78fb1edbfbfd193aeaf7514c98ba4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979530"
---
# <a name="midi-renderer-filter"></a><span data-ttu-id="db67b-103">MIDI 轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="db67b-103">MIDI Renderer Filter</span></span>

<span data-ttu-id="db67b-104">MIDI 轉譯器篩選器會從 [midi](midi-parser-filter.md) 剖析器篩選器呈現 midi 資料。</span><span class="sxs-lookup"><span data-stu-id="db67b-104">The MIDI Renderer filter renders MIDI data from the [MIDI Parser](midi-parser-filter.md) filter.</span></span>



|                                          |                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db67b-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="db67b-105">Filter Interfaces</span></span>                        | <span data-ttu-id="db67b-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)、 [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)、 [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span><span class="sxs-lookup"><span data-stu-id="db67b-106">[**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)</span></span> |
| <span data-ttu-id="db67b-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="db67b-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="db67b-108">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="db67b-108">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="db67b-109">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="db67b-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="db67b-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="db67b-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="db67b-111">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="db67b-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="db67b-112">不適用</span><span class="sxs-lookup"><span data-stu-id="db67b-112">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="db67b-113">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="db67b-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="db67b-114">不適用</span><span class="sxs-lookup"><span data-stu-id="db67b-114">Not applicable</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="db67b-115">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="db67b-115">Filter CLSID</span></span>                             | <span data-ttu-id="db67b-116">CLSID \_ AVIMIDIRender</span><span class="sxs-lookup"><span data-stu-id="db67b-116">CLSID\_AVIMIDIRender</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="db67b-117">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="db67b-117">Property Page CLSID</span></span>                      | <span data-ttu-id="db67b-118">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="db67b-118">No property page</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="db67b-119">可執行檔</span><span class="sxs-lookup"><span data-stu-id="db67b-119">Executable</span></span>                               | <span data-ttu-id="db67b-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="db67b-120">quartz.dll</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="db67b-121">優點</span><span class="sxs-lookup"><span data-stu-id="db67b-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="db67b-122">\_慣用</span><span class="sxs-lookup"><span data-stu-id="db67b-122">MERIT\_PREFERRED</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="db67b-123">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="db67b-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="db67b-124">CLSID \_ MidiRendererCategory</span><span class="sxs-lookup"><span data-stu-id="db67b-124">CLSID\_MidiRendererCategory</span></span>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="db67b-125">備註</span><span class="sxs-lookup"><span data-stu-id="db67b-125">Remarks</span></span>

<span data-ttu-id="db67b-126">格式類型的 GUID 是 **Null**，但格式區塊包含下列結構：</span><span class="sxs-lookup"><span data-stu-id="db67b-126">The GUID for the format type is **NULL**, but the format block contains the following structure:</span></span>


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



<span data-ttu-id="db67b-127">**DwDivision** 成員會指定檔案的時間分割。</span><span class="sxs-lookup"><span data-stu-id="db67b-127">The **dwDivision** member specifies the time division of the file.</span></span> <span data-ttu-id="db67b-128">在區塊中任何標準 MIDI 檔案 (SMF) 的標頭中會提供時間劃分 `MThd` 。</span><span class="sxs-lookup"><span data-stu-id="db67b-128">The time division is given in the header of any standard MIDI file (SMF), in the `MThd` chunk.</span></span> <span data-ttu-id="db67b-129">MIDI 轉譯器會藉由呼叫 **midiStreamProperty** 函數，在 midi 資料流程上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="db67b-129">The MIDI Renderer sets this property on the MIDI data stream by calling the **midiStreamProperty** function.</span></span>

<span data-ttu-id="db67b-130">來自 MIDI 剖析器篩選器的範例包含一秒的 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="db67b-130">Samples from the MIDI Parser filter contain one second of MIDI data.</span></span> <span data-ttu-id="db67b-131">MIDI 轉譯器使用 **midiStreamOut** 函式來呈現 MIDI 資料。</span><span class="sxs-lookup"><span data-stu-id="db67b-131">The MIDI Renderer uses the **midiStreamOut** function to render the MIDI data.</span></span> <span data-ttu-id="db67b-132">每個範例都是同步處理點：緩衝區的開頭包含設定正確狀態以呈現該緩衝區所需的所有命令。</span><span class="sxs-lookup"><span data-stu-id="db67b-132">Each sample is a synchronization point: the start of the buffer contains all of the commands necessary to set the correct state for rendering that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="db67b-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="db67b-133">Requirements</span></span>



| <span data-ttu-id="db67b-134">需求</span><span class="sxs-lookup"><span data-stu-id="db67b-134">Requirement</span></span> | <span data-ttu-id="db67b-135">值</span><span class="sxs-lookup"><span data-stu-id="db67b-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db67b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="db67b-136">Header</span></span><br/> | <dl> <span data-ttu-id="db67b-137"><dt>Windows.。h</dt></span><span class="sxs-lookup"><span data-stu-id="db67b-137"><dt>Windows.devices.midi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db67b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db67b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db67b-139">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="db67b-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




