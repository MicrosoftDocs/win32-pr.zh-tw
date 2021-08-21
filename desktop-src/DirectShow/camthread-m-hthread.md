---
description: 執行緒的控制碼。
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'CAMThread：： m_hThread 成員 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158909"
---
# <a name="camthreadm_hthread-member"></a>CAMThread：： m \_ hThread 成員

執行緒的控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>備註

這個變數會初始化為 **Null**。 [**CAMThread：： Create**](camthread-create.md)方法會將這個變數設定為執行緒控制碼。 若要判斷線程是否存在，請呼叫 [**CAMThread：： ThreadExists**](camthread-threadexists.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




