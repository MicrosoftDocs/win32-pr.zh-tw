---
description: 如果媒體類型與先前的範例不同，則 GetMediaType 方法會抓取媒體類型。 這個方法會實 IMediaSample：： GetMediaType 方法。
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: 'CMediaSample. GetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee7b5464ff2620dbc0247b006dc323232131de3936d2c5e56f2232b67c00ba5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832298"
---
# <a name="cmediasamplegetmediatype-method"></a>CMediaSample. GetMediaType 方法

`GetMediaType`如果媒體類型與先前的範例不同，則方法會抓取媒體類型。 這個方法會實 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppMediaType* 
</dt> <dd>

接收 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標的變數位址。 如果媒體類型尚未從上一個範例變更， *\* ppMediaType* 會設為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | 描述                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | 媒體類型尚未從上一個範例變更。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                     |



 

## <a name="remarks"></a>備註

當您完成媒體類型時，請呼叫 [**DeleteMediaType**](deletemediatype.md) 公用程式函式來釋放記憶體區塊。

[**CMediaSample：： m \_ pMediaType**](cmediasample-m-pmediatype.md)成員變數會指定媒體類型。 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數指定媒體類型是否已變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




