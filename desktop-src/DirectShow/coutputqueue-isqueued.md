---
description: IsQueued 方法會判斷物件是否使用背景工作執行緒來傳遞範例。
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: 'COutputQueue. IsQueued 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e261127e16cd1190fb711d81a9f5fd5606738b7f9a3f8697902170662b99f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813578"
---
# <a name="coutputqueueisqueued-method"></a>COutputQueue. IsQueued 方法

`IsQueued`方法會判斷物件是否使用背景工作執行緒來傳遞範例。

## <a name="syntax"></a>語法


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果物件正在使用背景工作執行緒，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 




