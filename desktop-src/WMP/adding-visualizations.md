---
title: 新增視覺效果
description: 新增視覺效果
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- 建立外觀、視覺效果
- Windows Media Player 的外觀、視覺效果
- 外觀、視覺效果
- 視覺效果，外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673391"
---
# <a name="adding-visualizations"></a>新增視覺效果

您可以使用新增影片視窗的相同方式來新增視覺效果視窗。 您可以使用相同的面板，但會使用 **效果** 元素。

首先，您必須新增 **效果** 元素，並為其指定識別碼和大小：


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



然後，您可以為先前和下一個視覺效果程式碼字串指派兩個按鈕：


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



圖層和點陣圖與影片範例中所用的圖層和點陣圖相同，不同之處在于會以水準方式複製和翻轉播放箭號。

最後，新增了具有 **URL** 屬性的簡單 **播放機** 元素，以選擇要播放的歌曲。


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



您可以在 SDK 的範例區段中看到類似的工作視覺效果外觀。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀建立指南**](skin-creation-guide.md)
</dt> </dl>

 

 




