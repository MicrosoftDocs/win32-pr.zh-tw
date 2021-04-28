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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095406"
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

 

 




