---
description: CBaseAllocator. ~ CBaseAllocator 的函式-函式方法。
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096416"
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

 

 




