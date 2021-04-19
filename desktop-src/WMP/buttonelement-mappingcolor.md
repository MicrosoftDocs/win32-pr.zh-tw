---
title: BUTTONELEMENT.mappingColor
description: MappingColor 屬性會指定或抓取在 BUTTONGROUP 中識別此 BUTTONELEMENT 的色彩索引鍵。
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988668"
---
# <a name="buttonelementmappingcolor"></a>BUTTONELEMENT.mappingColor

**MappingColor** 屬性會指定或抓取在 **BUTTONGROUP** 中識別此 **BUTTONELEMENT** 的色彩索引鍵。

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。 它沒有預設值。

## <a name="remarks"></a>備註

這個屬性會指定按鈕群組 **mappingImage** 中對應于這個 button 元素的區域色彩。 此按鈕元素會處理此區域的所有點擊。

如果指定的色彩無效，則不會啟用 **BUTTONELEMENT** 。

## <a name="examples"></a>範例

下列範例是完整的面板定義檔，說明如何使用一些 **BUTTONELEMENT** 屬性。 您可以在與 SDK 一起安裝的範例目錄中找到它。


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**色彩參考**](color-reference.md)
</dt> <dt>

[**BUTTONELEMENT 元素**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





