---
description: CurrentRate 方法會抓取區段速率（由 CBasePin：： NewSegment 方法所設定）。
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: 'CBasePin. CurrentRate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c522a76aebce39e4670d4d00b3344bf56d20172c2d54243322dd36a5d203226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955197"
---
# <a name="cbasepincurrentrate-method"></a>CBasePin. CurrentRate 方法

方法會抓取 `CurrentRate` [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法所設定的區段速率。

## <a name="syntax"></a>語法


```C++
double CurrentRate();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBasePin：： m \_ dRate**](cbasepin-m-drate.md)的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




