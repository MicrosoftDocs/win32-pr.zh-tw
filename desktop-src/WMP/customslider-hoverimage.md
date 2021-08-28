---
title: CUSTOMSLIDER.hoverImage
description: 當滑鼠停留在自訂滑杆上時，hoverImage 屬性會指定或抓取顯示的影像。
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651398"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

當滑鼠停留在自訂滑杆上時， **hoverImage** 屬性會指定或抓取顯示的影像。

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

此屬性是選擇性的。 如果未指定，將會使用 **image** 屬性中指定的檔案。

**HoverImage** 代表 CUSTOMSLIDER 控制項的停留狀態;也就是滑鼠游標停留在其上方時所顯示的狀態。 它可以是單一影像或一系列的影像，代表滑杆的各種狀態。 如果使用多個映射，則會以與 **圖像** 檔相同的方式來排列它們

支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CUSTOMSLIDER 元素**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER 影像**](customslider-image.md)
</dt> </dl>

 

 





