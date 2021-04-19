---
description: GetMediaType 方法會依索引值抓取慣用的媒體類型。
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: 'CBasePin. GetMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987981"
---
# <a name="cbasepingetmediatype-method"></a>CBasePin. GetMediaType 方法

`GetMediaType`方法會依索引值抓取慣用的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetMediaType(
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

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                            | Description                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>              |
| <dl> <dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt> </dl> | 索引超出範圍。<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | 索引小於零。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>           | 非預期的錯誤。<br/>     |



 

## <a name="remarks"></a>備註

從 pin 的慣用媒體類型清單中，此方法會傳回索引值為 *ipositionsummaryview* 的類型。 [**CEnumMediaTypes**](cenummediatypes.md)類別會呼叫這個方法來列舉慣用的媒體類型。

基類傳回 E 非 \_ 預期的。 在您的衍生類別中覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




