---
title: EQUALIZERSETTINGS.nextPreset
description: NextPreset 方法會套用下一個等化器預設值。
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 715c5ee514cf2818cbab8b5553cab9565a2b448e47d1f6fe2282f17940cfc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748693"
---
# <a name="equalizersettingsnextpreset"></a>EQUALIZERSETTINGS.nextPreset

**NextPreset** 方法會套用下一個等化器預設值。

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果目前的預設值是最後一個預設值，則會將第一個預設值設為最新的。

## <a name="examples"></a>範例


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.previousPreset**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





