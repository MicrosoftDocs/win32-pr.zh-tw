---
title: AmbientAttributes
description: TabStop 屬性會指定或抓取值，指出控制項是否為定位順序。 您可以藉由將控制項放在其他控制項標記之前或之後的整體腳本，來設定定位順序。
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes Windows Media Player 的 tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996039"
---
# <a name="ambientattributestabstop"></a>AmbientAttributes

**TabStop** 屬性會指定或抓取值，指出控制項是否為定位順序。 您可以藉由將控制項放在其他控制項標記之前或之後的整體腳本，來設定定位順序。

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | 控制項處於 [定位順序] (控制項將會有一個索引標籤停止： [協助工具需求]) 。 |
| false | 控制項不在定位順序中。                                                       |



 

## <a name="remarks"></a>備註

**TabStop** 屬性不適用於 **效果** 元素。

除了 **AUTOMENU** 和 **TEXT** 以外的所有元素（預設值為 false），此屬性的預設值都是 true。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





