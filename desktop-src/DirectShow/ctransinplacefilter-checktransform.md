---
description: CheckTransform 方法會檢查輸入媒體類型是否與輸出媒體類型相容。 這個方法會覆寫 CTransformFilter：： CheckTransform 方法。
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: 'CTransInPlaceFilter. CheckTransform 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49b7f4aaac21cf6a55360e2e1b970bd9dfa62c0422241f7356871117e138d57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654957"
---
# <a name="ctransinplacefilterchecktransform-method"></a>CTransInPlaceFilter. CheckTransform 方法

`CheckTransform`方法會檢查輸入媒體類型是否與輸出媒體類型相容。 這個方法會覆寫 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mtIn* 
</dt> <dd>

指定輸入類型之 [**CMediaType**](cmediatype.md) 物件的指標。

</dd> <dt>

*mtOut* 
</dt> <dd>

指定輸出類型之 **CMediaType** 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

**CTransInPlace** 篩選準則永遠不會呼叫 `CheckTransform` 。 相反地，所有 pin 連接都會使用 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 來檢查媒體類型，並假設輸入和輸出類型一律相符。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




