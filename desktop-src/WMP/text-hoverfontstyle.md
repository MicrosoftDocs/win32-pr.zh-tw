---
title: HoverFontStyle
description: 當滑鼠游標停留在文字控制項上方時，hoverFontStyle 屬性會指定或抓取文字控制項所使用的字型樣式。
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- HoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04f2ae8e4231ca89f37a65e591271f2536679da649d1efd22ffc1063c89d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134621"
---
# <a name="texthoverfontstyle"></a>HoverFontStyle

當滑鼠游標停留在文字控制項上方時， **hoverFontStyle** 屬性會指定或抓取文字控制項所使用的字型樣式。

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a>可能的值

這個屬性是包含下列一或多個值的讀取/寫入 **字串** 。



| 值     | 描述           |
|-----------|-----------------------|
| 粗體      | 粗體字型樣式。      |
| 斜體    | 斜體字型樣式。    |
| Underline | 底線字型樣式。 |
| 帶 | 刪除線字型樣式。 |
| 正常    | 一般字型樣式。    |



 

## <a name="remarks"></a>備註

您可以使用值的任何組合，並以空格分隔。 標準樣式的優先順序會高於所有其他值，而且會忽略任何其他指定的標準。

如果未指定 **hoverFontStyle** ，則會使用 **fontStyle** 。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**FontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





