---
title: AmbientAttributes。可見
description: Visible 屬性會指定或抓取控制項的可見度。
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- AmbientAttributes visible Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124048"
---
# <a name="ambientattributesvisible"></a>AmbientAttributes。可見

**Visible** 屬性會指定或抓取控制項的可見度。

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                      |
|-------|----------------------------------|
| true  | 預設值。 可以看到控制項。 |
| false | 控制項是不可見的。      |



 

## <a name="remarks"></a>備註

這個屬性適用于隱藏控制項，例如，當您交換播放按鈕的 [暫停] 按鈕時。

如果值為 false，則不會顯示控制項，而是將事件傳遞給其後方的控制項。 如果值為 true，就會顯示控制項，並接收 click 事件本身。

**AUTOMENU** 元素的預設值為 false。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





