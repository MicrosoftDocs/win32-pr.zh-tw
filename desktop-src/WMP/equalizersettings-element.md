---
title: EQUALIZERSETTINGS 元素
description: EQUALIZERSETTINGS 元素
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Windows Media Player 的 EQUALIZERSETTINGS 元素
- 外觀，EQUALIZERSETTINGS 元素
- EQUALIZERSETTINGS 元素
- EQUALIZERSETTINGS 元素的外觀參考
- 元素，EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: facd5d9630536947614166bc8444ad38e33020920ce679180824ef9a3b007bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650948"
---
# <a name="equalizersettings-element"></a>EQUALIZERSETTINGS 元素

**EQUALIZERSETTINGS** 元素會使用此處所列的屬性和方法，提供管理 Windows Media Player 的圖形等化器和其他音訊設定的方式。

**EQUALIZERSETTINGS** 元素支援下列屬性。



| 屬性                                                          | 描述                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [寬線](equalizersettings-bands.md)                               | 抓取支援的頻率區段數目。                                                      |
| [旁路](equalizersettings-bypass.md)                             | 指定或抓取值，指出是否略過篩選圖形中的等化器篩選。 |
| [crossFade](equalizersettings-crossfade.md)                       | 指定或抓取值，指出是否已啟用交叉淡化。                                |
| [crossFadeWindow](equalizersettings-crossfadewindow.md)           | 指定或抓取交叉淡化重迭量（以毫秒為單位）。                                |
| [currentPreset](equalizersettings-currentpreset.md)               | 指定或抓取目前預設值的索引。                                                 |
| [currentPresetTitle](equalizersettings-currentpresettitle.md)     | 抓取目前預設值的標題。                                                              |
| [currentSpeakerName](equalizersettings-currentspeakername.md)     | 抓取目前說話者設定的名稱。                                                      |
| [enableSplineTension](equalizersettings-enablesplinetension.md)   | 指定或抓取值，指出是否已啟用或停用曲線張力。                |
| [enhancedAudio](equalizersettings-enhancedaudio.md)               | 指定或抓取指出增強音訊是否已開啟的值。                          |
| [gainLevels](equalizersettings-gainlevels.md)                     | 指定或抓取對應于所提供之索引的帶狀增益層級。                  |
| [gainLevel1](equalizersettings-gainlevel1.md)                     | 指定或抓取寬線1的增益層級。                                                        |
| [gainLevel2](equalizersettings-gainlevel2.md)                     | 指定或抓取寬線2的增益層級。                                                        |
| [gainLevel3](equalizersettings-gainlevel3.md)                     | 指定或抓取寬線3的增益層級。                                                        |
| [gainLevel4](equalizersettings-gainlevel4.md)                     | 指定或抓取寬線4的增益層級。                                                        |
| [gainLevel5](equalizersettings-gainlevel5.md)                     | 指定或抓取寬線5的增益層級。                                                        |
| [gainLevel6](equalizersettings-gainlevel6.md)                     | 指定或抓取寬線6的增益層級。                                                        |
| [gainLevel7](equalizersettings-gainlevel7.md)                     | 指定或抓取帶狀7的增益等級。                                                        |
| [gainLevel8](equalizersettings-gainlevel8.md)                     | 指定或抓取寬線8的增益層級。                                                        |
| [gainLevel9](equalizersettings-gainlevel9.md)                     | 指定或抓取寬線9的增益層級。                                                        |
| [gainLevel10](equalizersettings-gainlevel10.md)                   | 指定或抓取帶狀10的增益層級。                                                       |
| [正常化](equalizersettings-normalization.md)               | 指定或抓取表示正規化是否已啟用的值。                             |
| [normalizationAverage](equalizersettings-normalizationaverage.md) | 抓取平均正規化值。                                                              |
| [normalizationPeak](equalizersettings-normalizationpeak.md)       | 抓取尖峰標準化值。                                                                 |
| [presetCount](equalizersettings-presetcount.md)                   | 抓取可用的預設數目。                                                              |
| [speakerSize](equalizersettings-speakersize.md)                   | 指定或抓取目前說話者大小的索引。                                           |
| [splineTension](equalizersettings-splinetension.md)               | 指定或抓取等化器控制項的曲線張力。                                    |
| [truBassLevel](equalizersettings-trubasslevel.md)                 | 指定或抓取 SRS TruBass 層級。                                                           |
| [wowLevel](equalizersettings-wowlevel.md)                         | 指定或抓取 SRS WOW 效果等級。                                                        |



 

**EQUALIZERSETTINGS** 元素支援下列方法。



| 方法                                                 | 描述                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [nextPreset](equalizersettings-nextpreset.md)         | 套用下一個等化器預設值。                                   |
| [presetTitle](equalizersettings-presettitle.md)       | 使用指定的索引，抓取等化器預設值的名稱。 |
| [previousPreset](equalizersettings-previouspreset.md) | 套用先前的等化器預設值。                               |
| [reset](equalizersettings-reset.md)                   | 將所有波段的增益層級重設為零分貝。                |



 

**EQUALIZERSETTINGS** 元素可以執行 [屬性 \_ onchange](attribute-onchange.md)事件處理常式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀程式設計參考**](skin-programming-reference.md)
</dt> </dl>

 

 




