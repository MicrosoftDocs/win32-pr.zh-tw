---
title: 編輯方塊. setSelection
description: SetSelection 方法會從指定的開始索引到指定的結束索引，選取編輯方塊控制項中的文字。
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- 編輯方塊. setSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000710"
---
# <a name="editboxsetselection"></a>編輯方塊. setSelection

**SetSelection** 方法會從指定的開始索引到指定的結束索引，選取編輯方塊控制項中的文字。

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="start"></span><span id="START"></span>*開始*
</dt> <dd>

**Number** (**Long**) ，其中包含所選取文字之開始位置的字元索引。

</dd> <dt>

<span id="end"></span><span id="END"></span>*結束*
</dt> <dd>

**Number** (**Long**) ，其中包含所選取文字結束位置的字元索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 [開始] 為0且結尾是1，則會選取 [編輯方塊] 控制項中的所有文字。 如果啟動是1，則會取消選取任何目前的選取範圍。

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

[**編輯方塊. replaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





