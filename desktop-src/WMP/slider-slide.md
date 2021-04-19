---
title: 滑杆。投影片
description: 投影片屬性會指定或抓取值，指出前景影像是否滑在背景影像上，或是在背景影像的靜態位置中逐漸顯示。
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- 滑杆。投影片 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984356"
---
# <a name="sliderslide"></a>滑杆。投影片

投影 **片** 屬性會指定或抓取值，指出前景影像是否滑在背景影像上，或是在背景影像的靜態位置中逐漸顯示。

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                          |
|-------|----------------------------------------------------------------------|
| true  | 預設值。 前景影像會滑到背景影像上方。      |
| false | 前景影像會顯示在背景影像上。 |



 

## <a name="remarks"></a>備註

當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。 如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





