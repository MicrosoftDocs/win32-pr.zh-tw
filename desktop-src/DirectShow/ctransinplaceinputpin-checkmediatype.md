---
description: CTransInPlaceInputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: 'CTransInPlaceInputPin. CheckMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91a1889e9c8a4060b734449df9f73474c16d1aec09d6534de048359ced156958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654840"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>CTransInPlaceInputPin. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Pmt* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果建議的媒體類型是可接受的，則傳回 S OK。 否則，會傳回 \_ FALSE 或錯誤碼。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CTransformInputPin：： CheckMediaType**](ctransforminputpin-checkmediatype.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查輸入類型。 如果輸出連接已連線，此方法也會在下游輸入 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




