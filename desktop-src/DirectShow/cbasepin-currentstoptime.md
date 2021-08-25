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
ms.openlocfilehash: 2905913828c91fffde9fb474802c8dea0e0f83d59ccdb5408f846a1936071cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916698"
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

 

 




