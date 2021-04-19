---
title: 編輯方塊. getLineIndex
description: GetLineIndex 方法會使用指定的行索引，來抓取行第一個字元的字元索引。
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- 編輯方塊. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996111"
---
# <a name="editboxgetlineindex"></a>編輯方塊. getLineIndex

**GetLineIndex** 方法會使用指定的行索引，來抓取行第一個字元的字元索引。

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

**Number** (**Long**) ，其中包含要抓取其字元索引的行索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果指定的行索引是1，則會使用包含插入點的行。

只有在控制項變成可見之後，才能呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------|
| 版本<br/> | 適用于 Windows XP 或更新版本的 Windows Media Player<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**編輯方塊元素**](editbox-element.md)
</dt> <dt>

[**編輯方塊. getLine**](editbox-getline.md)
</dt> <dt>

[**編輯方塊. getLineFromChar**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





