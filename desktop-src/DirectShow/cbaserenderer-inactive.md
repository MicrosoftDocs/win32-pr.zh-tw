---
description: 當狀態切換為 [已停止] 時，會呼叫非使用中的方法。
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: 'CBaseRenderer：非使用中方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652398"
---
# <a name="cbaserendererinactive-method"></a>CBaseRenderer 方法

`Inactive`當狀態切換為 [已停止] 時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

輸入的 pin 會從它自己的 [**CRendererInputPin：：非**](crendererinputpin-inactive.md) 使用中的方法呼叫這個方法。 篩選準則會呼叫 [**CBaseRenderer：： ClearPendingSample**](cbaserenderer-clearpendingsample.md) 方法，以釋放最新的範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




