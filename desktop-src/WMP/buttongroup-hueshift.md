---
title: BUTTONGROUP. hueShift
description: HueShift 屬性會指定或抓取 BUTTONGROUP 影像的色調要移位的量。
ms.assetid: 156256ef-ec24-40c4-ad23-064e38c79e69
keywords:
- BUTTONGROUP. hueShift Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf77faea27ecc5adee6525c4ee8d8ff1541aac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977146"
---
# <a name="buttongrouphueshift"></a>BUTTONGROUP. hueShift

**HueShift** 屬性會指定或抓取 **BUTTONGROUP** 影像的色調要移位的量。

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **編號** (**float**) ，其值範圍從0.0 到360.0，預設值為0.0。

## <a name="remarks"></a>備註

這個屬性會變更 **disabledImage**、 **downImage**、 **hoverDownImage**、 **hoverImage** 和 **image** 屬性所指定之影像的色調值（如果已指定），而且它們參考的是8位的 BMP 影像。

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

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP 飽和度**](buttongroup-saturation.md)
</dt> </dl>

 

 





