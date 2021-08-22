---
description: ThreadExists 方法會查詢執行緒是否存在。
ms.assetid: 16be31c5-fae0-45d7-905d-4a2eef1ed819
title: 'CAMThread. ThreadExists 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadExists
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fe0681cf444b8b0e1072a38e54bbce99fef96ad7aa4810cd3456283f9850768
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641138"
---
# <a name="camthreadthreadexists-method"></a>CAMThread. ThreadExists 方法

`ThreadExists`方法會查詢執行緒是否存在。

## <a name="syntax"></a>語法


```C++
BOOL ThreadExists();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果執行緒存在，則傳回 **TRUE** ，如果執行緒不存在則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




