---
description: GetMediaType 方法會依索引值抓取慣用的媒體類型。
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: 'CTransformOutputPin. GetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990739"
---
# <a name="ctransformoutputpingetmediatype-method"></a>CTransformOutputPin. GetMediaType 方法

`GetMediaType`方法會依索引值抓取慣用的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Ipositionsummaryview* 
</dt> <dd>

以零為基底的索引值。

</dd> <dt>

*pMediaType* 
</dt> <dd>

接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                            | Description                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | Success<br/>            |
| <dl> <dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt> </dl> | 索引超出範圍<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法。 如果篩選的輸入 pin 未連接，則方法會傳回不再有 \_ 專案的 VFW \_ \_ \_ 。 否則，它會呼叫篩選器的 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法來取得媒體類型。 **CTransformFilter：： GetMediaType** 方法是純虛擬的;篩選準則的衍生類別必須覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




