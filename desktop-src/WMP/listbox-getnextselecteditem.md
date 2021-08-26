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
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003398"
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
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> </dl>

 

 





