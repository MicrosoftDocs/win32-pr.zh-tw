---
title: BackgroundColor
description: BackgroundColor 屬性會指定或抓取文字控制項的背景色彩。
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- BackgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995638"
---
# <a name="textbackgroundcolor"></a>BackgroundColor

**BackgroundColor** 屬性會指定或抓取文字控制項的背景色彩。

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值或值為 "none" 的讀取/寫入 **字串** 。 預設值為 "none"，表示背景是透明的。

## <a name="remarks"></a>備註

背景色彩會設定為控制項的高度和寬度。 如果未設定高度和寬度，則會將背景色彩設定為文字的高度和寬度。

當您使用 **AlphaBlend** 或 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。 如果前景色彩也是黑色 (這是 **foregroundColor** 屬性) 的預設值，您的文字可能會變成無法讀取。 若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AmbientAttributes. AlphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.AlphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**色彩參考**](color-reference.md)
</dt> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





