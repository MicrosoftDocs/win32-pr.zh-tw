---
description: 在取消認可操作期間會呼叫 Free 方法。
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: 'CMemAllocator 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2ffea6fdd60e4053f6c00ee1c87ca9596560909864c861d46b5728dad13a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155990"
---
# <a name="cmemallocatorfree-method"></a>CMemAllocator 方法

在 `Free` 取消認可作業期間會呼叫方法。 這個方法會執行純虛擬 [**CBaseAllocator：： Free**](cbaseallocator-free.md) 方法，但不會執行任何動作。 在 **CMemAllocator** 物件終結之前，不會實際釋放緩衝區記憶體。 「函式」方法會呼叫 [**CMemAllocator：： ReallyFree**](cmemallocator-reallyfree.md) 來釋放記憶體。

## <a name="syntax"></a>語法


```C++
void Free();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMemAllocator 類別**](cmemallocator.md)
</dt> </dl>

 

 




