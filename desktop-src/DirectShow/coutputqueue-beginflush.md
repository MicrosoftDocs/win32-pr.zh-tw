---
description: COutputQueue. BeginFlush 方法-BeginFlush 方法開始進行清除作業。
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: 'COutputQueue. BeginFlush 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099026"
---
# <a name="coutputqueuebeginflush-method"></a>COutputQueue. BeginFlush 方法

`BeginFlush`方法會開始清除作業。

## <a name="syntax"></a>語法


```C++
void BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會將 [**COutputQueue：： m \_ bFlushing**](coutputqueue-m-bflushing.md) 成員變數設定為 **TRUE**。 如果物件使用執行緒，執行緒會呼叫 [**COutputQueue：： FreeSamples**](coutputqueue-freesamples.md) 方法來釋放任何暫止的樣本。 否則，物件會在 [**COutputQueue：： EndFlush**](coutputqueue-endflush.md)方法期間呼叫 **FreeSamples** 。 這個方法也會將 [**COutputQueue：： m \_ hr**](coutputqueue-m-hr.md) 成員變數設定為 \_ FALSE，這會導致物件捨棄所有新的範例。

物件會在輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法，以傳遞排清通知。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




