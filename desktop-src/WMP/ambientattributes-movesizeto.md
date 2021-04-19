---
title: AmbientAttributes.moveSizeTo
description: MoveSizeTo 方法會移動控制項，並在新的位置指定控制項的新大小。 控制項會在指定的時間週期內以動畫方式移動和調整大小。
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes. moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976005"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

**MoveSizeTo** 方法會移動控制項，並在新的位置指定控制項的新大小。 控制項會在指定的時間週期內以動畫方式移動和調整大小。

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
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

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

為控制項的 **width** 屬性指定新值的 (**long**) **數位**。

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**數值** (**long**) 指定控制項 **height** 屬性的新值。

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Number** (**long**) 指定控制項移至新位置所需的時間（以毫秒為單位）。

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**布林值** ，指定移動控制項時所建立的動作類型。



| 值 | 描述                                                             |
|-------|-------------------------------------------------------------------------|
| true  | 移動是非線性的 (滑動動作，可加速和減速) 。 |
| false | 動作是線性的。                                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

控制項的動作可以是線性或非線性。 線性運動表示控制項會以固定速度移至新位置，突然開始和停止。 當指定非線性動作時，會建立滑動動作，以加速從動作開頭的零開始，並在結束時減速回零，以順利停止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes 高度**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes 寬度**](ambientattributes-width.md)
</dt> </dl>

 

 





