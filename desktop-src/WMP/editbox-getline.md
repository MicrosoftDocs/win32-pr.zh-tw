---
title: 編輯方塊. getLine
description: GetLine 方法會使用指定的索引來抓取行的文字。
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- 編輯方塊. getLine Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 28d555cb684fa849b5fc7cdb42ebaf0ab4fb278b4ef126845add2f12ddf59948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578834"
---
# <a name="editboxgetline"></a>編輯方塊. getLine

**GetLine** 方法會使用指定的索引來抓取行的文字。

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

包含要取出的行之索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

如果索引無效，則會傳回空字串。 只有在控制項變成可見之後，才能呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> <dt>

[**編輯方塊. getLineFromChar**](editbox-getlinefromchar.md)
</dt> <dt>

[**編輯方塊. getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





