---
title: EQUALIZERSETTINGS.gainLevel5
description: GainLevel5 屬性會指定或抓取寬線5的增益層級。
ms.assetid: 6077a4dc-b9b8-4e00-8b29-14afe5a44321
keywords:
- EQUALIZERSETTINGS. gainLevel5 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel5
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b68e3567b4064a650a9f69cc4608e2b69600cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993273"
---
# <a name="equalizersettingsgainlevel5"></a>EQUALIZERSETTINGS.gainLevel5

**GainLevel5** 屬性會指定或抓取寬線5的增益層級。

``` syntax
        elementID.gainLevel5
```

## <a name="possible-values"></a>可能的值

這個屬性是一個讀/寫 **號碼** (**Float**) ，其值通常範圍從20到 + 20。 預設值為零。

## <a name="remarks"></a>備註

這個屬性會調整以500Hz 為中心的音訊頻率範圍部分。

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

 

 





