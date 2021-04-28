---
description: COutputQueue. EndFlush 方法-EndFlush 方法會結束清除作業。
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: 'COutputQueue. EndFlush 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099006"
---
# <a name="coutputqueueendflush-method"></a>COutputQueue. EndFlush 方法

`EndFlush`方法會結束清除作業。

## <a name="syntax"></a>語法


```C++
void EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果物件使用執行緒，這個方法會等候 [**COutputQueue：： m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) 事件。 執行緒釋放任何暫止的樣本之後，會對此事件發出信號。 如果物件不是使用執行緒，這個方法會呼叫 [**COutputQueue：： FreeSamples**](coutputqueue-freesamples.md) 方法。 然後， `EndFlush` 方法會在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




