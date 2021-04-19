---
title: 滑杆。值
description: Value 屬性會指定或抓取滑杆的目前位置。 |滑杆。值
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- 滑杆。值 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984052"
---
# <a name="slidervalue"></a>滑杆。值

**Value** 屬性會指定或抓取滑杆的目前位置。

``` syntax
        elementID.value
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**float**) 的讀/寫 **數位**，預設值為 **min**。

## <a name="remarks"></a>備註

此 **值** 應該一律大於或等於 **最小** 值，且小於或等於 **max**。如果您指定超出此範圍的值，則 [ **值** ] 和滑杆的位置都不會變更。

請參閱 **CUSTOMSLIDER**。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆。最小值**](slider-min.md)
</dt> </dl>

 

 





