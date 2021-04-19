---
description: IsDiscontinuity 方法會判斷此範例是否表示資料流程中的中斷。 這個方法會實 IMediaSample：： IsDiscontinuity 方法。
ms.assetid: 125b4a86-bd26-4539-a9ab-281f1aed1836
title: 'CMediaSample. IsDiscontinuity 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e222ea813793dd537c8623f74403baed9a320a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982923"
---
# <a name="cmediasampleisdiscontinuity-method"></a>CMediaSample. IsDiscontinuity 方法

`IsDiscontinuity`方法會判斷此範例是否代表資料流程中的中斷點。 這個方法會實 [**IMediaSample：： IsDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-isdiscontinuity) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsDiscontinuity();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果範例是資料流程中的中斷，則傳回 s OK， \_ 否則傳回 FALSE。

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

 

 




