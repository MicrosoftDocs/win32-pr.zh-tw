---
title: 效果。 allowAll
description: AllowAll 屬性會指定或抓取值，指出是否要包含登錄中的所有視覺效果。
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- 效果： allowAll Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56760021fe34522072677e9524fe6636e519e20f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985552"
---
# <a name="effectsallowall"></a>效果。 allowAll

**AllowAll** 屬性會指定或抓取值，指出是否要包含登錄中的所有視覺效果。

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                         |
|-------|---------------------------------------------------------------------|
| true  | 預設值。 允許迴圈使用者系統上的所有視覺效果。 |
| false | 限制迴圈出現在 **效果** 標記內的視覺效果。 |



 

## <a name="remarks"></a>備註

如果這個屬性設定為 false，則只有在 **效果** 標籤內出現的視覺效果可以使用上一個/下一個來迴圈。 如果設定為 true，則所有在使用者系統上註冊的視覺效果都可以迴圈執行。 如果設定為 true，且您在 **效果** 標記內指定任何視覺效果，則會將這些標記中指定的屬性套用至使用者系統上的所有視覺效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> </dl>

 

 





