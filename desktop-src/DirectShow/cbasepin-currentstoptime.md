---
description: CurrentStopTime 方法會抓取區段停止時間，由 CBasePin：： NewSegment 方法設定。
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: 'CBasePin. CurrentStopTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977523"
---
# <a name="cbasepincurrentstoptime-method"></a>CBasePin. CurrentStopTime 方法

方法會抓取 `CurrentStopTime` 區段停止時間，由 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法設定。

## <a name="syntax"></a>語法


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBasePin：： m \_ tStop**](cbasepin-m-tstop.md)的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




