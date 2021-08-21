---
title: VOLUMESLIDER
description: 這是具有下列預設值的預先定義滑杆。 |VOLUMESLIDER
ms.assetid: 7533863b-49de-4c1b-8750-fd333c573a17
keywords:
- VOLUMESLIDER Windows Media Player
topic_type:
- apiref
api_name:
- VOLUMESLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ebc2e6ec82327be9cb423d05661a5a38bbcc445450fc6d4f56ceaf7caa8b270d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054006"
---
# <a name="volumeslider"></a>VOLUMESLIDER

這是具有下列預設值的預先定義滑杆。

``` syntax
toolTip="Volume"
max="100"
min="0"
value="wmpprop:player.settings.volume"
value_onchange="jscript:player.settings.volume=value;
player.settings.mute=false;"
```

## <a name="remarks"></a>備註

這會建立可設定音訊音量的滑杆控制項。 工具提示已當地語系化。 此滑杆的所有屬性都可以藉由明確指定來覆寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> </dl>

 

 





