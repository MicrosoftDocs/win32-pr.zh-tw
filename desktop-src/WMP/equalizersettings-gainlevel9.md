---
title: EQUALIZERSETTINGS.gainLevel9
description: GainLevel9 屬性會指定或抓取寬線9的增益層級。
ms.assetid: 2bed7486-4d4c-4c71-8bab-8dd0c4f56911
keywords:
- EQUALIZERSETTINGS. gainLevel9 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel9
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 869f3ff05b72a422e1d48d90972baa94dc9cf390dc93b3a72ed897f569762f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650719"
---
# <a name="equalizersettingsgainlevel9"></a>EQUALIZERSETTINGS.gainLevel9

**GainLevel9** 屬性會指定或抓取寬線9的增益層級。

``` syntax
        elementID.gainLevel9
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。 預設值為零。

## <a name="remarks"></a>備註

這個屬性會調整以8kHz 為中心的音訊頻率範圍部分。

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

 

 





