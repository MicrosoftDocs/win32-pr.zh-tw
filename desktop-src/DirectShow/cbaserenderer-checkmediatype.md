---
description: CheckMediaType 方法會判斷篩選是否接受特定的媒體類型。
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: 'CBaseRenderer. CheckMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997008"
---
# <a name="cbaserenderercheckmediatype-method"></a>CBaseRenderer. CheckMediaType 方法

`CheckMediaType`方法會判斷篩選準則是否接受特定的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
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

輸入 pin 會從它自己的 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法呼叫這個方法。 衍生的類別必須執行此方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




