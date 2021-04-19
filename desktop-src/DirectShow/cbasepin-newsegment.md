---
description: NewSegment 方法會在此呼叫群組為區段之後，通知 pin 所收到的媒體範例。 實行 IPin：： NewSegment 方法。
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: 'CBasePin. NewSegment 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994309"
---
# <a name="cbasepinnewsegment-method"></a>CBasePin. NewSegment 方法

`NewSegment`方法會通知釘選在此呼叫群組為區段之後所收到的媒體範例。 實行 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

區段的開始媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*tStop* 
</dt> <dd>

區段的結束媒體位置，以 100-毫微秒單位表示。

</dd> <dt>

*dRate* 
</dt> <dd>

此區段的處理速率（以原始費率的百分比表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會設定 [**CBasePin：： m \_ tStart**](cbasepin-m-tstart.md)、 [**CBasePin：： m \_ tStop**](cbasepin-m-tstop.md)和 [**CBasePin：： m \_ dRate**](cbasepin-m-drate.md) 成員變數。 在您的衍生類別中，覆寫這個方法以傳遞通知下游。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




