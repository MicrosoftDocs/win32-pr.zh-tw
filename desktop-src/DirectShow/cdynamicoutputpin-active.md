---
description: CDynamicOutputPin 方法-使用中的方法會通知釘選篩選現在為使用中狀態。
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: 'CDynamicOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12e59b434562e84c42228c16282620efe10866ea9dad85a4d62beb46f5a59e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688978"
---
# <a name="cdynamicoutputpinactive-method"></a>CDynamicOutputPin 方法

`Active`方法會通知釘選篩選現在已在使用中。

## <a name="syntax"></a>語法


```C++
HRESULT Active();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                            | Description                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                                                                                             |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 失敗。 未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：： Active**](cbaseoutputpin-active.md) 方法。 它會重設 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。 如果擁有篩選準則尚未呼叫 **SetConfigInfo**，這個方法會傳回 E \_ FAIL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




