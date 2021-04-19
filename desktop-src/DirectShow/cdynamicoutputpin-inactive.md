---
description: 非使用中的方法會通知釘選篩選已停止。
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: 'CDynamicOutputPin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992775"
---
# <a name="cdynamicoutputpininactive-method"></a>CDynamicOutputPin 方法

`Inactive`方法會通知釘選篩選已停止。

## <a name="syntax"></a>語法


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：：非**](cbaseoutputpin-inactive.md) 使用中的方法。 它會設定 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDynamicOutputPin 類別**](cdynamicoutputpin.md)
</dt> </dl>

 

 




