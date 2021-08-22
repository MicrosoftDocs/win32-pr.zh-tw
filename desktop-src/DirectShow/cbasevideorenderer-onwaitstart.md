---
description: OnWaitStart 方法會更新花費在等候和不等候的時間。
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: 'CBaseVideoRenderer. OnWaitStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bc3b895f27490377fd5de188b7cea8ccd429c55d36a5cdd0fea4ce025bac29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502598"
---
# <a name="cbasevideorendereronwaitstart-method"></a>CBaseVideoRenderer. OnWaitStart 方法

`OnWaitStart`方法會更新花費在等候和不等待的時間。

## <a name="syntax"></a>語法


```C++
void OnWaitStart();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

開始等候轉譯事件時，會呼叫這個成員函式。 它僅用於效能度量。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




