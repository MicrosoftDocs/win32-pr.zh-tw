---
description: CBasePin 方法-使用中的方法會通知釘選篩選現在為使用中狀態。
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: 'CBasePin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096105"
---
# <a name="cbasepinactive-method"></a>CBasePin 方法

`Active`方法會通知釘選篩選現在已在使用中。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當篩選準則從 [已停止] 變成 [已暫停] 時， [**CBaseFilter**](cbasefilter.md) 類別會在所有篩選連接的釘選上呼叫這個方法。

這個方法不會在基類中執行任何動作。 衍生類別可以覆寫這個方法;例如，pin 可能會認可配置器或取得硬體資源。

除非這個成員函式傳回，否則篩選圖形管理員的內部狀態不會更新，因此請勿從此方法測試狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




