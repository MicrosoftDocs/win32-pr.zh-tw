---
description: SetActualDataLength 方法會設定緩衝區中有效資料的長度。 這個方法會實 IMediaSample：： SetActualDataLength 方法。
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: 'CMediaSample. SetActualDataLength 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978615"
---
# <a name="cmediasamplesetactualdatalength-method"></a>CMediaSample. SetActualDataLength 方法

`SetActualDataLength`方法會設定緩衝區中有效資料的長度。 這個方法會實 [**IMediaSample：： SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lLen* 
</dt> <dd>

有效資料的長度（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                             | Description                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                                         |
| <dl> <dt>**VFW \_ E \_ 緩衝區 \_ 溢出**</dt> </dl> | *lLen* 大於配置的緩衝區大小。<br/> |



 

## <a name="remarks"></a>備註

這個方法會設定 [**CMediaSample：： m \_ lActual**](cmediasample-m-lactual.md) 成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




