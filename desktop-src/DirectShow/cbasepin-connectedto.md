---
description: ConnectedTo 方法會抓取連接的 pin （如果有的話）的指標。 這個方法會實 IPin：： ConnectedTo 方法。
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: 'CBasePin. ConnectedTo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a37eafe9abf226be20cf5d573abc91bc52ee070e7667dbab3a8799f74022c92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916758"
---
# <a name="cbasepinconnectedto-method"></a>CBasePin. ConnectedTo 方法

方法會抓取 `ConnectedTo` 連接的 pin （如果有的話）的指標。 這個方法會實 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppPin* 
</dt> <dd>

接收其他 pin 之 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                           | 描述                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                  | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>             | **Null** 指標引數。<br/> |
| <dl> <dt>**VFW \_ E \_ 未 \_ 連線**</dt> </dl> | Pin 未連接。<br/>      |



 

## <a name="remarks"></a>備註

如果方法成功，則傳回的 **IPin** 介面具有未處理的參考計數。 當您完成時，請務必放開。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




