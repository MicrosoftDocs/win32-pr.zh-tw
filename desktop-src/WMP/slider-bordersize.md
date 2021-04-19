---
title: 滑杆. borderSize
description: BorderSize 屬性會指定或抓取框線寬度（以圖元為單位）。
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- BorderSize Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994155"
---
# <a name="sliderbordersize"></a>滑杆. borderSize

**BorderSize** 屬性會指定或抓取框線寬度（以圖元為單位）。

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **數位** (**長**) 表示框線寬度（以圖元為單位）。 預設值為零。

## <a name="remarks"></a>備註

這個屬性會定義從滑杆控制項的開頭和結尾算起的位移，也就是當 **direction** 屬性設定為 "水準" 時，從左至右，如果設定為「垂直」，則是從上到下。 這些位移位置會指示滑杆捲動方塊的最小和最大位置，而不會套用前景色彩或影像。

如果使用背景影像 **並將 [並排屬性]** 設定為 [true]，則會將位移套用至影像，並將影像的數量 (從左邊和右邊，或從頂端和底部) 用於滑杆控制項的開始和結束框線，並在其餘部分並排顯示影像的中央部分。 如此一來，小型背景影像就可以用來涵蓋較大滑杆控制項的完整長度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**滑杆. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**滑杆。磚**](slider-tiled.md)
</dt> </dl>

 

 





