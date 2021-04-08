---
title: Controls 物件
description: Controls 物件提供使用下列屬性和方法來操作媒體播放的方式。
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- 控制項物件 Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678832"
---
# <a name="controls-object"></a>Controls 物件

**Controls** 物件提供使用下列屬性和方法來操作媒體播放的方式。

**Controls** 物件支援下列屬性。



| 屬性                                                            | 描述                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [audioLanguageCount](controls-audiolanguagecount.md)               | 抓取支援的音訊語言數目。                                                                                                |
| [currentAudioLanguage](controls-currentaudiolanguage.md)           | 指定或抓取用來播放音訊語言 (LCID) 的地區設定識別碼                                                            |
| [currentAudioLanguageIndex](controls-currentaudiolanguageindex.md) | 指定或抓取對應于播放音訊語言的單一索引。                                                   |
| [currentItem](controls-currentitem.md)                             | 指定或抓取目前的媒體專案。                                                                                                    |
| [currentMarker](controls-currentmarker.md)                         | 指定或抓取目前的標記編號。                                                                                                 |
| [currentPosition](controls-currentposition.md)                     | 以秒為單位，指定或抓取媒體專案中的目前位置。                                                      |
| [currentPositionString](controls-currentpositionstring.md)         | 以 **字串** 形式捕獲媒體專案中的目前位置。                                                                                 |
| [currentPositionTimecode](controls-currentpositiontimecode.md)     | 使用時間代碼格式，指定或抓取目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。 |
| [isAvailable](controls-isavailable.md)                             | 抓取指定的資訊類型是否可用，或是否可以執行指定的動作。                                                |



 

**Controls** 物件支援下列方法。



| 方法                                                                  | 描述                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [fastForward](controls-fastforward.md)                                 | 以正向方向啟動媒體專案的快速播放。                                     |
| [fastReverse](controls-fastreverse.md)                                 | 以相反方向啟動媒體專案的快速播放。                                     |
| [getAudioLanguageDescription](controls-getaudiolanguagedescription.md) | 抓取對應于指定之以一為基礎之索引的音訊語言描述。 |
| [getAudioLanguageID](controls-getaudiolanguageid.md)                   | 抓取指定音訊語言索引的 LCID。                                         |
| [getLanguageName](controls-getlanguagename.md)                         | 使用指定的 LCID 抓取音訊語言的名稱。                                |
| [下一步](controls-next.md)                                               | 將目前的專案設定為播放清單中的下一個專案。                                          |
| [pause](controls-pause.md)                                             | 暫停媒體專案的播放。                                                            |
| [玩](controls-play.md)                                               | 造成媒體專案開始播放。                                                          |
| [playItem](controls-playitem.md)                                       | 導致目前的媒體專案開始播放，或繼續播放暫停的專案。                |
| [previous](controls-previous.md)                                       | 將目前的專案設定為播放清單中的上一個專案。                                      |
| [步](controls-step.md)                                               | 導致目前的影片媒體專案凍結下一個畫面格的播放。                        |
| [停止](controls-stop.md)                                               | 停止播放媒體專案。                                                             |



 

您可以透過下列屬性來存取 **Controls** 物件。



| Object                      | 屬性                        |
|-----------------------------|---------------------------------|
| [球員](player-object.md) | [控制](player-controls.md) |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




