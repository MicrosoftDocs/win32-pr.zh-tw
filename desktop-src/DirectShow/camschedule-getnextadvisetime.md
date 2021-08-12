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
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662344"
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

 

 




