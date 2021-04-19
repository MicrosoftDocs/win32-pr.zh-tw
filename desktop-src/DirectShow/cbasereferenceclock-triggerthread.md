---
description: TriggerThread 方法會喚醒處理排程的背景工作執行緒。
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: 'CBaseReferenceClock. TriggerThread 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979553"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>CBaseReferenceClock. TriggerThread 方法

`TriggerThread`方法會喚醒處理排程的背景工作執行緒。

## <a name="syntax"></a>語法


```C++
void TriggerThread();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

時鐘會使用在適當時間呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法的背景工作執行緒。 衍生的類別可以呼叫 `TriggerThread` 喚醒執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Refclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseReferenceClock 類別**](cbasereferenceclock.md)
</dt> </dl>

 

 




