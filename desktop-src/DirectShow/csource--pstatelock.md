---
description: PStateLock 方法會抓取篩選準則的重要區段物件的指標。
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: 'CSource. pStateLock 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b74027e2ee2339e647938592e05162ce85108eb6985061b30a825394c2f2e7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953787"
---
# <a name="csourcepstatelock-method"></a>CSource. pStateLock 方法

**PStateLock** 方法會抓取篩選準則的重要區段物件的指標。

> [!Note]  
> 雖然命名如同成員變數，但 **pStateLock** 是一種方法。

 

## <a name="syntax"></a>語法


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CSource：： m \_ cStateLock**](csource-m-cstatelock.md) 成員變數的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 




