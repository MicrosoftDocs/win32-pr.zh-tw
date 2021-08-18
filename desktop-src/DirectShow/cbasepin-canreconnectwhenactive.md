---
description: CanReconnectWhenActive 方法會查詢 pin 是否支援動態重新連接。
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: 'CBasePin. CanReconnectWhenActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916918"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>CBasePin. CanReconnectWhenActive 方法

`CanReconnectWhenActive`方法會查詢 pin 是否支援動態重新連接。

## <a name="syntax"></a>語法


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回布林值，指定 pin 是否可動態重新連接。 若 **為 TRUE**，則 pin 可以動態重新連接。

## <a name="remarks"></a>備註

根據預設，您必須先停止篩選，才能重新連接其任何 pin。 但是，如果 pin 支援動態重新連接，則在篩選作用中時，它可以重新連接。 如需詳細資訊，請參閱[動態 Graph 建立](dynamic-graph-building.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




