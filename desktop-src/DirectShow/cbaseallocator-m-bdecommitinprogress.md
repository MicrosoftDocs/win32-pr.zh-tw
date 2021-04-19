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
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978642"
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

 

 




