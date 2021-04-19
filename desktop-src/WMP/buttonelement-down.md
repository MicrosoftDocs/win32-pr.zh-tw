---
title: BUTTONELEMENT 向下
description: 向下屬性會指定或抓取值，指出 button 元素在上或下移位置。
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987163"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT 向下

**向下** 屬性會指定或抓取值，指出 button 元素在上或下移位置。

``` syntax
        elementID.down
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                     |
|-------|-----------------------------------------------------------------|
| true  | 表示 **BUTTONELEMENT** 在下的位置。        |
| false | 預設值。 表示 **BUTTONELEMENT** 在上的位置。 |



 

## <a name="remarks"></a>備註

若要讓按鈕元素保持在關閉位置，必須將 [ **粘滯** ] 設定為 [true]。 依預設，[ **粘滯** ] 為 false，而任何設定為 [true **] 的嘗試** 都會被忽略。

如果指定了不正確值，則會維護先前的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONELEMENT 元素**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





