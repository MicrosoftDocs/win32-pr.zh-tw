---
title: 編輯方塊. fontStyle
description: FontStyle 屬性會指定或抓取編輯方塊控制項的字型樣式。
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- 編輯方塊. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986177"
---
# <a name="editboxfontstyle"></a>編輯方塊. fontStyle

**FontStyle** 屬性會指定或抓取編輯方塊控制項的字型樣式。

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
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> <dt>

[**編輯方塊. fontFace**](editbox-fontface.md)
</dt> <dt>

[**編輯方塊. fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





