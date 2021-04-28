---
description: CTransformInputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: 'CTransformInputPin. CheckMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084996"
---
# <a name="ctransforminputpincheckmediatype-method"></a>CTransformInputPin. CheckMediaType 方法

`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtIn* 
</dt> <dd>

[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法，這也是純虛擬的方法。 篩選準則的衍生類別必須執行 **CheckInputType** ，以判斷指定的輸入類型是否可接受。

如果篩選的輸出連接已連接，這個方法也會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，以判斷輸入類型是否與輸出類型相容。 **CheckTransform** 方法也是單純的虛擬。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




