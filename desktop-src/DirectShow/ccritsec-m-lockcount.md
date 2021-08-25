---
description: 此物件上的未完成鎖定數目。
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'CCritSec：： m_lockCount 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9885f3270c021432342605ad84c1b521672022f4a13cecac5ac49c9248c65d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872208"
---
# <a name="ccritsecm_lockcount-member"></a>CCritSec：： m \_ lockCount 成員

此物件上的未完成鎖定數目。

## <a name="syntax"></a>語法


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>備註

這個成員變數只會在基類的 debug 版本中定義。 [重要區段調試](critical-section-debugging-functions.md)函式函數會使用這個成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

 




