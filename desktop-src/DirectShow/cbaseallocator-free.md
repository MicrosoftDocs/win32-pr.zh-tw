---
description: Free 方法會釋放所有緩衝區記憶體。 當主控篩選器在最後一個媒體樣本釋出之後解除配置器時，就會呼叫這個方法。
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: 'CBaseAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995939"
---
# <a name="cbaseallocatorfree-method"></a>CBaseAllocator 方法

`Free`方法會釋放所有緩衝區記憶體。 當主控篩選器在最後一個媒體樣本釋出之後解除配置器時，就會呼叫這個方法。

## <a name="syntax"></a>語法


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

呼叫 [**取消認可**](cbaseallocator-decommit.md) 方法之後，配置器會在釋放最後一個媒體範例時呼叫這個方法。 衍生的類別必須執行此方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




