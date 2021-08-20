---
description: 函式方法。 此函數會鎖定指定的重要區段物件。
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: 'CAutoLock. CAutoLock (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11267b444df319e339bcf13b30f200868a0f62d67712ed147513c2f8bc7d000c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017566"
---
# <a name="cautolockcautolock-constructor"></a>CAutoLock. CAutoLock 函數

函式方法。 此函數會鎖定指定的重要區段物件。

## <a name="syntax"></a>語法


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plock* 
</dt> <dd>

[**CCritSec**](ccritsec.md)物件的指標，其中包含重要區段物件。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAutoLock 類別**](cautolock.md)
</dt> </dl>

 

 




