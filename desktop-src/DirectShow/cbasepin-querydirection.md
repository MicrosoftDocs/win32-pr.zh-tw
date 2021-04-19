---
description: QueryDirection 方法會 (輸入或輸出) 來抓取 pin 的方向。 這個方法會實 IPin：： QueryDirection 方法。
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: 'CBasePin. QueryDirection 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999234"
---
# <a name="cbasepinquerydirection-method"></a>CBasePin. QueryDirection 方法

方法會抓取 `QueryDirection` pin (輸入或輸出) 的方向。 這個方法會實 [**IPin：： QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPinDir* 
</dt> <dd>

變數的指標，此變數會接收釘選 [**\_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction) 列舉類型的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




