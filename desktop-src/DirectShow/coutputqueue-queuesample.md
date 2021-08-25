---
description: QueueSample 方法會將範例排在佇列中。
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: 'COutputQueue. QueueSample 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3770029f732629f12d94c9304d144226d873f38cc1b8452036d39ca2abdd757a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909588"
---
# <a name="coutputqueuequeuesample-method"></a>COutputQueue. QueueSample 方法

方法會將 `QueueSample` 範例排在佇列中。

## <a name="syntax"></a>語法


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會將範例新增至佇列的結尾。 在呼叫這個方法之前，請先保存重要區段，並只在物件使用執行緒來傳遞範例時呼叫它。 若要判斷物件是否使用執行緒，請呼叫 [**COutputQueue：： IsQueued**](coutputqueue-isqueued.md) 方法。

這個方法也可以用來將控制訊息放到佇列上。 控制訊息是已定義的常數 (轉換成長的 \_ PTR 型別) ，指示執行緒執行某些動作。 **COutputQueue** 類別會定義下表中顯示的控制訊息。



| 標籤 | 值 |
|---------------|----------------------------------------|
| 訊息       | 動作                                 |
| EOS 封 \_ 包   | 傳遞資料流程結束通知。 |
| 新 \_ 區段  | 傳遞新的區段。                 |
| 重設封 \_ 包 | 重設佇列的狀態。          |
| 傳送封 \_ 包  | 傳送部分範例的批次。       |



 

這是 **COutputQueue** 類別在內部使用的受保護方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




