---
description: GetSize 方法會擷取緩衝區的大小。 這個方法會實 IMediaSample：： GetSize 方法。
ms.assetid: 14562ef4-f554-4d5a-83d3-1a29abae08a4
title: 'CMediaSample. GetSize 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3559f972f35a01738c60f32414ab0b42a079032ac5bc6b3ab0e5b7212900d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156749"
---
# <a name="cmediasamplegetsize-method"></a>CMediaSample. GetSize 方法

`GetSize`方法會擷取緩衝區的大小。 這個方法會實 [**IMediaSample：： GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize) 方法。

## <a name="syntax"></a>語法


```C++
LONG GetSize();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回緩衝區的大小（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




