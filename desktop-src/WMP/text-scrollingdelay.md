---
title: ScrollingDelay
description: ScrollingDelay 屬性會指定或抓取滾動移動之間的時間延遲。
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- ScrollingDelay Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987142"
---
# <a name="textscrollingdelay"></a>ScrollingDelay

**ScrollingDelay** 屬性會指定或抓取滾動移動之間的時間延遲。

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**int**) 指定延遲（以毫秒為單位）。 其最小值為30，預設值為85。 如果指定的值小於最小值，則會使用預設值。

## <a name="remarks"></a>備註

如果 [ **滾動** ] 設定為 [false]，則會忽略 **scrollingDelay** 。

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

 

 





