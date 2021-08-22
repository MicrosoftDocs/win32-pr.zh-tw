---
description: ResetEndOfStreamTimer 方法會取消排定 EC \_ 完成通知的計時器。
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: 'CBaseRenderer. ResetEndOfStreamTimer 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e589288059eabbbbaaa23904ba021199cb051d9034345cb2c92ac946a6cba9c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502678"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>CBaseRenderer. ResetEndOfStreamTimer 方法

`ResetEndOfStreamTimer`方法會取消排定 [**EC \_ 完成**](ec-complete.md)通知的計時器。

## <a name="syntax"></a>語法


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer：： TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




