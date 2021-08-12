---
title: LISTBOX. fontStyle
description: FontStyle 屬性會指定或抓取清單方塊控制項的字型樣式。
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575035"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

**FontStyle** 屬性會指定或抓取清單方塊控制項的字型樣式。

``` syntax
        elementID.fontStyle
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

基於轉譯目的，Normal 是預設字型樣式。 從此屬性抓取的預設值為 "" (空白字串) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> <dt>

[**LISTBOX. fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





