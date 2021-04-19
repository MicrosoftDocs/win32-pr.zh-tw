---
title: 滑杆. backgroundImage
description: BackgroundImage 屬性會指定或抓取滑杆的背景影像。
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982930"
---
# <a name="sliderbackgroundimage"></a>滑杆. backgroundImage

**BackgroundImage** 屬性會指定或抓取滑杆的背景影像。

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

此屬性是選擇性的。 使用影像來建立滑杆時， **backgroundImage** 會用於主要滑杆影像。 **ThumbImage** 代表實際的滑杆，而且可以使用滑鼠移動。 在 **thumbImage** 滑杆有一個不可見的行，其中的背景影像會顯示在一行的一端，而前景影像會顯示在另一端。

當您以滑鼠移動 **thumbImage** 滑杆時，如果投影 **片** 設為 true，則前景影像會沿著滑杆拉出以涵蓋背景影像的方式滑出。 如果投影 **片** 設為 false，則前景影像不會移動，但會顯示在原處，如同滑杆將背景影像移出前景影像。

如果 [並排顯示 **] 屬性設定** 為 [true]，而且背景影像小於滑杆控制項，則會根據 [ **方向** ] 屬性，以水準或垂直方式並排顯示影像。 如果 [ **borderSize** ] 屬性設定為大於零的值，則指定的數位將會是從影像左邊、右邊或頂端和底部開始 (的圖元數，視將保留給滑杆控制項框線的 **方向** 屬性) 而定。 在此情況下，只有影像的中央部分會用來將其餘的控制項平平鋪。

支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**滑杆。投影片**](slider-slide.md)
</dt> <dt>

[**滑杆. thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





