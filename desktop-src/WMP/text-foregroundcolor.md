---
title: ForegroundColor
description: ForegroundColor 屬性會指定或抓取文字控制項的文字色彩。
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- ForegroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982951"
---
# <a name="textforegroundcolor"></a>ForegroundColor

**ForegroundColor** 屬性會指定或抓取文字控制項的文字色彩。

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>可能的值

這個屬性是包含任何 Microsoft Internet Explorer 色彩值的讀取/寫入 **字串** 。 預設值為「黑色」。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

當您使用 **AlphaBlend** 或 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。 如果前景色彩也是黑色 (這是 **foregroundColor** 屬性) 的預設值，您的文字可能會變成無法讀取。 若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。

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

[**BackgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





