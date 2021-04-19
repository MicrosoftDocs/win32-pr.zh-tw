---
description: 中斷連接方法會中斷目前的 pin 連線。 這個方法會實 IPin：:D isconnect 方法。
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: 'CDynamicOutputPin 連接方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65c61ecc825d703976aa3163be5922da1ac4471a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000938"
---
# <a name="cdynamicoutputpindisconnect-method"></a>CDynamicOutputPin 中斷方法

`Disconnect`方法會中斷目前的 pin 連接。 這個方法會實 [**IPin：:D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | Description                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Pin 未連接。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                   |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：:D isconnect**](cbasepin-disconnect.md) 方法，以在篩選作用中時啟用中斷連接。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




