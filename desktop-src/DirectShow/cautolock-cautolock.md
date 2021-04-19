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
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998614"
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

 

 




