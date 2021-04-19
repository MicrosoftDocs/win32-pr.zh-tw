---
description: IsPreroll 方法會判斷此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 IMediaSample：： IsPreroll 方法。
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: 'CMediaSample. IsPreroll 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995915"
---
# <a name="cmediasampleispreroll-method"></a>CMediaSample. IsPreroll 方法

`IsPreroll`方法會判斷此範例是否為可提前取樣。 不應顯示預先提供的範例。 這個方法會實 [**IMediaSample：： IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果此範例是一個預先進行的範例，則傳回 [確定]， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

[**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md)成員變數會指定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




