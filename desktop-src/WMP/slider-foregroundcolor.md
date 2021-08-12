---
title: 滑杆. foregroundColor
description: ForegroundColor 屬性會指定或抓取滑杆控制項的前景色彩。
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- ForegroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569084"
---
# <a name="sliderforegroundcolor"></a>滑杆. foregroundColor

**ForegroundColor** 屬性會指定或抓取滑杆控制項的前景色彩。

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。 預設值為 "白色"。

## <a name="remarks"></a>備註

您可以指定兩組屬性的其中一個來建立基本滑杆控制項： **backgroundColor** 和 **ForegroundColor**，或 **backgroundImage** 和 **foregroundImage**。

當您使用 [色彩] 屬性來建立滑杆控制項時，滑杆控制項的維度會定義以背景色彩填滿的區域。 前景色彩會包含滑杆位置增加時的背景色彩。

若要將漸層填滿背景或前景色彩所佔用的區域，請指定 **backgroundEndColor** 或 **foregroundEndColor** 屬性。

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

[**滑杆. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**滑杆. backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**滑杆. foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





