---
title: AmbientAttributes
description: MoveTo 方法會以線性速度將控制項移至新的位置。
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992886"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes

**MoveTo** 方法會以線性速度將控制項移至新的位置。

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**數值** (**long**) 指定控制項 **左方** 屬性的新值。

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**數值** (**long**) 指定控制項 **頂端** 屬性的新值。

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*時間*
</dt> <dd>

**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這種方法適用于動畫的子 **視圖** 專案 (例如，如果使用者按一下紙匣，而控制項向下滑) 。

這個方法會在移動控制項時建立線性動作。 這不同于 **slideTo**，它會建立非線性的動畫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





