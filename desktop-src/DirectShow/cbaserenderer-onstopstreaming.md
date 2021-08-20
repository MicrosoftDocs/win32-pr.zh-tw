---
description: 當篩選停止串流時，會呼叫 OnStopStreaming 方法。
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: 'CBaseRenderer. OnStopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c61490a0719ce45d9776982b9230734d1126cef747330bb595c205500aca331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157661"
---
# <a name="cbaserendereronstopstreaming-method"></a>CBaseRenderer. OnStopStreaming 方法

`OnStopStreaming`當篩選停止串流時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBaseRenderer：： StopStreaming**](cbaserenderer-stopstreaming.md)方法會呼叫這個方法。 它不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




