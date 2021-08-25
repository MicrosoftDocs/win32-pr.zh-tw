---
description: DisconnectInternal 方法會中斷目前的 pin 連接。
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: 'CBasePin. DisconnectInternal 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916528"
---
# <a name="cbasepindisconnectinternal-method"></a>CBasePin. DisconnectInternal 方法

`DisconnectInternal`方法會中斷目前的 pin 連接。

## <a name="syntax"></a>語法


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                         | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | Pin 未連接。<br/>                                              |
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 成功。<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl> | 篩選準則為使用中，且 pin 不支援動態重新連接。<br/> |



 

## <a name="remarks"></a>備註

[**CBasePin：:D isconnect**](cbasepin-disconnect.md)方法會將中斷進程委派給這個方法。 這個方法會呼叫 [**CBasePin：： BreakConnect**](cbasepin-breakconnect.md) 方法。 此外，它也會釋放其他 pin 的參考計數，由 [**CBasePin：： m \_ 連接**](cbasepin-m-connected.md) 的成員變數所持有。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




