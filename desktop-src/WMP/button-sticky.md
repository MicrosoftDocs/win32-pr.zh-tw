---
title: 按鈕。粘滯
description: 「粘滯」屬性（attribute）會指定或抓取值，指出按鈕是否為切換，也就是是否為雙狀態或單一狀態按鈕。
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- 按鈕。粘滯 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990034"
---
# <a name="buttonsticky"></a>按鈕。粘滯

「 **粘滯** 」屬性（attribute）會指定或抓取值，指出 **按鈕** 是否為切換，也就是是否為雙狀態或單一狀態 **按鈕**。

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                        |
|-------|------------------------------------|
| true  | **按鈕** 為粘滯。              |
| false | 預設值。 **按鈕** 不是相黏鍵。 |



 

## <a name="remarks"></a>備註

如果 [ **粘滯** ] 設定為 [true]，當您按下按鈕時， **按鈕** 將會變更為 [關閉] 狀態，直到再次按一下為止。 當 **按鈕** 處於關閉狀態時， **向下** 屬性會是 true，而且會顯示 **downImage** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕。向下鍵**](button-down.md)
</dt> <dt>

[**按鈕. downImage**](button-downimage.md)
</dt> </dl>

 

 





