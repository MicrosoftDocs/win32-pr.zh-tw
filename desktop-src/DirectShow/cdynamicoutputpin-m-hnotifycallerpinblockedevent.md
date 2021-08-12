---
description: 當 pin 成功封鎖或使用者取消暫止的區塊時，會發出信號的事件。
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'CDynamicOutputPin：： m_hNotifyCallerPinBlockedEvent 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656403"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>CDynamicOutputPin：： m \_ hNotifyCallerPinBlockedEvent 成員

當 pin 成功封鎖或使用者取消暫止的區塊時，會發出信號的事件。

## <a name="syntax"></a>語法


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
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

 

 




