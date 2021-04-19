---
title: LISTBOX. insertItem
description: InsertItem 方法會將指定的文字插入清單方塊控制項中的指定索引處。
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX. insertItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981626"
---
# <a name="listboxinsertitem"></a>LISTBOX. insertItem

**InsertItem** 方法會將指定的文字插入清單方塊控制項中的指定索引處。

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

包含要取出的行之索引的 (**長**) **數目**。

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

包含要插入之文字的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

插入線條時，插入行下方行的行索引會增加1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LISTBOX 元素**](listbox-element.md)
</dt> </dl>

 

 





