---
title: LISTBOX. getNextSelectedItem
description: GetNextSelectedItem 方法會從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982598"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. getNextSelectedItem

**GetNextSelectedItem** 方法會從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Number** (**Long**) ，其中包含要抓取之專案之前的專案索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**Long**) ，其中包含下一個選取專案的索引。

## <a name="remarks"></a>備註

若要從頭開始搜尋，請使用1作為開始索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> </dl>

 

 





