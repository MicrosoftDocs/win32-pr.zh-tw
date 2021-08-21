---
description: ThreadProc 方法會從佇列中取出範例，並將其傳遞至輸入釘選。
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: 'COutputQueue. ThreadProc 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d37158d71a74726e9bf27e76ffedb076f99b7380ffcca4edfa95928767eedbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073632"
---
# <a name="coutputqueuethreadproc-method"></a>COutputQueue. ThreadProc 方法

`ThreadProc`方法會從佇列中取出範例，並將其傳遞至輸入圖釘。

## <a name="syntax"></a>語法


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回零。

## <a name="remarks"></a>備註

[**COutputQueue：： InitialThreadProc**](coutputqueue-initialthreadproc.md)方法會呼叫這個方法，它會執行主執行緒迴圈。 在迴圈中，此方法會執行下列步驟：

1.  抓取佇列的範例。
2.  如果範例是控制訊息，執行緒就會執行控制項動作。 否則，它會將範例放入 [**COutputQueue：： m \_ ppSamples**](coutputqueue-m-ppsamples.md) 陣列中。
3.  當陣列已滿 (或 [**COutputQueue：： m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) 為 **FALSE**) 時，執行緒會呼叫 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法來傳遞範例。
4.  如果未將任何範例排入佇列，執行緒就會等待 [**COutputQueue：： m \_ hSem**](coutputqueue-m-hsem.md) 信號。

當 [**COutputQueue：： m \_ bTerminate**](coutputqueue-m-bterminate.md) 成員變數變成 **TRUE** 時，執行緒就會終止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




