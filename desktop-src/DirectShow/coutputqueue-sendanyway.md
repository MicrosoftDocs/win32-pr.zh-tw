---
description: SendAnyway 方法會提供任何暫止的範例。
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: 'COutputQueue. SendAnyway 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986174"
---
# <a name="coutputqueuesendanyway-method"></a>COutputQueue. SendAnyway 方法

`SendAnyway`方法會提供任何暫止的範例。

## <a name="syntax"></a>語法


```C++
void SendAnyway();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 [**COutputQueue：： m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) 成員變數為 **TRUE**，則物件會先填滿 [**COutputQueue：： m \_ ppSamples**](coutputqueue-m-ppsamples.md) 陣列，然後再傳遞一批樣本。 呼叫此方法以傳遞部分批次。 例如， [**COutputQueue：： EOS**](coutputqueue-eos.md) 方法會呼叫 `SendAnyway` 以序列化資料流程結束的訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




