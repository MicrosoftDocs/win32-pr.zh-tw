---
description: DynamicReconnect 方法會以新的媒體類型執行動態重新連接。 當篩選圖形正在執行時，就會發生重新連接。
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: 'CDynamicOutputPin. DynamicReconnect 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986783"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>CDynamicOutputPin. DynamicReconnect 方法

`DynamicReconnect`方法會以新的媒體類型執行動態重新連接。 當篩選圖形正在執行時，就會發生重新連接。

## <a name="syntax"></a>語法


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                                                                                                                                 |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 失敗。 可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 方法。<br/> |



 

## <a name="remarks"></a>備註

您必須從將資料傳遞至 pin 的相同執行緒呼叫這個方法。 呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。 呼叫端必須確定沒有任何舊的樣本暫止。

呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) ，然後再呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




