---
description: CBaseOutputPin. EndOfStream 方法-EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: 'CBaseOutputPin. EndOfStream 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93ba617ddb061a928236e9bbf7d7a411812809092efa8a71f5890ddeecb88328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823597"
---
# <a name="cbaseoutputpinendofstream-method"></a>CBaseOutputPin. EndOfStream 方法

`EndOfStream`方法會通知 pin，不需要任何其他資料。 這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 E 非 \_ 預期的。

## <a name="remarks"></a>備註

這個方法應該只在輸入圖釘上呼叫，因此 **CBaseOutputPin** 的執行會傳回非 \_ 預期的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




