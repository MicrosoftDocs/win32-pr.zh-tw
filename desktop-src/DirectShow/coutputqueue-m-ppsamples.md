---
description: 大小為 COutputQueue：： m lBatchSize 的範例陣列 \_ 。
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'COutputQueue：： m_ppSamples 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994760"
---
# <a name="coutputqueuem_ppsamples-member"></a>COutputQueue：： m \_ ppSamples 成員

大小為 [**COutputQueue：： m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)的範例陣列。

## <a name="syntax"></a>語法


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>備註

背景工作執行緒會從佇列提取範例，並將它們放在此陣列中。 它會將陣列傳遞給 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。 如果物件不是使用背景工作執行緒，則物件會將範例直接放入這個陣列中。 [**COutputQueue：： m \_ List**](coutputqueue-m-list.md)成員變數會保存佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




