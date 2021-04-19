---
title: ScrollingAmount
description: ScrollingAmount 屬性會指定或抓取文字在每個滾動移動期間移動的圖元數。
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- ScrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989623"
---
# <a name="textscrollingamount"></a>ScrollingAmount

**ScrollingAmount** 屬性會指定或抓取文字在每個滾動移動期間移動的圖元數。

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**int**) 的正數讀/寫 **數位**，預設值是6。

## <a name="remarks"></a>備註

若要順暢地滾動， **scrollingAmount** 應該很小。 針對具有顯著間距的快速繪圖， **scrollingAmount** 應該更大。 如果 **滾動** = "false"，則會忽略 **scrollingAmount** 。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**文字。滾動**](text-scrolling.md)
</dt> </dl>

 

 





