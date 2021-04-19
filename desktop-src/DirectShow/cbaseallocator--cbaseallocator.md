---
description: 函式方法。
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: 'CBaseAllocator. ~ CBaseAllocator (Amfilter 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976761"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>CBaseAllocator. ~ CBaseAllocator 的函式

函式方法。

## <a name="syntax"></a>語法


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>備註

在終結物件之前，請一律呼叫 [**CBaseAllocator：:D ecommit**](cbaseallocator-decommit.md) 方法。 基類的函式無法呼叫 **取消認可**，因為該方法會呼叫純虛擬方法 [**CBaseAllocator：： Free**](cbaseallocator-free.md)。 衍生類別應該覆寫這個函式並呼叫 **取消認可**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 




