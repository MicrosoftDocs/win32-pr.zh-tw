---
title: 編輯方塊. replaceSelection
description: ReplaceSelection 方法會以指定的文字取代目前的選取範圍。
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- 編輯方塊. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997676"
---
# <a name="editboxreplaceselection"></a>編輯方塊. replaceSelection

**ReplaceSelection** 方法會以指定的文字取代目前的選取範圍。

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**字串** ，包含要取代所選取文字的文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果未選取任何文字，則會將取代文字插入插入點的目前位置。

只有在控制項變成可見之後，才能呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> <dt>

[**編輯方塊. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**編輯方塊. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**編輯方塊. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





