---
description: EndFlush 方法會結束清除作業。 這個方法會實 IPin：： EndFlush 方法。
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: 'CBaseOutputPin. EndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996034"
---
# <a name="cbaseoutputpinendflush-method"></a>CBaseOutputPin. EndFlush 方法

`EndFlush`方法會結束清除作業。 這個方法會實 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 E 非 \_ 預期的。

## <a name="remarks"></a>備註

這個方法應該只在輸入圖釘上呼叫，因此 **CBaseOutputPin** 的執行會傳回非 \_ 預期的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseOutputPin 類別**](cbaseoutputpin.md)
</dt> </dl>

 

 




