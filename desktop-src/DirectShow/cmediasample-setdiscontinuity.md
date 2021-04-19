---
description: SetDiscontinuity 方法會指定此範例是否表示資料流程中的中斷。 這個方法會實 IMediaSample：： SetDiscontinuity 方法。
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: 'CMediaSample. SetDiscontinuity 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982936"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>CMediaSample. SetDiscontinuity 方法

`SetDiscontinuity`方法會指定此範例是否表示資料流程中的中斷。 這個方法會實 [**IMediaSample：： SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bDiscont* 
</dt> <dd>

指定此範例是否為不中斷的布林值。 若 **為 TRUE**，則表示媒體範例與上一個範例不連續。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定不中斷屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




