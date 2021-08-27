---
description: CBasePin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: 'CBasePin. BreakConnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c40c7614f94b2be5e5f588a706b4b0bd1eec92c3181ffbedcad3ae1e57183f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955227"
---
# <a name="cbasepinbreakconnect-method"></a>CBasePin. BreakConnect 方法

`BreakConnect`方法會從連接釋放 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBasePin：:D isconnect**](cbasepin-disconnect.md)方法在 pin 中斷連接期間會呼叫這個方法。 如果 [**CBasePin：： CheckConnect**](cbasepin-checkconnect.md) 方法失敗，也會在嘗試連接期間呼叫此方法。

這個方法必須釋放 **CheckConnect** 方法所取得的任何資源。 例如，如果 **CheckConnect** 配置記憶體，則 `BreakConnect` 應該釋放記憶體。 如果 **CheckConnect** 查詢介面的連接 pin，則 `BreakConnect` 應該釋放介面。

請注意，您 `BreakConnect` 可以呼叫，而不需要對應的 **CompleteConnect** 呼叫。 因此，您無法假設先前已呼叫過 **CompleteConnect** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




