---
description: CTransInPlaceFilter. GetMediaType 方法-GetMediaType 方法會針對輸出釘選慣用的媒體類型。
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: 'CTransInPlaceFilter. GetMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a714d3dba30b3038d6c04ecedd51db4196a3c4d899d7c607dd12f9a068f8a803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079298"
---
# <a name="ctransinplacefiltergetmediatype-method"></a>CTransInPlaceFilter. GetMediaType 方法

方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。

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

傳回 E 非 \_ 預期的。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法。 在 **CTransInPlaceFilter** 類別中，每個圖釘都會呼叫相對的連線 pin 來列舉慣用的媒體類型。 輸入的 pin 會呼叫下游篩選器的輸入 pin，而且輸出 pin 會呼叫上游篩選器的輸出 pin。 因此永遠不會呼叫篩選的 `GetMediaType` 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




