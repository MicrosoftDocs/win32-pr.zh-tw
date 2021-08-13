---
title: AmbientAttributes.slideTo
description: SlideTo 方法會將控制項移至新的位置。 控制項在指定的時間週期內以非線性方式移動。
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes. slideTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469908"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

**SlideTo** 方法會將控制項移至新的位置。 控制項在指定的時間週期內以非線性方式移動。

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**數值** (**long**) 指定控制項 **左方** 屬性的新值。

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**數值** (**long**) 指定控制項 **頂端** 屬性的新值。

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法與 **moveTo** 不同，後者會在移動控制項時建立線性動作。 這個方法所建立的非線性動畫是一個滑動動作，可從動作開頭的零速度加速，並在結束時減速回零，以順利停止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





