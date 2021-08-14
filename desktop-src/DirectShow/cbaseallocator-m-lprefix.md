---
description: 每個緩衝區的前置詞（以位元組為單位）。
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'CBaseAllocator：： m_lPrefix 成員 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a22f2ac1a54c4820f109b55002428c87df321328ef6b6b6d6096343df8cde85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955287"
---
# <a name="cbaseallocatorm_lprefix-member"></a>CBaseAllocator：： m \_ lPrefix 成員

每個緩衝區的前置詞（以位元組為單位）。 如果此值不是零， [**CBaseAllocator：： GetBuffer**](cbaseallocator-getbuffer.md) 方法所傳回的每個緩衝區指標前面都會加上大小為 *m \_ lPrefix* 的位元組區塊。 這個記憶體區塊稱為 *前置* 詞。 [**CBaseAllocator：： m \_ lSize**](cbaseallocator-m-lsize.md)成員變數不包含前置詞值。

## <a name="syntax"></a>Syntax


```C++
long m_lPrefix;
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

 

 




