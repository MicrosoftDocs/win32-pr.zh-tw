---
title: VIEW 元素
description: VIEW 元素
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player 的外觀、VIEW 元素
- 外觀，VIEW 元素
- VIEW 元素
- 外觀的參考、VIEW 元素
- 元素、VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372316"
---
# <a name="view-element"></a>VIEW 元素

**VIEW** 元素包含面板的使用者介面詳細資料，並使用下表所示的屬性、方法和事件處理常式。

您可以將多個 **VIEW** 專案定義為面板 **主題** 專案的子系，以針對不同的情況提供不同的介面。 **VIEW** 元素不能指定為任何其他專案的子系，而且它們包含所有其他的面板元素。 請注意，每個視圖都有自己的變數範圍，這表示它無法與其他視圖共用屬性值。

**View** global 屬性可以用來從它內部的任何位置參考特定的 **view** 元素。 這是使用其 **id** 屬性的替代方案，必須從其他 **VIEW** 專案或 **主題** 專案內使用。

**VIEW** 元素支援下列屬性。 子視圖專案也支援標記有星號 (\*) 的屬性 。



| 屬性                                                       | 描述                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)\*                  | 指定或抓取 **視圖** 或 **子視圖的背景色彩。**                                             |
| [backgroundImage](view-backgroundimage.md) \*                  | 指定或抓取 **視圖** 或 **子視圖的背景影像。**                                             |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | 指定或抓取背景影像色調的位移量。                                  |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | 指定或抓取背景影像的飽和度值。                                                    |
| [backgroundTiled](view-backgroundtiled.md)\*                  | 指定或抓取值，指出 **視圖** 或子視圖的背景 **影像是否已** 平鋪。         |
| [類別](view-category.md)                                   | 指定或抓取將顯示使用者介面的分類。                                           |
| [focusObjectID](view-focusobjectid.md)                         | 指定或抓取值，指出哪個元素具有鍵盤焦點。                                             |
| [maxHeight](view-maxheight.md)                                 | 當調整大小時，指定或抓取 **視圖** 的最大高度。                                                |
| [maxWidth](view-maxwidth.md)                                   | 當調整大小時，指定或抓取 **視圖** 的最大寬度。                                                 |
| [minHeight](view-minheight.md)                                 | 在調整大小時，指定或抓取 **視圖** 的最小高度。                                                |
| [minWidth](view-minwidth.md)                                   | 當調整大小時，指定或抓取 **視圖** 的寬度下限。                                                 |
| [小時](view-resizable.md)                                 | 指定或抓取值，指出是否可以調整 **視圖** 的大小。                                          |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | 指定或抓取值，指出背景影像是否可以調整大小。                                  |
| [scriptFile](view-scriptfile.md)                               | 指定隨附之 JScript 檔案的檔案名。                                                                 |
| [timerInterval](view-timerinterval.md)                         | 指定或抓取計時器引發事件至 **ontimer** 事件處理常式的間隔（以毫秒為單位）。 |
| [title](view-title.md)                                         | 指定或抓取 **視圖** 的標題。 只能在設計階段設定。                                       |
| [標題列](view-titlebar.md)                                   | 指定或抓取值，指出是否顯示視窗標題列。                                        |
| [transparencyColor](view-transparencycolor.md)\*              | 指定或抓取背景影像的透明色彩。                                                  |



 

**VIEW** 元素支援下列方法。



| 方法                                              | 描述                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [close](view-close.md)                             | 關閉 **VIEW**。                                       |
| [最大化](view-maximize.md)                       | 將 **視圖** 最大化。                                    |
| [最小 化](view-minimize.md)                       | 將 **視圖** 降至最低。                                    |
| [restore](view-restore.md)                         | 還原 **視圖**。                                     |
| [returnToMediaCenter](view-returntomediacenter.md) | 將使用者返回 Windows Media Player 的完整模式。 |
| [size](view-size.md)                               | 調整指定邊緣的 **視圖** 大小。                  |



 

**VIEW** 元素可以執行下列事件處理常式。



| 事件處理常式               | Description                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [onclose](view-onclose.md) | 處理 **視圖** 即將關閉時所發生的事件。      |
| [onerror](view-onerror.md) | 如果設定 **. enableErrorDialogs** 設定為 false，則會處理錯誤事件。 |
| [onload](view-onload.md)   | 處理第一次顯示 **視圖** 時所發生的事件。         |
| [ontimer](view-ontimer.md) | 處理計時器事件。                                                      |



 

**VIEW** 元素支援環境屬性，而且可以執行環境事件處理常式（除非有注明）。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




