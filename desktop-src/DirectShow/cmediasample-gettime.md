---
description: GetTime 方法會抓取這個範例開始和完成的資料流程時間。 這個方法會實 IMediaSample：： GetTime 方法。
ms.assetid: ddb0df1c-707d-405d-9e73-0d5a59f487b6
title: 'CMediaSample. GetTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 755965864692cf2b34ebaadc6e064a47a7514c69fe891a6a15f1bb364e5345e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655249"
---
# <a name="cmediasamplegettime-method"></a>CMediaSample. GetTime 方法

`GetTime`方法會抓取這個範例開始和完成的資料流程時間。 這個方法會實 [**IMediaSample：： GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimeStart* 
</dt> <dd>

接收開始資料流程時間之變數的指標，以 100-毫微秒單位表示。

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

接收結束資料流程時間之變數的指標，以 100-毫微秒單位表示。 如果範例沒有停止時間，此值會設定為開始時間加一。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                   | 描述                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                          | 成功。<br/>                                         |
| <dl> <dt>**VFW \_ S \_ 沒有 \_ 停止 \_ 時間**</dt> </dl>         | 範例有有效的開始時間，但沒有停止時間。<br/> |
| <dl> <dt>**\_ \_ \_ \_ 未設定 VFW E 取樣 \_ 時間**</dt> </dl> | 範例沒有有效的時間戳記。<br/>          |



 

## <a name="remarks"></a>備註

[**CMediaSample：： m \_ Start**](cmediasample-m-start.md)和 [**CMediaSample：： m \_ End**](cmediasample-m-end.md)成員變數會指定時間戳記。 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定時間戳記是否有效。

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

 

 




