---
title: 滑杆. backgroundColor
description: BackgroundColor 屬性會指定或抓取滑杆控制項的背景色彩。
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc2de30392c58cfad151e2d3c209f0407880a47522a536bf08dbe42d7f56dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995228"
---
# <a name="sliderbackgroundcolor"></a>滑杆. backgroundColor

**BackgroundColor** 屬性會指定或抓取滑杆控制項的背景色彩。

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。 它沒有預設值。

## <a name="remarks"></a>備註

您可以藉由指定 **backgroundColor** 或 **BackgroundImage**，以及 **foregroundColor** 或 **foregroundImage** 來建立基本滑杆控制項。

使用色彩時，滑杆控制項的維度會定義以背景色彩填滿的區域。 前景色彩會包含滑杆位置增加時的背景色彩。

若要為背景或前景色彩所佔用的區域進行漸層填滿，請指定 **backgroundEndColor** 或 **foregroundEndColor** 屬性。

請參閱 *CUSTOMSLIDER*。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**色彩參考**](color-reference.md)
</dt> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**滑杆. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**滑杆. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**滑杆. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





