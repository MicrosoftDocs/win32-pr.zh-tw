---
title: 編輯方塊. getSelectionStart
description: GetSelectionStart 方法會抓取編輯方塊控制項中所選取文字的開始位置。
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- 編輯方塊. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001634"
---
# <a name="editboxgetselectionstart"></a>編輯方塊. getSelectionStart

**GetSelectionStart** 方法會抓取編輯方塊控制項中所選取文字的開始位置。

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果未選取任何文字，這個方法會傳回插入點的位置。

如果控制項是多行，此方法會傳回控制項中的字元索引，而不是行索引。

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

[**編輯方塊. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**編輯方塊. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





