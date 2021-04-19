---
description: ResetEndOfStream 方法會重設資料流程結尾旗標。
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: 'CBaseRenderer. ResetEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991356"
---
# <a name="cbaserendererresetendofstream-method"></a>CBaseRenderer. ResetEndOfStream 方法

`ResetEndOfStream`方法會重設資料流程結尾旗標。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

這個方法會清除先前的資料流程結束條件。 屆時，篩選器可以接收新的資料。 [**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法會呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




