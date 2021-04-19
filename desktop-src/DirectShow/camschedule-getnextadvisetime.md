---
description: GetNextAdviseTime 方法會捕獲下一個建議要求的時間。
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: 'CAMSchedule. GetNextAdviseTime 方法 (Dsschedule .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987190"
---
# <a name="camschedulegetnextadvisetime-method"></a>CAMSchedule. GetNextAdviseTime 方法

`GetNextAdviseTime`方法會捕獲下一個建議要求的時間。

## <a name="syntax"></a>語法


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下一個建議要求的參考時間，或 \_ 未排定任何要求的最大時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dsschedule (包含： .h) </dt> </dl>                                                                                |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMSchedule 類別**](camschedule.md)
</dt> </dl>

 

 




