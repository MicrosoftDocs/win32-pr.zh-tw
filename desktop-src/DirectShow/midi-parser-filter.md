---
description: MIDI 剖析器篩選
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: MIDI 剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5907c36e668a39494b46ec6bbc67e4d8cb4870357df9c1f0303c882bc86f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256508"
---
# <a name="midi-parser-filter"></a>MIDI 剖析器篩選

MIDI 剖析器篩選器會讀取中找到的 MIDI 資料。中間和。RMI 檔。 篩選器會接受來自非同步檔案 [來源](file-source--async--filter.md) 或 URL 檔案 [來源](file-source--url--filter.md) 篩選的資料流程，並將 Midi 範例輸出至 [**midi**](midi-renderer-filter.md) 轉譯器以供播放。



| 標籤 | 值 |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| 篩選介面                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)、 [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| 輸入 Pin 媒體類型                    | 媒體媒體 \_ 、MEDIASUBTYPE \_ Midi                                                                    |
| 輸入 Pin 介面                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| 輸出 Pin 媒體類型                   | 媒體媒體 \_ 、MEDIASUBTYPE \_ Null                                                                      |
| 輸出 Pin 介面                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| 篩選 CLSID                             | CLSID \_ MIDIParser                                                                                        |
| 屬性頁 CLSID                      | 沒有屬性頁                                                                                         |
| 可執行檔                               | quartz.dll                                                                                               |
| [優點](merit.md)                       | 不 \_ 太可能                                                                                          |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>備註

如需詳細資訊，請參閱 [**MIDI**](midi-renderer-filter.md)轉譯器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> </dl>

 

 



