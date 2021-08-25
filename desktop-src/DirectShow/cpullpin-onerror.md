---
description: 如果在資料流程處理期間發生錯誤，則會呼叫 OnError 方法。 衍生的類別必須執行此方法。
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: 'CPullPin： OnError 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0d9873e2d327c424b2cd1ffda7112676f53399a63d2a9ca92dca1f50a02f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908878"
---
# <a name="cpullpinonerror-method"></a>CPullPin 的 OnError 方法

`OnError`如果在串流處理期間發生錯誤，則會呼叫方法。 衍生的類別必須執行此方法。

## <a name="syntax"></a>語法


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*小時* 
</dt> <dd>

指定失敗的方法所傳回的 **HRESULT** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每當發生會中止資料提取執行緒的錯誤時，物件就會呼叫這個方法。 篩選可以使用這個方法，以正常方式從資料流程錯誤中復原。 在大多數情況下，錯誤是從上游篩選傳回，因此上游篩選器會負責將它報告給篩選 Graph 管理員。 如果錯誤發生在 [**CPullPin：： Receive**](cpullpin-receive.md) 方法內，您的篩選器應該會傳送 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件。  (參閱 [**IMediaEventSink：： Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




