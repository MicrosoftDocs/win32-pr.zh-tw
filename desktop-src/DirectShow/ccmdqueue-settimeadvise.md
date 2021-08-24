---
description: SetTimeAdvise 方法會使用參考時鐘來設定計時器事件。
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: 'CCmdQueue. SetTimeAdvise 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757128"
---
# <a name="ccmdqueuesettimeadvise-method"></a>CCmdQueue. SetTimeAdvise 方法

`SetTimeAdvise`方法會使用參考時鐘來設定計時器事件。

## <a name="syntax"></a>語法


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此成員函式會呼叫 [**IReferenceClock：： AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) 方法，以針對佇列中所需的最早時間設定通知。 一律會檢查延遲的呈現時間命令。 如果篩選圖形處於執行模式，則也會檢查使用資料流程時間的延後命令。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




