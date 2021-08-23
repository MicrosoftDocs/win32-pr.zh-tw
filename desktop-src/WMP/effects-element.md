---
title: 效果元素
description: 效果元素
ms.assetid: ada3c452-1bc6-4700-8048-1a4b2ee00aeb
keywords:
- Windows Media Player 的外觀、效果元素
- 外觀、效果元素
- 效果元素
- 外觀、效果元素的參考
- 元素、效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a859414ffae934cafaa0c35b6b364eb42a5795bbeeef637857a0d81f47623379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651138"
---
# <a name="effects-element"></a>效果元素

**效果** 元素提供使用下列屬性和方法來組織和操作視覺效果的方法。 為了方便起見，也提供預先定義的 **效果** 元素。

**效果** 元素支援下列屬性。



| 屬性                                                        | 描述                                                                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [allowAll](effects-allowall.md)                                 | 指定或抓取值，指出是否要在登錄中包含所有視覺效果。                                                                                                                                                 |
| [currentEffect](effects-currenteffect.md)                       | 指定或抓取目前的視覺效果。                                                                                                                                                                                                    |
| [currentEffectPresetCount](effects-currenteffectpresetcount.md) | 抓取目前視覺效果的可用預設數目。                                                                                                                                                                                 |
| [currentEffectTitle](effects-currenteffecttitle.md)             | 抓取目前視覺效果的顯示標題。                                                                                                                                                                                            |
| [currentEffectType](effects-currenteffecttype.md)               | 抓取目前視覺效果的登錄名稱。                                                                                                                                                                                            |
| [currentPreset](effects-currentpreset.md)                       | 指定或抓取目前視覺效果目前的預設值。                                                                                                                                                                              |
| [currentPresetTitle](effects-currentpresettitle.md)             | 抓取目前視覺效果目前預設值的標題。                                                                                                                                                                              |
| [effectCanGoFullScreen](effects-effectcangofullscreen.md)       | 抓取值，指出目前的視覺效果是否可以全螢幕顯示。                                                                                                                                                         |
| [effectCount](effects-effectcount.md)                           | 抓取可用視覺效果的數目。                                                                                                                                                                                                    |
| [effectHasPropertyPage](effects-effecthaspropertypage.md)       | 抓取值，指出目前的視覺效果是否有屬性頁。                                                                                                                                                                  |
| [全屏](effects-fullscreen.md)                             | 指定或抓取值，指出目前的視覺效果是否以全螢幕顯示。 只有在執行時間才可設定。                                                                                                                   |
| [視窗](effects-windowed.md)                                 | 指定或抓取值，指出視覺效果是否為視窗化或無視窗，也就是控制項的整個矩形是否會在任何時間顯示，或是是否可以裁剪。 只能在設計階段設定。 |



 

**效果** 元素支援下列方法。



| 方法                                       | 描述                                                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [effectTitle](effects-effecttitle.md)       | 使用指定的登錄索引來抓取視覺效果的易記名稱。                               |
| [>effecttype](effects-effecttype.md)         | 使用指定的登錄索引來抓取視覺效果的登錄名稱。                               |
| [下一步](effects-next.md)                     | 顯示下一個視覺效果預設值，視需要移至下一個視覺效果。                            |
| [nextEffect](effects-nexteffect.md)         | 顯示下一個視覺效果的第一個預設值，略過中間的預設值。                                |
| [nextPreset](effects-nextpreset.md)         | 顯示目前視覺效果的下一個預設值。                                                            |
| [previous](effects-previous.md)             | 顯示先前的視覺效果預設值，視需要移至先前視覺效果的最後一個預設值。 |
| [previousEffect](effects-previouseffect.md) | 顯示先前的視覺效果，略過預設值。                                                            |
| [previousPreset](effects-previouspreset.md) | 顯示目前視覺效果的先前預設值。                                                        |
| [設定](effects-settings.md)             | 顯示目前視覺效果的屬性頁面（如果有的話）。                                            |



 

**效果** 元素支援環境屬性，並可執行環境事件處理常式。 如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。

預先定義的效果是標準 **效果** 元素，預設會指定各種不同的屬性設定。 以下是可用的預先定義效果。



| 預先定義的效果           | 描述                                                         |
|------------------------------|---------------------------------------------------------------------|
| [WMPEFFECTS](wmpeffects.md) | 逐一查看可用效果的 **效果** 元素。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




