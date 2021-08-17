---
title: 滑杆。磚
description: 並排顯示的屬性會指定或抓取值，指出是否要將滑杆影像並排顯示。
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- 滑杆。磚 Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a97be7ee857574b24585ffd7ffd9b63acdfad0a37762445699daa3a06f94e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832534"
---
# <a name="slidertiled"></a>滑杆。磚

並排顯示 **的屬性會** 指定或抓取值，指出是否要將滑杆影像並排顯示。

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | 預設值。 影像點陣圖會重複，直到填滿控制項的整個區域為止。 |
| false | 影像將不會並排顯示。                                                                |



 

## <a name="remarks"></a>備註

只有當您使用前景和背景影像來定義滑杆控制項時，才適用這個屬性。 如果影像小於滑杆的定義區域，而且 **已將並排顯示的** 屬性設為 true，則影像將會重複，直到填滿控制項的整個長度為止。

您可能會想要搭配使用此屬性與 **borderSize** 屬性。 **BorderSize** 屬性可讓您定義在平鋪期間不重複的框線。

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

[**滑杆. borderSize**](slider-bordersize.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





