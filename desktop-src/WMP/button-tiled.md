---
title: 按鈕。磚
description: 並排顯示的屬性會指定或抓取值，指出是否將按鈕影像並排顯示。
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- 按鈕。磚 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f4f1dda0b5a79749cfbffaa30f29522ff318a763ad50fcd005479afa9c8997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581372"
---
# <a name="buttontiled"></a>按鈕。磚

並排顯示 **的屬性會** 指定或抓取值，指出是否將 **按鈕** 影像並排顯示。

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                       |
|-------|-----------------------------------|
| true  | 影像將會並排顯示。              |
| false | 預設值。 影像將不會並排顯示。 |



 

## <a name="remarks"></a>備註

如果影像小於控制項的實際區域，則平鋪影像將會重複，直到填滿整個區域為止。 如果未指定或無法抓取影像，則會將 **磚** 設定為 false。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕。影像**](button-image.md)
</dt> </dl>

 

 





