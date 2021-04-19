---
description: 重要區段的指標。
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'CBaseMediaFilter：： m_pLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997018"
---
# <a name="cbasemediafilterm_plock-member"></a>CBaseMediaFilter：： m \_ pLock 成員

重要區段的指標。

## <a name="syntax"></a>語法


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>備註

重要區段會在狀態轉換期間保留 ([**CBaseMediaFilter：： Run**](cbasemediafilter-run.md)、 [**CBaseMediaFilter：:P ause**](cbasemediafilter-pause.md)、 [**CBaseMediaFilter：： Stop**](cbasemediafilter-stop.md)) 、存取參考時鐘 ([**CBaseMediaFilter：： SetSyncSource**](cbasemediafilter-setsyncsource.md)、 [**CBaseMediaFilter：： GetSyncSource**](cbasemediafilter-getsyncsource.md)) 和 [**CBaseMediaFilter：： IsActive**](cbasemediafilter-isactive.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




