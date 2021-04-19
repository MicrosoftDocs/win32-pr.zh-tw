---
description: CheckInputType 方法會檢查輸入是否可接受指定的媒體類型。
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: 'CTransformFilter. CheckInputType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000706"
---
# <a name="ctransformfiltercheckinputtype-method"></a>CTransformFilter. CheckInputType 方法

`CheckInputType`方法會檢查輸入是否可接受指定的媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtIn* 
</dt> <dd>

指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                                | Description                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 媒體類型是可接受的。<br/>     |
| <dl> <dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt> </dl> | 媒體類型無法接受。<br/> |



 

## <a name="remarks"></a>備註

衍生的類別必須執行此方法。 \_如果可接受建議的輸入格式，則傳回 S OK，否則傳回錯誤碼。

如果有任何) ，則這個方法不需要確認輸入格式是否與輸出格式相容 (。 輸入 pin 會藉由呼叫 [**CheckTransform**](ctransformfilter-checktransform.md) 方法來確認。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




