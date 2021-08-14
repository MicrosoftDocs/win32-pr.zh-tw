---
title: BUTTONGROUP. transparencyColor
description: TransparencyColor 屬性會指定或抓取 BUTTONGROUP 影像的透明色彩。
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf97a25081e3f5c5729721bd675d9c59be1a4d52adc86acf6b9b75a0ee86dbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342661"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP. transparencyColor

**TransparencyColor** 屬性會指定或抓取 **BUTTONGROUP** 影像的透明色彩。

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>可能的值

這個屬性是沒有預設值的讀取/寫入 **字串** ，其中包含下列其中一個值。



| 值                                       | 描述                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| 自動                                        | 影像中位置0、0的圖元會變成透明色彩。                              |
| 任何 Microsoft Internet Explorer 色彩值 | Internet Explorer 色彩值變成透明色彩 (例如，「紅色」或「 \# FF0000」 ) 。 |
| 無                                        | 預設值。 沒有透明度。                                                                          |



 

## <a name="remarks"></a>備註

影像中的透明色彩會允許影像背後的任何內容顯示在透明區域中。 透明區域是可按的，除非 **clippingImage** 標記將其裁剪。

色彩可以是任何 Microsoft Internet Explorer 的色彩值。 如果值為 Auto，則會使用影像中位置0、0的圖元色彩。

如果指定的色彩不是有效 Internet Explorer 色彩之一，則會傳回警告，並維持先前的值。

由於 Jpg 是有損耗的，因此可能會發生未預期的色彩變更，因此在使用 **transparencyColor** 時不建議使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BUTTONGROUP 元素**](buttongroup-element.md)
</dt> <dt>

[**色彩參考**](color-reference.md)
</dt> </dl>

 

 





