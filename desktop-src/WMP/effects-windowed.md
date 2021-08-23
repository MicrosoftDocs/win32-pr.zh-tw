---
title: 效果。視窗化
description: 視窗型屬性會指定或抓取值，指出視覺效果是否為視窗化或無視窗，也就是控制項的整個矩形是否會在任何時間顯示，或是是否可以裁剪。
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- 效果。視窗化 Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650998"
---
# <a name="effectswindowed"></a>效果。視窗化

**視窗** 型屬性會指定或抓取值，指出視覺效果是否為視窗化或無視窗，也就是控制項的整個矩形是否會在任何時間顯示，或是是否可以裁剪。 這個屬性只能在設計階段設定。

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>可能的值

這個屬性是在設計階段指定的 **布林值** ，之後是唯讀的。



| 值 | 描述                              |
|-------|------------------------------------------|
| true  | 控制項將會是視窗化。            |
| false | 預設值。 控制項將會是無視窗的。 |



 

## <a name="remarks"></a>備註

如果需要非矩形的視覺效果視窗，或是任何部分的視窗包含在影像中，則此屬性必須設定為 false。 這會犧牲一些執行必要裁剪的效能。

如果 **視窗** 設定為 true，則會忽略涵蓋視覺效果視窗的任何影像，而視覺效果視窗會具有最高層級的迭置順序。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> </dl>

 

 





