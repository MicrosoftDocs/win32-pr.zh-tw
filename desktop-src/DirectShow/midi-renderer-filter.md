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
# <a name="midi-renderer-filter"></a>MIDI 轉譯器篩選

MIDI 轉譯器篩選器會從 [midi](midi-parser-filter.md) 剖析器篩選器呈現 midi 資料。



| 標籤 | 值 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)、 [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)、 [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                                                                                                                                                                                                                                                                                                  |
| 輸入 Pin 介面                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| 輸出 Pin 媒體類型                   | 不適用                                                                                                                                                                                                                                                                                                                                                                       |
| 輸出 Pin 介面                    | 不適用                                                                                                                                                                                                                                                                                                                                                                       |
| 篩選 CLSID                             | CLSID \_ AVIMIDIRender                                                                                                                                                                                                                                                                                                                                                                 |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                                                                                                                                                                                                                                                                                                     |
| 可執行檔                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [優點](merit.md)                       | \_慣用                                                                                                                                                                                                                                                                                                                                                                     |
| [篩選準則分類](filter-categories.md) | CLSID \_ MidiRendererCategory                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

格式類型的 GUID 是 **Null**，但格式區塊包含下列結構：


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



**DwDivision** 成員會指定檔案的時間分割。 在區塊中任何標準 MIDI 檔案 (SMF) 的標頭中會提供時間劃分 `MThd` 。 MIDI 轉譯器會藉由呼叫 **midiStreamProperty** 函數，在 midi 資料流程上設定此屬性。

來自 MIDI 剖析器篩選器的範例包含一秒的 MIDI 資料。 MIDI 轉譯器使用 **midiStreamOut** 函式來呈現 MIDI 資料。 每個範例都是同步處理點：緩衝區的開頭包含設定正確狀態以呈現該緩衝區所需的所有命令。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Windows.。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 篩選](directshow-filters.md)
</dt> </dl>

 

 




