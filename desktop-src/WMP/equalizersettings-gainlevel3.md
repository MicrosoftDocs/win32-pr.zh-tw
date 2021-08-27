---
title: EQUALIZERSETTINGS.gainLevel3
description: GainLevel3 屬性會指定或抓取寬線3的增益層級。
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- EQUALIZERSETTINGS. gainLevel3 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8e719cd59a253ded35ad10e067f537d6f7d3a68d0d0b05a4cf79d0cd976f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123648"
---
# <a name="equalizersettingsgainlevel3"></a>EQUALIZERSETTINGS.gainLevel3

**GainLevel3** 屬性會指定或抓取寬線3的增益層級。

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。 預設值為零。

## <a name="remarks"></a>備註

這個屬性會調整以125Hz 為中心的音訊頻率範圍部分。

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

 

 





