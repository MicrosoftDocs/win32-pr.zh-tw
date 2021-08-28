---
description: CBasePin 方法-非使用中方法會通知 pin，篩選已不再有效。
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: 'CBasePin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052738"
---
# <a name="cbasepininactive-method"></a>CBasePin 方法

`Inactive`方法會通知 pin，篩選已不再有效。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當篩選準則停止時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選連接的釘選上呼叫這個方法。

這個方法不會在基類中執行任何動作。 衍生類別應該覆寫這個方法，以釋放 [**CBasePin：： Active**](cbasepin-active.md) 方法所取得的任何資源;例如，取消認可釘選的配置器。

在這個方法傳回之前，不會更新篩選圖形管理員的內部狀態，因此請勿從此方法測試狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




