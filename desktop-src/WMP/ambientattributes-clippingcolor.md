---
title: AmbientAttributes.clippingColor
description: ClippingColor 屬性會指定或抓取從 clippingImage 點陣圖裁剪的色彩。
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes. clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995958"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

**ClippingColor** 屬性會指定或抓取從 **clippingImage** 點陣圖裁剪的色彩。

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串**。



| 值                                       | 描述                                       |
|---------------------------------------------|---------------------------------------------------|
| 自動                                        | 預設值。 使用圖元位置0、0的色彩。 |
| 任何 Microsoft Internet Explorer 色彩值 | 使用指定的 Internet Explorer 色彩。    |



 

## <a name="remarks"></a>備註

裁剪色彩表示 **clippingImage** 的區域 (**或)** **backgroundImage** ，可對應 **至控制項的** 透明、不可按的部分。 裁剪色彩可以表示要裁剪多個區域。如果 **clippingImage** 是一個 JPG 來警告 jpg 中的色彩遺失，就會發出警告。

**播放清單** 元素不支援 **clippingColor** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**色彩參考**](color-reference.md)
</dt> </dl>

 

 





