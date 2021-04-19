---
title: BUTTONELEMENT。
description: 「粘滯」屬性（attribute）會指定或抓取值，指出 BUTTONELEMENT 是否為切換，也就是是否為雙狀態或單一狀態按鈕。
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT Windows Media Player 的不乾膠
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987168"
---
# <a name="buttonelementsticky"></a>BUTTONELEMENT。

「 **粘滯** 」屬性（attribute）會指定或抓取值，指出 **BUTTONELEMENT** 是否為切換，也就是是否為雙狀態或單一狀態按鈕。

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                               |
|-------|-------------------------------------------|
| true  | **BUTTONELEMENT** 為粘滯。              |
| false | 預設值。 **BUTTONELEMENT** 不是粘滯。 |



 

## <a name="remarks"></a>備註

如果 [ **粘滯** ] 屬性設定為 [true]，當您按下按鈕時，按鈕元素將會變更為 [關閉] 狀態，且會維持在該狀態中，直到再次按一下為止。 當 button 專案處於關閉狀態時， **向下** 屬性會是 true，而且會顯示按鈕群組 **downImage** 的適當部分。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONELEMENT 元素**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT 向下**](buttonelement-down.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





