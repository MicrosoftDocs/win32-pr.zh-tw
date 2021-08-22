---
title: LISTBOX. findItem
description: FindItem 方法會從指定的專案索引後面的專案開始，搜尋指定的字串。
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3625c8d8e9993d09e7b5b41911ead8df857c257a7a2354d71c8d81c1fecc645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135321"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

**FindItem** 方法會從指定的專案索引後面的專案開始，搜尋指定的字串。

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Number** (**Long**) ，其中包含要開始搜尋之專案的索引。

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

包含要搜尋之文字的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**Long**) ，其中包含包含字串之專案的索引。

## <a name="remarks"></a>備註

若要在清單方塊控制項的第一行開始搜尋，請使用1做為 *startIndex*。 若要在找到第一行之後繼續搜尋文字，請使用傳回的行索引作為 *startIndex*，然後搜尋將從下一行開始。 這個方法會搜尋子字串，且不區分大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> </dl>

 

 





