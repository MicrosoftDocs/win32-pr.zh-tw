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
ms.openlocfilehash: a8b53af246e029b5142b68840cfde0e776208e3c51093438042dd74f42a1b3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076438"
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

 

 




