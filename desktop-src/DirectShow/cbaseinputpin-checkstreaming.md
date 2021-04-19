---
description: 判斷 pin 是否可以接受範例。
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: 'CBaseInputPin. CheckStreaming 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975733"
---
# <a name="cbaseinputpincheckstreaming-method"></a>CBaseInputPin. CheckStreaming 方法

判斷 pin 是否可以接受範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                                           | Description                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                   |
| <dl> <dt>**S \_ FALSE**</dt> </dl>               | Pin 目前正在排清。<br/> |
| <dl> <dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt> </dl> | 發生執行階段錯誤。<br/> |
| <dl> <dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt> </dl>   | 已停止 pin。<br/>        |



 

## <a name="remarks"></a>備註

衍生類別可以覆寫這個方法，以執行進一步的檢查。 在覆寫方法中，也呼叫基類執行。

[**CBaseInputPin：： Receive 方法會**](cbaseinputpin-receive.md)呼叫這個方法。 您也應該覆寫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法，以呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> </dl>

 

 




