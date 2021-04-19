---
description: SetMediaType 方法會設定連接的媒體類型。
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: 'CTransformOutputPin. SetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45bd16f0c0e5ea9cd1e719518fab15180177fd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984444"
---
# <a name="ctransformoutputpinsetmediatype-method"></a>CTransformOutputPin. SetMediaType 方法

`SetMediaType`方法會設定連接的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： SetMediaType**](cbasepin-setmediatype.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： SetMediaType**](ctransformfilter-setmediatype.md) 方法來通知篩選。

Pin 必須在呼叫這個方法之前，先確認媒體類型是可接受的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




