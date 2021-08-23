---
description: 防止其他執行緒存取執行緒的重要區段。
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'CAMThread：： m_AccessLock 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017596"
---
# <a name="camthreadm_accesslock-member"></a>CAMThread：： m \_ AccessLock 成員

防止其他執行緒存取執行緒的重要區段。

## <a name="syntax"></a>語法


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>備註

[**CAMThread：： Create**](camthread-create.md)和 [**CAMThread：： CallWorker**](camthread-callworker.md)方法會保存此鎖定，以序列化執行緒上的作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




