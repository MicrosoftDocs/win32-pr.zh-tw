---
title: BUTTONGROUP. hoverImage
description: HoverImage 屬性會指定或抓取影像的名稱，代表 BUTTONGROUP 中按鈕的暫留狀態。 當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106974914"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP. hoverImage

**HoverImage** 屬性會指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫留狀態。 當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

支援的影像格式為 BMP、JPG、PNG 和 GIF。 如果影像是8位的 BMP 檔案，則可以使用 **hueShift** 和 **飽和度** 屬性動態變更其色調和飽和度值。

預設影像是 **image** 屬性中指定的影像或其預設值。

如果暫留影像大於定義的區域，則會裁剪停留影像。

如果無法抓取影像，則會顯示 (紅 x 影像) 的預設影像。

## <a name="examples"></a>範例

請參閱 *BUTTONELEMENT*。說明如何使用此屬性之範例的 [mappingColor](buttonelement-mappingcolor.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP 影像**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP 飽和度**](buttongroup-saturation.md)
</dt> </dl>

 

 





