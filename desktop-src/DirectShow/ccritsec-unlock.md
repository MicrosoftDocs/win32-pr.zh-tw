---
description: 解除鎖定方法會解除鎖定重要區段物件。
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: 'CCritSec 解除鎖定方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 919b73e5e1fc0becfb7c5fad40b87a5eb28fa008ba5cea1706373ddec9128682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074382"
---
# <a name="ccritsecunlock-method"></a>CCritSec 解除鎖定方法

**解除鎖定** 方法會解除鎖定重要區段物件。

## <a name="syntax"></a>語法


```C++
void Unlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會呼叫 [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) 函數。 針對 [**CCritSec：： Lock**](ccritsec-lock.md) 方法的每個呼叫呼叫這個方法一次。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

