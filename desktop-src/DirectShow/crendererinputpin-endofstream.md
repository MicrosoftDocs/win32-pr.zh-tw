---
description: EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會覆寫 CBasePin：： EndOfStream 方法。
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: 'CRendererInputPin. EndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991018"
---
# <a name="crendererinputpinendofstream-method"></a>CRendererInputPin. EndOfStream 方法

`EndOfStream`方法會通知 pin，不需要任何其他資料。 這個方法會覆寫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 




