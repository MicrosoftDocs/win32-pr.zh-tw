---
title: 滑杆. useForegroundProgress
description: UseForegroundProgress 屬性會指定或抓取值，指出是否會使用前景進度列。
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- UseForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989722"
---
# <a name="slideruseforegroundprogress"></a>滑杆. useForegroundProgress

**UseForegroundProgress** 屬性會指定或抓取值，指出是否會使用前景進度列。

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                              |
|-------|------------------------------------------|
| true  | 使用前景進度。                 |
| false | 預設值。 請勿使用前景進度。 |



 

## <a name="remarks"></a>備註

這個屬性允許使用 **foregroundProgress** 屬性，此屬性主要用於追蹤媒體檔案的下載進度，同時使用 **value** 屬性來追蹤檔案目前的播放位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**滑杆。值**](slider-value.md)
</dt> </dl>

 

 





