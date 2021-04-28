---
description: CTransformFilter. GetMediaType 方法-GetMediaType 方法會針對輸出釘選慣用的媒體類型。
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: 'CTransformFilter. GetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095116"
---
# <a name="ctransformfiltergetmediatype-method"></a>CTransformFilter. GetMediaType 方法

方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
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



| 傳回碼                                                                                            | Description                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                   | 成功。<br/>              |
| <dl> <dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt> </dl> | 索引超出範圍。<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | 索引小於零。<br/> |



 

## <a name="remarks"></a>備註

輸出釘選的 [**CTransformOutputPin：： GetMediaType**](ctransformoutputpin-getmediatype.md) 方法會呼叫這個方法。 衍生的類別必須執行此方法。 如需詳細資訊，請參閱 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




