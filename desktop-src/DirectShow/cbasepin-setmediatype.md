---
description: CBasePin. SetMediaType 方法-SetMediaType 方法會設定連接的媒體類型。
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: 'CBasePin. SetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095983"
---
# <a name="cbasepinsetmediatype-method"></a>CBasePin. SetMediaType 方法

`SetMediaType`方法會設定連接的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會建立 pin 連接的格式。 在呼叫這個方法之前，pin 會呼叫 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法，以判斷是否可接受媒體類型。 因此，會假設 *pmt* 參數是可接受的媒體類型。

在基類中，這個方法會設定 [**CBasePin：： m \_ mt**](cbasepin-m-mt.md) 成員變數，並傳回 S \_ OK。 如果在設定媒體類型時需要通知，則衍生類別可以覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




