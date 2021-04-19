---
description: ChangeOutputFormat 方法會動態變更連接的媒體類型，並提供新的區段資訊。
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: 'CDynamicOutputPin. ChangeOutputFormat 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993545"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a>CDynamicOutputPin. ChangeOutputFormat 方法

`ChangeOutputFormat`方法會動態變更連接的媒體類型，並提供新的區段資訊。 當篩選圖形正在執行時，就會發生變更。 呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。 呼叫端必須確定沒有任何舊的樣本暫止。

## <a name="syntax"></a>語法


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> <dt>

*tSegmentStart* 
</dt> <dd>

區段的開始時間。

</dd> <dt>

*tSegmentStop* 
</dt> <dd>

區段的停止時間。

</dd> <dt>

*dSegmentRate* 
</dt> <dd>

區段速率。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                           | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                                                                                                      |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                | 失敗。 可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)。<br/> |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/>                                                                                                     |



 

## <a name="remarks"></a>備註

當篩選執行時，這個方法會變更格式類型。 如果下游 pin 接受新的格式，就不需要重新連接。 否則，方法會嘗試重新連接 pin。 如果方法成功變更格式，則會傳遞新的區段資訊。 這個方法會呼叫 [**CDynamicOutputPin：： ChangeMediaType**](cdynamicoutputpin-changemediatype.md) 方法來執行格式變更。

呼叫這個方法之前，您必須先呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




