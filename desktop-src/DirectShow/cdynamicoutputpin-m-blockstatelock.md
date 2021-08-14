---
description: 保護封鎖狀態的重要區段。
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'CDynamicOutputPin：： m_BlockStateLock 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa5382a30dcd434965c53e893d6818ab0f08a84c19ea0ddec53846c0c01c80f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656678"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>CDynamicOutputPin：： m \_ BlockStateLock 成員

保護封鎖狀態的重要區段。

## <a name="syntax"></a>語法


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>備註

使用下列任何成員變數之前，請先保留此重要區段：

-   [**CDynamicOutputPin：： m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)
-   [**CDynamicOutputPin：： m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**CDynamicOutputPin：： m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**CDynamicOutputPin：： m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




