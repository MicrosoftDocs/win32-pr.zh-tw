---
description: NewSegment 方法會通知篩選此呼叫之後所收到的媒體範例會分組為區段。
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: 'CTransformFilter. NewSegment 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953547"
---
# <a name="ctransformfilternewsegment-method"></a>CTransformFilter. NewSegment 方法

`NewSegment`方法會在此呼叫群組為區段之後，通知篩選出所收到的媒體範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tStart* 
</dt> <dd>

相對於原始來源之區段的開始時間。

</dd> <dt>

*tStop* 
</dt> <dd>

相對於原始來源之區段的停止時間。

</dd> <dt>

*dRate* 
</dt> <dd>

應處理區段的速率。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

輸入釘選的 [**CTransformInputPin：： NewSegment**](ctransforminputpin-newsegment.md) 方法會呼叫這個方法。 這個方法會傳遞對 `NewSegment` 下游輸入 pin 的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




