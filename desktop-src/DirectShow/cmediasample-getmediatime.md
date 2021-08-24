---
description: GetMediaTime 方法會捕獲此範例的媒體時間。 這個方法會實 IMediaSample：： GetMediaTime 方法。
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: 'CMediaSample. GetMediaTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634678"
---
# <a name="cmediasamplegetmediatime-method"></a>CMediaSample. GetMediaTime 方法

`GetMediaTime`方法會捕獲此範例的媒體時間。 這個方法會實 [**IMediaSample：： GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStart* 
</dt> <dd>

接收媒體開始時間之變數的指標。

</dd> <dt>

*暫止* 
</dt> <dd>

接收媒體停止時間之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                  | 描述                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                                 |
| <dl> <dt>**\_ \_ \_ \_ 未設定 VFW E 媒體 \_ 時間**</dt> </dl> | 未設定此範例的媒體時間。<br/> |



 

## <a name="remarks"></a>備註

[**CMediaSample：： m \_ MediaEnd**](cmediasample-m-mediaend.md)成員變數會指定從 [**CMediaSample：： m \_ MediaStart**](cmediasample-m-mediastart.md)的位移，但由 *暫* 止參數接收的值是絕對媒體時間，以 **m \_ MediaStart**  +  **m \_ MediaEnd** 計算。

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

 

 




