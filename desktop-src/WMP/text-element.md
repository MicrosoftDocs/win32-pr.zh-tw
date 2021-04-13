---
title: " (Windows Media Player SDK 的 TEXT 元素) "
description: TEXT 元素
ms.assetid: 4523fe7a-a77a-4bf2-9195-3943bff0eb21
keywords:
- Windows Media Player 的外觀，TEXT 元素
- 外觀，TEXT 元素
- TEXT 元素
- 外觀的參考，TEXT 元素
- 元素、文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acdad737fda44cc0e090eb13fb20c765b447ccbd
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313599"
---
# <a name="text-element"></a>TEXT 元素

**Text** 元素提供一種方式，可讓您使用下列屬性來建立和控制台內文字的外觀。 為了方便起見，也提供預先定義的 **文字** 元素。

**TEXT** 元素支援下列屬性。



| 屬性                                                   | 描述                                                                                                 |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](text-backgroundcolor.md)                 | 指定或抓取文字控制項的背景色彩。                                           |
| [cursor](text-cursor.md)                                   | 指定或抓取值，指出當滑鼠停留在文字控制項上時，所顯示的游標。     |
| [disabledBackgroundColor](text-disabledbackgroundcolor.md) | 指定或抓取文字控制項停用時所用的背景色彩。                  |
| [disabledFontStyle](text-disabledfontstyle.md)             | 指定或抓取文字控制項停用時所用的字型樣式。                        |
| [disabledForegroundColor](text-disabledforegroundcolor.md) | 指定或抓取文字控制項停用時使用的文字色彩。                               |
| [fontFace](text-fontface.md)                               | 指定或抓取文字控制項的字樣。                                                   |
| [fontSize](text-fontsize.md)                               | 指定或抓取文字控制項的字型大小。                                                  |
| [fontSmoothing](text-fontsmoothing.md)                     | 指定或抓取值，指出是否已啟用字型平滑。                                |
| [fontStyle](text-fontstyle.md)                             | 指定或抓取文字控制項的字型樣式。                                                 |
| [foregroundColor](text-foregroundcolor.md)                 | 指定或抓取文字控制項的文字色彩。                                                 |
| [hoverBackgroundColor](text-hoverbackgroundcolor.md)       | 指定或抓取當滑鼠游標停留在文字控制項上方時，用於文字控制項的背景色彩。 |
| [hoverFontStyle](text-hoverfontstyle.md)                   | 指定或抓取當滑鼠游標停留在文字控制項上方時，用於文字控制項的字型樣式。       |
| [hoverForegroundColor](text-hoverforegroundcolor.md)       | 指定或抓取當滑鼠游標停留在文字控制項上方時，用於文字控制項的文字色彩。       |
| [理由](text-justification.md)                     | 指定或抓取文字控制項中文字的對齊方式。                                   |
| [滾動](text-scrolling.md)                             | 指定或抓取值，指出文字是否滾動。                                         |
| [scrollingAmount](text-scrollingamount.md)                 | 指定或抓取文字在每個滾動移動期間移動的圖元數。             |
| [scrollingDelay](text-scrollingdelay.md)                   | 指定或抓取滾動移動之間的時間延遲。                                          |
| [scrollingDirection](text-scrollingdirection.md)           | 指定或抓取滾動文字的方向。                                                 |
| [textWidth](text-textwidth.md)                             | 抓取 **值** 屬性中所包含之字串的寬度（以圖元為單位）。                           |
| [提示](text-tooltip.md)                                 | 指定或抓取文字控制項的工具提示文字。                                               |
| [value](text-value.md)                                     | 指定或抓取文字控制項中顯示的文字。                                      |
| [wordWrap](text-wordwrap.md)                               | 指定或抓取值，指出是否啟用或停用自動換行。                     |



 

**TEXT** 元素支援環境屬性，並可執行環境事件處理常式。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

預先定義的文字專案是一般 **文字** 元素，預設會指定各種不同的屬性設定。 提供下列預先定義的文字專案。



| 預先定義的文字                                | Description                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------|
| [CURRENTPOSITIONTEXT](currentpositiontext.md) | 具有 **currentPositionString** 之內建接聽程式的 **文字** 專案。 |
| [DURATIONTEXT](durationtext.md)               | 具有 **CurrentMedia DurationString** 之內建接聽程式的 **文字** 專案。    |
| [STATUSTEXT](statustext.md)                   | 具有適用于 **播放** 程式之內建接聽程式的 **文字** 專案。                         |
| [TRACKNAMETEXT](tracknametext.md)             | 具有 **player.currentMedia.name** 之內建接聽程式的 **文字** 專案。              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




