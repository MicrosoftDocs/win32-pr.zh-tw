---
description: 此 pin 上最後一次呼叫 IPinFlowControl：： Block 方法之執行緒的識別碼。 只有當 pin 遭到封鎖時，此成員變數才有效。
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'CDynamicOutputPin：： m_dwBlockCallerThreadID 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996094"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>CDynamicOutputPin：： m \_ dwBlockCallerThreadID 成員

此 pin 上最後一次呼叫 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 方法之執行緒的識別碼。 只有當 pin 遭到封鎖時，此成員變數才有效。

## <a name="syntax"></a>語法


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>備註

存取此變數之前，請先保留 [**CDynamicOutputPin：： m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) 重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




