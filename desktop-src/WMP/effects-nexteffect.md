---
title: 效果。 nextEffect
description: NextEffect 方法會顯示下一個視覺效果的第一個預設值，略過中間的預設值。
ms.assetid: dedd8e8b-2337-46f5-91a8-43ef54c86012
keywords:
- 效果： nextEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.nextEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 359571dde65c8cb65f422de58667c715cb7a3099e79a443dd64777edbf8767d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339983"
---
# <a name="effectsnexteffect"></a>效果。 nextEffect

**NextEffect** 方法會顯示下一個視覺效果的第一個預設值，略過中間的預設值。

``` syntax
        elementID.nextEffect()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會以撰寫順序顯示下一個視覺效果的第一個預設值。 如果目前的視覺效果是撰寫順序中的最後一個視覺效果，而且如果 **allowAll** 為 false，則會將第一個視覺效果設為最新。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> <dt>

[**效果。 allowAll**](effects-allowall.md)
</dt> <dt>

[**效果。 previousEffect**](effects-previouseffect.md)
</dt> </dl>

 

 





