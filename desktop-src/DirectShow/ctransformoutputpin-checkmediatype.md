---
description: CTransformOutputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: 'CTransformOutputPin. CheckMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3894e701b22f6380e591eccf978e84a1321f57a84485cea8a6e3116181f3f2c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538458"
---
# <a name="ctransformoutputpincheckmediatype-method"></a>CTransformOutputPin. CheckMediaType 方法

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

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 篩選的輸入 pin 未連接。<br/> |



 

## <a name="remarks"></a>備註

這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。 如果篩選的輸入 pin 未連接，則方法會失敗。 否則，它會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，這也是純虛擬的方法。 篩選準則的衍生類別必須執行 **CheckTransform**，以判斷提議的輸出媒體類型是否與輸入媒體類型相容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




