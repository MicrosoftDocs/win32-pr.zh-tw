---
title: 文字。工具提示
description: ToolTip 屬性會指定或抓取文字控制項的工具提示文字。
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- 文字。工具提示 Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 726337ffb31b86d4eaa3a20a1d922fc622110b647fe9be747e8ae239c4548276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831817"
---
# <a name="texttooltip"></a>文字。工具提示

**Tooltip** 屬性會指定或抓取文字控制項的工具提示文字。

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串** ，最大長度為1024個字元。 它沒有預設值。

## <a name="remarks"></a>備註

如果未指定這個屬性，而且 **值** 屬性中的文字在文字控制項中被截斷，或 **wordWrap** 設定為 True，則工具提示會顯示 **值** 屬性的全文檢索。

當這個屬性設定為 "" (空白字串) 時，不會顯示任何工具提示。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**TEXT。值**](text-value.md)
</dt> <dt>

[**WordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





