---
description: COutputQueue。 COutputQueue 函式-函數方法。
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: 'COutputQueue. COutputQueue (Outputq. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095326"
---
# <a name="coutputqueuecoutputqueue-constructor"></a>COutputQueue. COutputQueue 函數

函式方法。

## <a name="syntax"></a>語法


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInputPin* 
</dt> <dd>

輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。 物件將會傳遞範例給此 pin。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 傳回碼的指標。 呼叫這個方法之前，請先將值設定為 S \_ OK。 傳回時， *phr* 會收到指出方法成功或失敗的值。

</dd> <dt>

*bAuto* 
</dt> <dd>

旗標，指定物件是否決定建立佇列的時機。 若 **為 TRUE**，則只有在輸入釘選可能封鎖時，物件才會建立佇列。 如果為 **FALSE**，則 *bQueue* 參數會指定是否要建立佇列。

</dd> <dt>

*bQueue* 
</dt> <dd>

如果 *bAuto* 為 **TRUE**，則會忽略此參數。 如果 *bAuto* 為 **FALSE**，此旗標會指定是否要建立佇列。

</dd> <dt>

*lBatchSize* 
</dt> <dd>

要在一個批次中傳遞的最大樣本數。

</dd> <dt>

*bBatchExact* 
</dt> <dd>

指定是否使用精確批次大小的旗標。 若 **為 TRUE**，則物件會等待 *lBatchSize* 範例，再將它們傳遞給輸入釘選。 如果 **為 FALSE**，則物件會在接收時傳遞範例。

</dd> <dt>

*lListSize* 
</dt> <dd>

佇列的快取大小。 預設值為 DEFAULTCACHE 是針對 [**CBaseList**](cbaselist.md) 類別定義的常數。

</dd> <dt>

*dwPriority* 
</dt> <dd>

傳遞範例之執行緒的優先順序。

</dd> </dl>

## <a name="remarks"></a>備註

如果 *bAuto* 為 **TRUE**，則物件會呼叫下游釘選上的 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) 方法。 如果 **ReceiveCanBlock** 傳回 S \_ OK (表示 pin 可能會在 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)) 呼叫上封鎖，則物件會建立傳遞範例的執行緒。 否則，它不會建立執行緒。

如果 *bAuto* 為 **FALSE**，則 *bQueue* 的值會決定是否要建立執行緒。

如果物件建立執行緒，則會將執行緒控制碼指派給 [**COutputQueue：： m \_ hThread**](coutputqueue-m-hthread.md) 成員變數。 執行緒程式是 [**COutputQueue：： InitialThreadProc**](coutputqueue-initialthreadproc.md)，執行緒參數是指向這個的指標。 物件也會建立用來保存範例的佇列，這是由 [**COutputQueue：： m \_ List**](coutputqueue-m-list.md) 成員變數提供。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




