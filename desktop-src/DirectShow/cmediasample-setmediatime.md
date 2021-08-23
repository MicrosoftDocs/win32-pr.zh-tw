---
description: SetMediaTime 方法會設定此範例的媒體時間。 這個方法會實 IMediaSample：： SetMediaTime 方法。
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: 'CMediaSample. SetMediaTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3709a5f487855148b8ad4042f61b74fbe6029ef64e00b751672bf478f1da866e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016366"
---
# <a name="cmediasamplesetmediatime-method"></a>CMediaSample. SetMediaTime 方法

`SetMediaTime`方法會設定此範例的媒體時間。 這個方法會實 [**IMediaSample：： SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

媒體開始時間的指標，或 **為 Null**。

</dd> <dt>

*暫止* 
</dt> <dd>

媒體停止時間的指標，或 **為 Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

媒體停止時間必須大於媒體開始時間。 使用 **Null** 來使媒體時間失效。

*暫* 止的參數會指定絕對媒體時間，但 [**CMediaSample：： m \_ MediaEnd**](cmediasample-m-mediaend.md)成員變數會計算為 *pStart* 的位移。 換句話說， **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*。  

如需媒體時間的相關資訊，請參閱[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




