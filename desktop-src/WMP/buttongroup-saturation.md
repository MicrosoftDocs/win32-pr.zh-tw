---
title: BUTTONGROUP 飽和度
description: 飽和度屬性會指定或抓取 BUTTONGROUP 影像的飽和度值。
ms.assetid: bfd957f0-8201-4a4f-9162-a397ed97c747
keywords:
- BUTTONGROUP 飽和度 Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8de7dd39eb0b1a9e3f24031e24851eba22c6c6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999354"
---
# <a name="buttongroupsaturation"></a>BUTTONGROUP 飽和度

**飽和度** 屬性會指定或抓取 **BUTTONGROUP** 影像的飽和度值。

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到2.0，預設值為1.0。

## <a name="remarks"></a>備註

這個屬性會變更 **disabledImage**、 **downImage**、 **hoverDownImage**、 **hoverImage** 和 **image** 屬性所指定之影像的飽和度值（如果已指定），而且它們參考的是8位的 BMP 影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. disabledImage**](buttongroup-disabledimage.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverDownImage**](buttongroup-hoverdownimage.md)
</dt> <dt>

[**BUTTONGROUP. hoverImage**](buttongroup-hoverimage.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> </dl>

 

 





