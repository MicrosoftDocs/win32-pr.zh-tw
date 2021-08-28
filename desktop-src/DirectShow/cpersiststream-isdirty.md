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
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108438"
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

 

 




