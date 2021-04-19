---
description: ChangeMediaType 方法會動態變更連接的媒體類型。
ms.assetid: 38efdfdc-f636-4cad-b8d3-8c63a277644e
title: 'CDynamicOutputPin. ChangeMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89c15e3076a95f8fee3f2f2970fc59da5cf3bf4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001002"
---
# <a name="cdynamicoutputpinchangemediatype-method"></a>CDynamicOutputPin. ChangeMediaType 方法

`ChangeMediaType`方法會動態變更連接的媒體類型。 當篩選圖形正在執行時，就會發生變更。 呼叫這個方法之後，就無法傳遞具有舊媒體類型的範例。 呼叫端必須確定沒有任何舊的樣本暫止。

## <a name="syntax"></a>語法


```C++
HRESULT ChangeMediaType(
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



| 傳回碼                                                                                           | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                                                                                                                      |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                | 失敗。 可能是擁有篩選未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)。<br/> |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/>                                                                                                     |



 

## <a name="remarks"></a>備註

呼叫這個方法之前，請先呼叫 [**CDynamicOutputPin：： StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) 方法。

這個方法會先檢查下游輸入 pin 是否可以接受新的格式，而不需要重新連接。 它會查詢 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面的輸入 pin。 如果輸入 pin 支援 **IPinConnection**，此方法會以建議的媒體類型呼叫 [**IPinConnection：:D ynamicqueryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipinconnection-dynamicqueryaccept) 方法。 如果輸入 pin 接受新的媒體類型，方法會呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法，並重新協商配置器需求。

另一方面，如果下游 pin 不支援 **IPinConnection**，或者它拒絕新的媒體類型，則方法會呼叫 [**CDynamicOutputPin：:D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) 方法來執行動態重新連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




