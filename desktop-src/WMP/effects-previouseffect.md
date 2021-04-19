---
title: 效果。 previousEffect
description: PreviousEffect 方法會顯示先前的視覺效果，並略過預設值。
ms.assetid: f1cfef29-0241-4028-b047-4f17bf0e9250
keywords:
- 效果： previousEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.previousEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5482e7c202d6d35f3a833b5bafc8a41dca38956
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984883"
---
# <a name="effectspreviouseffect"></a>效果。 previousEffect

**PreviousEffect** 方法會顯示先前的視覺效果，並略過預設值。

``` syntax
        elementID.previousEffect()
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會以撰寫順序顯示先前的視覺效果。 如果目前的視覺效果是撰寫順序中的第一個視覺效果，而且如果 **allowAll** 為 false，則最後一個視覺效果會成為最新的視覺效果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> <dt>

[**效果。 nextEffect**](effects-nexteffect.md)
</dt> <dt>

[**效果。 allowAll**](effects-allowall.md)
</dt> </dl>

 

 





