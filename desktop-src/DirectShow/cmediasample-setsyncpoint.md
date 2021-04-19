---
description: SetSyncPoint 方法會指定此範例的開頭是否為同步處理點。 這個方法會實 IMediaSample：： SetSyncPoint 方法。
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: 'CMediaSample. SetSyncPoint 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991538"
---
# <a name="cmediasamplesetsyncpoint-method"></a>CMediaSample. SetSyncPoint 方法

`SetSyncPoint`方法會指定此範例的開頭是否為同步處理點。 這個方法會實 [**IMediaSample：： SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bIsSyncPoint* 
</dt> <dd>

指定這是否為同步處理點的布林值。 若 **為 TRUE**，表示這是同步處理點。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會更新 [**CMediaSample：： m \_ dwFlags**](cmediasample-m-dwflags.md) 成員變數，以指定同步處理點屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaSample 類別**](cmediasample.md)
</dt> </dl>

 

 




