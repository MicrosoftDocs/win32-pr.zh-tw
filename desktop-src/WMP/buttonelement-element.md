---
title: BUTTONELEMENT 元素
description: BUTTONELEMENT 元素
ms.assetid: 2c1bac51-8aea-4c73-b9b4-4ddbf1e4231b
keywords:
- Windows Media Player 的 BUTTONELEMENT 元素
- 外觀，BUTTONELEMENT 元素
- BUTTONELEMENT 元素
- BUTTONELEMENT 元素的外觀參考
- 元素，BUTTONELEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4cc69154821981874f0072f6282f708cc4826d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674151"
---
# <a name="buttonelement-element"></a>BUTTONELEMENT 元素

**BUTTONELEMENT** 元素會定義父 **BUTTONGROUP** 元素內的單一按鈕。 它支援下列屬性。 為了方便起見，也提供預先定義的 **BUTTONELEMENT** 元素。

**BUTTONELEMENT** 元素支援下列屬性。



| 屬性                                      | 描述                                                                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [cursor](buttonelement-cursor.md)             | 指定或抓取當滑鼠停留在 **BUTTONELEMENT** 上時，所顯示之 **BUTTONELEMENT** 游標的值。                                                                                      |
| [分解](buttonelement-down.md)                 | 指定或抓取 **BUTTONELEMENT** 的向上或向下值。                                                                                                                                            |
| [downToolTip](buttonelement-downtooltip.md)   | 指定或抓取當滑鼠停留在 **BUTTONELEMENT** 上，且 **BUTTONELEMENT** 處於關閉狀態時，所顯示的工具提示文字。                                                                |
| [index](buttonelement-index.md)               | 捕獲 **BUTTONGROUP** 內 **BUTTONELEMENT** 的索引。                                                                                                                                         |
| [mappingColor](buttonelement-mappingcolor.md) | 指定或抓取在 **BUTTONELEMENT** 群組中識別此 **BUTTONELEMENT** 的色彩索引鍵。                                                                                                      |
| [粘](buttonelement-sticky.md)             | 指定或抓取值，指出 **BUTTONELEMENT** 是否為粘滯。 當您按一下時， **BUTTONELEMENT** 會在按下後變更狀態，並會維持在新狀態，直到再次按一下為止。 |
| [upToolTip](buttonelement-uptooltip.md)       | 指定或抓取當滑鼠停留在 **BUTTONELEMENT** 上，且 **BUTTONELEMENT** 處於啟動或使用中狀態時，所顯示的工具提示文字。                                                        |



 

**BUTTONELEMENT** 元素支援下列方法。



| 方法                           | 描述                                                            |
|----------------------------------|------------------------------------------------------------------------|
| [點擊](buttonelement-click.md) | 呼叫針對 **BUTTONELEMENT** 所定義的 **onclick** 事件處理常式。 |



 

**BUTTONELEMENT** 元素可以執行環境事件處理常式。 如需詳細資訊，請參閱 [環境事件處理常式](ambient-event-handlers.md)。

**BUTTONELEMENT** 元素支援下列環境屬性： [enabled](ambientattributes-enabled.md)和 [tabStop](ambientattributes-tabstop.md)。

預先定義的效果是標準 **效果** 元素，預設會指定各種不同的屬性設定。 以下是可用的預先定義 **BUTTONELEMENT** 元素。



| 預先定義的 BUTTONELEMENT         | Description                                                                                               |
|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| [FFWDELEMENT](ffwdelement.md)   | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，可呼叫 **fastForward**。 |
| [NEXTELEMENT](nextelement.md)   | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，此處理程式會呼叫 **player。接下來**。        |
| [PAUSEELEMENT](pauseelement.md) | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，此處理程式會呼叫 **player。 pause**。       |
| [PLAYELEMENT](playerelement.md) | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，此處理程式會呼叫 **播放機。**        |
| [PREVELEMENT](prevelement.md)   | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，可呼叫 **player**。    |
| [REWELEMENT](rewelement.md)     | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，可呼叫 **player**。      |
| [STOPELEMENT](stopelement.md)   | 具有內建 **onclick** 事件處理常式的 **BUTTONELEMENT** ，此處理程式會呼叫 **player。**        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




