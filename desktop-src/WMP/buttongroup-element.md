---
title: BUTTONGROUP 元素
description: BUTTONGROUP 元素
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Windows Media Player 的 BUTTONGROUP 元素
- 外觀，BUTTONGROUP 元素
- BUTTONGROUP 元素
- BUTTONGROUP 元素的外觀參考
- 元素，BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092307"
---
# <a name="buttongroup-element"></a>BUTTONGROUP 元素

**BUTTONGROUP** 元素提供將面板中的數個按鈕分組的方式。 您可以使用 **BUTTONELEMENT** 專案做為 **BUTTONGROUP** 元素的子系，以指定這些按鈕。

**BUTTONGROUP** 元素支援下列屬性。



| 屬性                                              | 描述                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [buttonCount](buttongroup-buttoncount.md)             | 捕獲 **BUTTONGROUP** 中的按鈕數目。                                                                                                                                                                         |
| [cursor](buttongroup-cursor.md)                       | 指定或抓取當滑鼠停留在 **BUTTONGROUP** 中的按鈕上時，所顯示的游標類型。                                                                                                                  |
| [disabledImage](buttongroup-disabledimage.md)         | 指定或抓取表示 **BUTTONGROUP** 中按鈕已停用狀態之影像的名稱。                                                                                                             |
| [downImage](buttongroup-downimage.md)                 | 指定或抓取表示 **BUTTONGROUP** 關閉狀態之影像的名稱。                                                                                                                                |
| [hoverDownImage](buttongroup-hoverdownimage.md)       | 指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫止狀態。 當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。 |
| [hoverImage](buttongroup-hoverimage.md)               | 指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫留狀態。 當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。             |
| [hueShift](buttongroup-hueshift.md)                   | 指定或抓取 **BUTTONGROUP** 影像色調的位移量。                                                                                                                                    |
| [image](buttongroup-image.md)                         | 指定或抓取表示 **BUTTONGROUP** 按鈕的影像名稱。                                                                                                                                     |
| [mappingImage](buttongroup-mappingimage.md)           | 指定或抓取表示 **BUTTONGROUP** 按鈕對應的影像名稱。                                                                                                                                |
| [radio](buttongroup-radio.md)                         | 指定或抓取值，指出 **BUTTONGROUP** 是否包含選項按鈕。                                                                                                                             |
| [飽和](buttongroup-saturation.md)               | 指定或抓取 **BUTTONGROUP** 影像的飽和度值。                                                                                                                                                      |
| [showBackground](buttongroup-showbackground.md)       | 指定或抓取值，指出 **BUTTONGROUP** 是否只會顯示按鈕，或顯示 **影像** 屬性中指定的完整點陣圖。                                                              |
| [transparencyColor](buttongroup-transparencycolor.md) | 指定或抓取 **BUTTONGROUP** 影像的透明色彩。                                                                                                                                                     |



 

**BUTTONGROUP** 元素支援下列方法。



| 方法                                 | 描述                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [點擊](buttongroup-click.md)         | 使用指定的索引，呼叫針對 **BUTTONELEMENT** 所定義的 **onclick** 事件處理常式。 |
| [getButton](buttongroup-getbutton.md) | 使用指定的索引來抓取 **BUTTONELEMENT** 。                                       |



 

**BUTTONGROUP** 元素支援環境屬性，並可執行環境事件處理常式。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




