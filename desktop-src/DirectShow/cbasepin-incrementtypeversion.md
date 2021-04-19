---
description: IncrementTypeVersion 方法會遞增一組慣用媒體類型的版本號碼。
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: 'CBasePin. IncrementTypeVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978494"
---
# <a name="cbasepinincrementtypeversion-method"></a>CBasePin. IncrementTypeVersion 方法

`IncrementTypeVersion`方法會遞增一組慣用媒體類型的版本號碼。

## <a name="syntax"></a>語法


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會遞增 [**CBasePin：： m \_ TypeVersion**](cbasepin-m-typeversion.md) 成員變數。 如果 pin 會動態變更慣用媒體類型的清單，則每當清單變更時，就會呼叫這個方法。 如需詳細資訊，請參閱 [**CBasePin：： GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




