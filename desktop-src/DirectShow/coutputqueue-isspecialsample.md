---
description: IsSpecialSample 方法會判斷佇列資料是否為控制訊息。
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: 'COutputQueue. IsSpecialSample 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995646"
---
# <a name="coutputqueueisspecialsample-method"></a>COutputQueue. IsSpecialSample 方法

`IsSpecialSample`方法會判斷佇列資料是否為控制訊息。

## <a name="syntax"></a>語法


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSample* 
</dt> <dd>

佇列中專案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *pSample* 是控制訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

[**COutputQueue：： QueueSample**](coutputqueue-queuesample.md)方法除了媒體範例之外，還可以接收控制訊息。 控制訊息是已定義的常數 (轉換成長的 \_ PTR 類型) ，指示執行緒執行動作。 控制訊息不包含媒體資料。 如需詳細資訊，請參閱 **COutputQueue：： QueueSample**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




