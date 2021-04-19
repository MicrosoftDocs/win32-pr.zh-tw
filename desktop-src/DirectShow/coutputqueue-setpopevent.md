---
description: SetPopEvent 方法會指定當物件從佇列中移除範例時發出信號的事件。
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: 'COutputQueue. SetPopEvent 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992790"
---
# <a name="coutputqueuesetpopevent-method"></a>COutputQueue. SetPopEvent 方法

`SetPopEvent`方法會指定當物件從佇列中移除範例時，會發出信號的事件。

## <a name="syntax"></a>語法


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hEvent* 
</dt> <dd>

呼叫端所建立之事件的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




