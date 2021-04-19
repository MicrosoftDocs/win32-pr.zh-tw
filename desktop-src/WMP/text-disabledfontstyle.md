---
title: DisabledFontStyle
description: DisabledFontStyle 屬性會指定或抓取文字控制項停用時所用的字型樣式。
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- DisabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998880"
---
# <a name="textdisabledfontstyle"></a>DisabledFontStyle

**DisabledFontStyle** 屬性會指定或抓取文字控制項停用時所用的字型樣式。

``` syntax
        elementID.disabledFontStyle
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

如果未指定 **disabledFontStyle** ，則會使用 **fontStyle** 。

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

 

 





