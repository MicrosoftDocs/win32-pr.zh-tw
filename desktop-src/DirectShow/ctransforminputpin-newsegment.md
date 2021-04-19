---
description: NewSegment 方法會在此呼叫群組為區段之後，通知 pin 所收到的媒體範例。 這個方法會實 IPin：： NewSegment 方法。
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: 'CTransformInputPin. NewSegment 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989683"
---
# <a name="ctransforminputpinnewsegment-method"></a>CTransformInputPin. NewSegment 方法

`NewSegment`方法會通知釘選在此呼叫群組為區段之後所收到的媒體範例。 這個方法會實 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。

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

區段的開始時間。

</dd> <dt>

*tStop* 
</dt> <dd>

區段的停止時間。

</dd> <dt>

*dRate* 
</dt> <dd>

區段的速率。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： NewSegment**](ctransformfilter-newsegment.md) 方法，以傳遞下游的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




