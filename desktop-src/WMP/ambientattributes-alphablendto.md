---
title: AmbientAttributes.AlphaBlendTo
description: AlphaBlendTo 方法會在一段時間內調整 AlphaBlend 屬性。
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes. AlphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999333"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.AlphaBlendTo

**AlphaBlendTo** 方法會在一段時間內調整 **AlphaBlend** 屬性。

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

 (long) 指定新的不透明度值的 **數位**。 範圍從 0 (不會) 255 (完全不透明度) 。

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*AlphaTime*
</dt> <dd>

**Number** (**long**) 指定時間（以毫秒為單位），這會讓元素變更不透明度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法適用于讓元素逐漸出現或消失。

當您使用 **AlphaBlendTo** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。 如果前景色彩也是黑色 (這是 *文字* 的預設值。**foregroundColor**) ，您的文字可能會變成無法讀取。 若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。

> [!Note]  
> Windows 98 不支援這個屬性。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. AlphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**BackgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





