---
description: 指出物件自從上次儲存至其目前資料流程之後是否已變更。
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: 'CPersistStream. IsDirty 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990246"
---
# <a name="cpersiststreamisdirty-method"></a>CPersistStream. IsDirty 方法

指出物件自從上次儲存至其目前資料流程之後是否已變更。

## <a name="syntax"></a>語法


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果篩選準則需要儲存，則傳回 [確定]， \_ 如果不需要儲存則傳回 FALSE。

## <a name="remarks"></a>備註

此成員函式會實作為 **IPersistStream：： IsDirty** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 




