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
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993455"
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

根據預設，您必須先停止篩選，才能重新連接其任何 pin。 但是，如果 pin 支援動態重新連接，則在篩選作用中時，它可以重新連接。 如需詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




