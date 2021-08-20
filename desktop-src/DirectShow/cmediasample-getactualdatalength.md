---
description: GetActualDataLength 方法會擷取緩衝區中有效資料的長度。 這個方法會實 IMediaSample：： GetActualDataLength 方法。
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: 'CMediaSample. GetActualDataLength 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d41c23e45ba65416a0f57336e51d2784b194ee556a778b7036e8dc5fd829ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016386"
---
# <a name="cmediasamplegetactualdatalength-method"></a>CMediaSample. GetActualDataLength 方法

`GetActualDataLength`方法會擷取緩衝區中有效資料的長度。 這個方法會實 [**IMediaSample：： GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) 方法。

## <a name="syntax"></a>語法


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回有效資料的長度（以位元組為單位）。

## <a name="remarks"></a>備註

[**CMediaSample：： m \_ lActual**](cmediasample-m-lactual.md)成員變數會指定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

