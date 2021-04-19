---
title: CUSTOMSLIDER.disabledImage
description: DisabledImage 屬性會指定或抓取滑杆停用時使用的滑杆影像。
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995038"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

**DisabledImage** 屬性會指定或抓取滑杆停用時使用的滑杆影像。

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

此屬性是選擇性的。 如果未指定，將會使用 **image** 屬性中指定的檔案。

**DisabledImage** 代表 **CUSTOMSLIDER** 控制項的停用狀態。 它可以是單一影像或一系列的影像，代表滑杆的各種狀態。 如果使用多個映射，則會以與 **圖像** 檔相同的方式來排列它們。

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

 

 





