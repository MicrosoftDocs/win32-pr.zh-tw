---
title: TEXT。值
description: Value 屬性會指定或抓取文字控制項中顯示的文字。
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT. value Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998793"
---
# <a name="textvalue"></a>TEXT。值

**Value** 屬性會指定或抓取文字控制項中顯示的文字。

``` syntax
        elementID.value
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

如果文字控制項的寬度不足以包含提供的文字，則會裁剪文字，並顯示省略號來說明事實。 如果尚未設定 **工具提示** 屬性，則在游標停留在控制項上時，完整文字會顯示為工具提示。

如果未指定寬度，控制項的預設寬度就是字串的寬度。

如果未指定控制項的高度，則預設高度為一行。

如果 [ **wordWrap** ] 屬性設定為 [true]，而且控制項的高度足以容納另一行文字，則文字會換行至後續的行。 只會在文字之間進行換行。 也可以強制換行，如 **wordWrap** 中所述。

## <a name="examples"></a>範例

下列範例是完整的面板定義檔，說明如何使用 **TEXT** 專案的屬性。 您可以在與 SDK 一起安裝的範例目錄中找到它。


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**文字。工具提示**](text-tooltip.md)
</dt> <dt>

[**WordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





