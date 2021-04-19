---
title: 編輯方塊. getLineFromChar
description: GetLineFromChar 方法會抓取指定字元索引的行索引。
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- 編輯方塊. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000488"
---
# <a name="editboxgetlinefromchar"></a>編輯方塊. getLineFromChar

**GetLineFromChar** 方法會抓取指定字元索引的行索引。

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*指數*
</dt> <dd>

**Number** (**Long**) ，其中包含要抓取其行索引的字元索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果指定的字元位置是1，這個方法會抓取目前行的行索引。

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

[**編輯方塊. getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





