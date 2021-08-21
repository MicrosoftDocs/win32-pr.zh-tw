---
description: IsSyncPoint 方法會判斷範例的開頭是否為同步處理點。 這個方法會實 IMediaSample：： IsSyncPoint 方法。
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: 'CMediaSample. IsSyncPoint 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00d238bb9289ba71237bfdf8e72acde384430f72470f16211093cb2ece8d68f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074002"
---
# <a name="cmediasampleissyncpoint-method"></a>CMediaSample. IsSyncPoint 方法

`IsSyncPoint`方法會判斷範例的開頭是否為同步處理點。 這個方法會實 [**IMediaSample：： IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果範例是同步處理點，則傳回 s OK， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




