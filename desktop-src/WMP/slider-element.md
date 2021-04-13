---
title: 滑杆元素
description: 滑杆元素
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Windows Media Player 面板，滑杆元素
- 外觀，滑杆元素
- 滑杆元素
- 外觀、滑杆元素的參考
- 元素、滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301148"
---
# <a name="slider-element"></a>滑杆元素

**滑杆** 元素提供建立和操作簡單水準或垂直滑杆控制項的方式。 它支援下列屬性和事件處理常式。 為了方便起見，也提供預先定義的 **滑杆** 元素。

**滑杆** 元素支援下列屬性。



| 屬性                                                 | 描述                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](slider-backgroundcolor.md)             | 指定或抓取滑杆控制項的背景色彩。                                                |
| [backgroundEndColor](slider-backgroundendcolor.md)       | 指定或抓取滑杆控制項的背景結束色彩。                                         |
| [backgroundHoverImage](slider-backgroundhoverimage.md)   | 指定或抓取將滑鼠停留在其上方時顯示之滑杆的背景影像。      |
| [backgroundImage](slider-backgroundimage.md)             | 指定或抓取滑杆的預設背景影像。                                                |
| [borderSize](slider-bordersize.md)                       | 指定或抓取框線大小（以圖元為單位）。                                                                 |
| [cursor](slider-cursor.md)                               | 指定或抓取值，指出當滑鼠停留在滑杆控制項上時，所顯示的游標類型。 |
| [direction](slider-direction.md)                         | 指定或抓取滑杆影像的配置方向。                                             |
| [disabledColor](slider-disabledcolor.md)                 | 指定或抓取滑杆控制項的停用色彩。                                                  |
| [disabledImage](slider-disabledimage.md)                 | 指定或抓取停用控制項時所顯示之滑杆的影像。                         |
| [foregroundColor](slider-foregroundcolor.md)             | 指定或抓取滑杆控制項的前景色彩。                                                |
| [foregroundEndColor](slider-foregroundendcolor.md)       | 指定或抓取滑杆控制項的前景結束色彩。                                         |
| [foregroundHoverImage](slider-foregroundhoverimage.md)   | 指定或抓取將滑鼠停留在其上方時顯示之滑杆的前景影像。      |
| [foregroundImage](slider-foregroundimage.md)             | 指定或抓取滑杆的預設前景影像。                                                |
| [foregroundProgress](slider-foregroundprogress.md)       | 指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。    |
| [max](slider-max.md)                                     | 指定或抓取滑杆控制項所定義範圍的最大值。                              |
| [min](slider-min.md)                                     | 指定或抓取滑杆控制項所定義範圍的最小值。                              |
| [幻燈片](slider-slide.md)                                 | 指定或抓取值，指出前景影像是否滑過背景影像。          |
| [thumbDisabledImage](slider-thumbdisabledimage.md)       | 指定或抓取滑杆控制項的停用捲動方塊影像。                                            |
| [thumbDownImage](slider-thumbdownimage.md)               | 指定或抓取表示 thumb 關閉狀態的影像。                                        |
| [thumbHoverImage](slider-thumbhoverimage.md)             | 指定或抓取將滑鼠停留在其上方時所顯示之捲動方塊的影像。                  |
| [thumbImage](slider-thumbimage.md)                       | 指定或抓取將用來表示滑杆目前位置的影像。               |
| [平鋪](slider-tiled.md)                                 | 指定或抓取值，指出是否要將滑杆影像並排顯示。                                |
| [提示](slider-tooltip.md)                             | 指定或抓取滑杆控制項的工具提示文字。                                                   |
| [transparencyColor](slider-transparencycolor.md)         | 指定或抓取滑杆影像的透明色彩。                                                |
| [useForegroundProgress](slider-useforegroundprogress.md) | 指定或抓取值，指出是否將使用前景進度列。                       |
| [value](slider-value.md)                                 | 指定並抓取滑杆的目前位置。                                                       |



 

**滑杆** 元素可以執行下列事件處理常式。



| 事件處理常式                                   | Description                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [onDragBegin](slider-ondragbegin.md)           | 處理當使用者按一下並按住滑鼠左鍵並開始拖曳滑鼠時所發生的事件。 |
| [onDragEnd](slider-ondragend.md)               | 處理在拖曳作業之後放開滑鼠左鍵時所發生的事件。                      |
| [onPositionChange](slider-onpositionchange.md) | 處理當滑杆的位置由於使用者按一下或拖曳而變更時所發生的事件。   |



 

**滑杆** 元素支援環境屬性，並可執行環境事件處理常式。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

預先定義的滑杆是標準 **滑杆** 元素，預設會指定各種不同的通用屬性設定。 您可以使用下列預先定義的滑杆。



| 預先定義的滑杆                  | Description                                                    |
|------------------------------------|----------------------------------------------------------------|
| [BALANCESLIDER](balanceslider.md) | 用來設定音訊餘額的 **滑杆** 。                        |
| [SEEKSLIDER](seekslider.md)       | 用來搜尋媒體檔案內任何位置的 **滑杆** 。 |
| [VOLUMESLIDER](volumeslider.md)   | 用來設定音訊音量的 **滑杆** 。                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




