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
ms.openlocfilehash: d9a283867036254b7a13b45ba152c3f16ecccbdb59d4d59e98c8d1dae7480e13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634218"
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

 

 




