---
description: 鎖定方法會鎖定重要區段物件。
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: 'CCritSec： Lock 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4241b2cd5e94fbd6a3cbe0abd91d47ad6312c44b71f76c214cffb22836033a7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928587"
---
# <a name="ccritseclock-method"></a>CCritSec Lock 方法

**鎖定** 方法會鎖定重要區段物件。

## <a name="syntax"></a>語法


```C++
void Lock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會呼叫 [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) 函數。

呼叫 [**CCritSec：： unlock**](ccritsec-unlock.md) 成員函式，以將重要區段解除鎖定。 您可以對相同執行緒上的 **鎖定** 方法進行多次呼叫;請務必呼叫 **解除鎖定** 對應的次數。

如果物件已經由另一個執行緒鎖定， **CCritSec：： Lock** 方法會封鎖，直到釋放物件為止，或直到發生可能的鎖死例外狀況為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

