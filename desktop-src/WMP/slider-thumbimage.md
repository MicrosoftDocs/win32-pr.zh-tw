---
title: 滑杆. thumbImage
description: ThumbImage 屬性會指定或抓取將用來表示滑杆目前位置的影像。
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- ThumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0711cb7a652032db4b167040fbd604d1e561885926bf8fc7c31d1fedb65049e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995138"
---
# <a name="sliderthumbimage"></a>滑杆. thumbImage

**ThumbImage** 屬性會指定或抓取將用來表示滑杆目前位置的影像。

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

**ThumbImage** 會指定要用來代表目前位置的影像，以及表示使用者可以對控制項採取動作。 如果未指定任何 thumb 影像，則滑杆為非互動式。

捲動方塊的影像會以滑杆控制項的窄維度為中心。 如果 thumb 影像比控制項窄，則影像會出現在背景的中間。 如果 thumb 影像大於控制項，則會將影像的末端剪下。

滑杆的位置是由 thumb 影像的中心所指定。 如果 **borderSize** 為零，則只有一半的 thumb 影像會顯示在開頭和結束滑杆的位置。 若要避免這種情況，請將 **borderSize** 設定為大於或等於 thumb (影像寬度一半的值，如果 **方向** 設為「垂直」 ) ，則為一半的高度。

支援的格式為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

請參閱 **CUSTOMSLIDER**。說明如何使用 **滑杆** 元素屬性之範例的 [positionImage](customslider-positionimage.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆. borderSize**](slider-bordersize.md)
</dt> <dt>

[**滑杆。方向**](slider-direction.md)
</dt> </dl>

 

 





