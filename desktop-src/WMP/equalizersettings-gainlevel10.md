---
title: EQUALIZERSETTINGS.gainLevel10
description: GainLevel10 屬性會指定或抓取帶狀10的增益層級。
ms.assetid: 0d645719-86aa-4475-8e87-ea6c20e4fed7
keywords:
- EQUALIZERSETTINGS. gainLevel10 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e80e05686d06871aa40e8a649a119a41fb1a7a59bbb60a77b56497561ae9f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748815"
---
# <a name="equalizersettingsgainlevel10"></a>EQUALIZERSETTINGS.gainLevel10

**GainLevel10** 屬性會指定或抓取帶狀10的增益層級。

``` syntax
        elementID.gainLevel10
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。 預設值為零。

## <a name="remarks"></a>備註

這個屬性會調整以16kHz 為中心的音訊頻率範圍部分。

如果未指定此屬性，則會保留先前的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





