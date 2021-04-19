---
title: BackgroundImage
description: BackgroundImage 屬性會指定或抓取 VIEW 或子視圖的背景影像。
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96f4a93882e02589d7f15b74ba5cb225f506d69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985553"
---
# <a name="viewbackgroundimage"></a>BackgroundImage

**BackgroundImage** 屬性會指定或抓取 **VIEW** 或子視圖的背景影像 **。**

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的格式為 BMP、JPG、GIF 和 PNG。 如果影像是8位的 BMP 檔案，則可以使用 **backgroundImageHueShift** 和 **backgroundImageSaturation** 屬性動態變更其色調和飽和度值。

在 Windows Media 下載封裝中，如果您為 **VIEW** 元素指定 **backgroundImage** 屬性，則還必須指定該元素的 **backgroundColor** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VIEW 元素**](view-element.md)
</dt> <dt>

[**BackgroundImageHueShift**](view-backgroundimagehueshift.md)
</dt> <dt>

[**BackgroundImageSaturation**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





