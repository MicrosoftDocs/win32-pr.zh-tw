---
description: 等候時間結束時，會呼叫 OnWaitEnd 方法。
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: 'CBaseVideoRenderer. OnWaitEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b130bf38833951cad4f82fd559c0299d2aea86854ca0ab5545f3f2794ab9b4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432468"
---
# <a name="cbasevideorendereronwaitend-method"></a>CBaseVideoRenderer. OnWaitEnd 方法

等候時間結束時，會呼叫 OnWaitEnd 方法。

## <a name="syntax"></a>語法


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式只會執行效能記錄。 從視窗中的等候喚醒執行緒，或在下一個範例是因為呈現時，就會呼叫它。 它最後可以用來收集控制同步處理的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




