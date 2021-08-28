---
description: CCritSec. ~ CCritSec 的函式-函式方法。
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: 'CCritSec. ~ CCritSec (Wxutil 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d34665bb18a6ea9f6e76ad6332a5d7f344993067848c1b5e473893e702b62a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999608"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec. ~ CCritSec 的函式

函式方法。

## <a name="syntax"></a>語法


```C++
~CCritSec();
```



## <a name="remarks"></a>備註

這個方法會呼叫 [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) 函數來刪除重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

