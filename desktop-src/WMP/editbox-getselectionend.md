---
title: 編輯方塊. getSelectionEnd
description: GetSelectionEnd 方法會抓取編輯方塊控制項中所選取文字的結束位置。
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- 編輯方塊. getSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001230"
---
# <a name="editboxgetselectionend"></a>編輯方塊. getSelectionEnd

**GetSelectionEnd** 方法會抓取編輯方塊控制項中所選取文字的結束位置。

``` syntax
        elementID.getSelectionEnd()
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

[**編輯方塊. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**編輯方塊. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**編輯方塊. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





