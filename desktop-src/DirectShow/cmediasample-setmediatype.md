---
description: SetMediaType 方法會設定範例的媒體類型。 這個方法會實 IMediaSample：： SetMediaType 方法。
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: 'CMediaSample. SetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977429"
---
# <a name="cmediasamplesetmediatype-method"></a>CMediaSample. SetMediaType 方法

`SetMediaType`方法會設定範例的媒體類型。 這個方法會實 [**IMediaSample：： SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaType* 
</dt> <dd>

[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | Description                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/> |



 

## <a name="remarks"></a>備註

這個方法會設定 [**CMediaSample：： m \_ pMediaType**](cmediasample-m-pmediatype.md) 成員變數（指定媒體類型），以及指定媒體類型是否已變更的 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數。

這個方法會複製 AM \_ 媒體 \_ 類型結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




