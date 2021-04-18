---
description: CurrentStartTime 方法會捕獲區段開始時間，由 CBasePin：： NewSegment 方法設定。
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: 'CBasePin. CurrentStartTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976270"
---
# <a name="cbasepincurrentstarttime-method"></a>CBasePin. CurrentStartTime 方法

方法會抓取 `CurrentStartTime` 區段開始時間，由 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法設定。

## <a name="syntax"></a>語法


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBasePin：： m \_ tStart**](cbasepin-m-tstart.md)的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




