---
title: VIEW. 可調整大小
description: 可調整大小的屬性會抓取值，指出是否可以調整視圖的大小。
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW. 可調整大小的 Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622c732ce6a1218fa16bbe70c1ef18d53ba4211abfde9d39fc794ec862348033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332906"
---
# <a name="viewresizable"></a>VIEW. 可調整大小

可重設 **大小** 的屬性會抓取值，指出是否可以調整 **視圖** 的大小。

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林** 值，預設值等於 **標題列** 屬性。



| 值 | 描述             |
|--------|-------------------------|
| true   | 您可以調整 View 的大小。    |
| false  | 無法調整 View 的大小。 |



 

## <a name="remarks"></a>備註

如果沒有 **標題列**，因此沒有視窗或框線，您必須使用 **size** 方法來調整 **VIEW** 元素的大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> </dl>

 

 





