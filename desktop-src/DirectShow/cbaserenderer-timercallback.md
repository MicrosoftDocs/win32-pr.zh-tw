---
description: TimerCallback 方法是結束資料流程計時器事件的回呼方法。
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: 'CBaseRenderer. TimerCallback 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d3164959ecaa701397b5550c43449884208df1110300b6a042879ac4f146584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537428"
---
# <a name="cbaserenderertimercallback-method"></a>CBaseRenderer. TimerCallback 方法

`TimerCallback`方法是結束資料流程計時器事件的回呼方法。

## <a name="syntax"></a>語法


```C++
void TimerCallback();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**CBaseRenderer：： SendEndOfStream**](cbaserenderer-sendendofstream.md)方法會使用計時器事件來排程 EC \_ 完成的通知。 **CBaseRenderer：： TimerCallback** 方法是計時器事件的回呼函數。 `TimerCallback`方法會再次呼叫 **SendEndOfStream** ，而 **SendEndOfStream** 會決定是要傳送 EC \_ 完成通知或設定另一個計時器。

[**CBaseRenderer：： ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)方法會取消計時器事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




