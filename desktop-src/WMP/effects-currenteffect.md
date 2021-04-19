---
title: 效果。 currentEffect
description: CurrentEffect 屬性會指定或抓取目前的視覺效果。
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- 效果： currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000384"
---
# <a name="effectscurrenteffect"></a>效果。 currentEffect

**CurrentEffect** 屬性會指定或抓取目前的視覺效果。

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **物件**。 預設值是撰寫順序中的第一個視覺效果。 如果面板中未撰寫任何視覺效果，則預設為登錄中的第一個視覺效果。

## <a name="remarks"></a>備註

您可以使用此物件來存取您所建立的自訂視覺效果。 例如，您可以透過視覺效果中的 **IDispatch** 介面公開屬性。 然後，您可以將視覺效果設為目前效果，然後使用 **currentEffect** 物件來設定屬性的新值，藉以變更面板中的屬性值。 例如，如果您的視覺效果公開名為 backgroundColor 的屬性，則下列 JScript 程式碼會指定新的值：


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> <dt>

[**效果。 currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**效果。 currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





