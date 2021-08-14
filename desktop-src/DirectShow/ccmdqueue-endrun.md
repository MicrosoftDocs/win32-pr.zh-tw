---
description: EndRun 方法會切換至已停止或已暫停模式。
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: 'CCmdQueue. EndRun 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757358"
---
# <a name="ccmdqueueendrun-method"></a>CCmdQueue. EndRun 方法

`EndRun`方法會切換至已停止或已暫停模式。

## <a name="syntax"></a>語法


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回相依于執行的 **HRESULT** 值。

## <a name="remarks"></a>備註

在呼叫這個成員函式之後，不知道串流時間與呈現時間之間的時間對應。 呼叫 [**CCmdQueue：： Run**](ccmdqueue-run.md) 成員函式來執行此對應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




