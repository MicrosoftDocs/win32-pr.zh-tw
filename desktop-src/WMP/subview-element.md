---
title: 子視圖元素
description: 子視圖元素
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Windows Media Player 的外觀、子視圖元素
- 外觀，子視圖元素
- 子視圖元素
- 外觀的參考、子視圖元素
- 元素、子視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef4f7860d1db04991a35ffeff2903e7a16a5d7bd84929313c296006f6f1c092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122908"
---
# <a name="subview-element"></a>子視圖元素

[子 **視圖** ] 元素提供操作面板部分的方式，例如，提供在未使用時可以隱藏的 [控制台]。 子視圖 **元素一律** 是父 **VIEW** 專案的子系，而且可以包含其他面板元素，但 **VIEW**、**主題** 和 **其他子視圖專案** 除外。

子 **視圖元素支援** 下列屬性，這些屬性定義于 **VIEW** 元素之下。



| 屬性                                                       | 描述                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)                     | 指定或抓取子 **視圖** 控制項的背景色彩。 預設值為 "none"。        |
| [backgroundImage](view-backgroundimage.md)                     | 指定或抓取子 **視圖** 控制項的背景影像。                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | 指定或抓取背景影像色調的位移量。                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | 指定或抓取背景影像的飽和度值。                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | 指定或抓取值，指出是否將子 **視圖** 控制項的背景影像並排顯示。 |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | 指定或抓取值，指出背景影像是否可以調整大小。                      |
| [transparencyColor](view-transparencycolor.md)                 | 指定或抓取背景影像的透明色彩。                                      |



 

除非有注明，否則 [子 **視圖** ] 元素支援環境屬性。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md)。

子 **視圖** 專案可以執行下列環境事件處理常式： [onendmove](onendmove.md) 和 [onresize](onresize.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> <dt>

[**VIEW 元素**](view-element.md)
</dt> </dl>

 

 




