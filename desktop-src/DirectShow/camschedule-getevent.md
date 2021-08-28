---
description: GetEvent 方法會抓取事件控制碼，此控制碼可用來在下一個建議時間中通知變更。
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: 'CAMSchedule. GetEvent 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e5126fde495c9553975daaf2db9e82de4ab4530a4629d217eba51818e20d1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689078"
---
# <a name="camschedulegetevent-method"></a>CAMSchedule. GetEvent 方法

此 `GetEvent` 方法會抓取事件控制碼，此控制碼可用來在下一個建議時間發出變更。

## <a name="syntax"></a>語法


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回事件的控制碼。

## <a name="remarks"></a>備註

如果下一個建議時間變更為其他字組，則如果新的建議要求新增至清單前端，則排程器會發出信號給此事件。 時鐘應該呼叫 [**CAMSchedule：： Advise**](camschedule-advise.md) 方法以判斷下一個建議時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMSchedule 類別**](camschedule.md)
</dt> </dl>

 

 




