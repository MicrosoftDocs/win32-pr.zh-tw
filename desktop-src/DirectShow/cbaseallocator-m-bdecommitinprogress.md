---
description: 旗標，指出取消認可作業是否正在進行中。
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'CBaseAllocator：： m_bDecommitInProgress 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6d73514ffbe2b6e2430230e64ccfa9006809523a95cd3220ca078d4c4e40f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017536"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>CBaseAllocator：： m \_ bDecommitInProgress 成員

旗標，指出取消認可作業是否正在進行中。 在呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md)方法之後，但在釋放所有緩衝區之前，此值為 **TRUE** 。 如果值為 **TRUE**， [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法將會失敗。 此外，在值為 **TRUE** 時，配置器不應該刪除本身。

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




