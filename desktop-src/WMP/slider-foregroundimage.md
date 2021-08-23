---
title: 滑杆. foregroundImage
description: ForegroundImage 屬性會指定或抓取滑杆的前景影像。
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- ForegroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735708"
---
# <a name="sliderforegroundimage"></a>滑杆. foregroundImage

**ForegroundImage** 屬性會指定或抓取滑杆的前景影像。

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

此屬性是選擇性的。 使用影像來建立滑杆控制項時， **backgroundImage** 會用於主要滑杆影像。 **ThumbImage** 代表實際的滑杆，而且可以使用滑鼠移動。 在 **thumbImage** 滑杆有一個不可見的行，其中的背景影像會顯示在一行的一端，而前景影像會顯示在另一端。

當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。 如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。

如果並排顯示 **的屬性設** 為 true，且前景影像小於滑杆控制項的前景區域，則會以水準或垂直方式並排顯示影像，視 **方向** 屬性而定，填滿可用的空間。

支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

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

[**滑杆。投影片**](slider-slide.md)
</dt> <dt>

[**滑杆. thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**滑杆。值**](slider-value.md)
</dt> </dl>

 

 





