---
description: 要提供的緩衝區數目。
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'CBaseAllocator：： m_lCount 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989881"
---
# <a name="cbaseallocatorm_lcount-member"></a>CBaseAllocator：： m \_ lCount 成員

要提供的緩衝區數目。 [**CBaseAllocator：： SetProperties**](cbaseallocator-setproperties.md)方法會設定此值。 在呼叫 [**CBaseAllocator：： Commit**](cbaseallocator-commit.md) 方法之前，不會配置緩衝區。 目前已配置的緩衝區數是由 [**CBaseAllocator：： m \_ lAllocated**](cbaseallocator-m-lallocated.md) 成員變數所指定。

## <a name="syntax"></a>Syntax


```C++
long m_lCount;
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

 

 




