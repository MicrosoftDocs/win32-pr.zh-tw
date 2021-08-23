---
description: CMemAllocator. ~ CMemAllocator 的函式-函式方法。
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: 'CMemAllocator. ~ CMemAllocator (Amfilter 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954377"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>CMemAllocator. ~ CMemAllocator 的函式

函式方法。

## <a name="syntax"></a>語法


```C++
~CMemAllocator();
```



## <a name="remarks"></a>備註

這個方法會覆寫基類的函式，以呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 和 [**CMemAllocator：： ReallyFree**](cmemallocator-reallyfree.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMemAllocator 類別**](cmemallocator.md)
</dt> </dl>

 

 




