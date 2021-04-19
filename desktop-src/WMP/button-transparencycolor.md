---
title: 按鈕. transparencyColor
description: TransparencyColor 屬性會指定或抓取按鈕影像中透明的色彩。
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- TransparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001190"
---
# <a name="buttontransparencycolor"></a>按鈕. transparencyColor

**TransparencyColor** 屬性會指定或抓取 **按鈕** 影像中透明的色彩。

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>可能的值

這個屬性是一個不含預設值的讀取/寫入 **字串** ，其中包含下列其中一個值。



| 值                                    | 描述                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 自動                                     | 影像中位置0、0的圖元色彩會變成透明色彩。                        |
| 任何 Internet Explorer 色彩格式值 | Internet Explorer 的色彩格式值會變成透明色彩 (例如，「紅色」或「 \# FF0000」 ) 。 |
| 無                                     | 沒有透明度。                                                                                          |



 

## <a name="remarks"></a>備註

影像中的透明色彩可讓影像背後的任何內容顯示在透明區域中。 **按鈕** 仍會在透明區域上收到點擊。

透明色彩可以是任何 Internet Explorer 的色彩值。 如果 **transparencyColor** 屬性的值設定為「自動」，則會使用影像中位置0、0的圖元色彩。

如果指定的色彩不是其中一種有效的 IE 色彩，則會保留先前的值。

由於 Jpg 是有損耗的，因此可能會發生未預期的色彩變更，因此在使用 **transparencyColor** 時不建議使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTON 元素**](button-element.md)
</dt> <dt>

[**按鈕。影像**](button-image.md)
</dt> <dt>

[**色彩參考**](color-reference.md)
</dt> </dl>

 

 





