---
title: 按鈕。向下鍵
description: 向下屬性會指定或抓取值，指出按鈕是否在上或向下位置。
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- 按鈕。關閉 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979440"
---
# <a name="buttondown"></a>按鈕。向下鍵

**向下** 屬性會指定或抓取值，指出 **按鈕** 是否在上或向下位置。

``` syntax
        elementID.down
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                   |
|-------|---------------------------------------------------------------|
| true  | 指出 **按鈕** 位於下位置。        |
| false | 預設值。 指出 **按鈕** 在上的位置。 |



 

## <a name="remarks"></a>備註

若要讓 **按鈕** 保持在關閉位置，必須將 [ **粘滯** ] 設定為 [true]。 依預設，[ **粘滯** ] 為 false，而任何設定為 [true **] 的嘗試** 都會被忽略。

如果指定了不正確值，則會維護先前的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕. downImage**](button-downimage.md)
</dt> <dt>

[**按鈕. downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





