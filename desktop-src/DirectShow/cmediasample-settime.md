---
description: SetTime 方法會設定這個範例開始和完成時的資料流程時間。 這個方法會實 IMediaSample：： SetTime 方法。
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: 'CMediaSample. SetTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be9028db35cb6d74623bde77fac21e32793de436ea2f80d2f513687c15d1b64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156510"
---
# <a name="cmediasamplesettime-method"></a>CMediaSample. SetTime 方法

`SetTime`方法會設定這個範例開始和完成時的資料流程時間。 這個方法會實 [**IMediaSample：： SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimeStart* 
</dt> <dd>

範例開始的資料流程時間指標，以 100-毫微秒單位表示，或 **為 Null**。

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

樣本結束的資料流程時間指標，以 100-毫微秒單位表示，或 **為 Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會設定 [**CMediaSample：： m \_ Start**](cmediasample-m-start.md) 和 [**CMediaSample：： m \_ End**](cmediasample-m-end.md) 成員變數，以指定時間戳記。 它也會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定時間戳記是否有效。

如需時間戳記的詳細資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




