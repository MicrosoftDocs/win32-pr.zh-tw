---
description: GetMediaTypeVersion 方法會抓取慣用媒體類型集的版本號碼。
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: 'CBasePin. GetMediaTypeVersion 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999539"
---
# <a name="cbasepingetmediatypeversion-method"></a>CBasePin. GetMediaTypeVersion 方法

方法會抓取一 `GetMediaTypeVersion` 組慣用媒體類型的版本號碼。

## <a name="syntax"></a>語法


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBasePin：： m \_ TypeVersion**](cbasepin-m-typeversion.md) 成員變數。

## <a name="remarks"></a>備註

**CBasePin** 函式會將版本號碼初始化為1。 在基類中，此數位永遠不會變更。 如果 pin 會動態變更其慣用媒體類型的清單，則每當清單變更時，就應該遞增版本號碼。 若要遞增版本號碼，請呼叫 [**CBasePin：： IncrementTypeVersion**](cbasepin-incrementtypeversion.md) 方法。

由 [**CEnumMediaTypes**](cenummediatypes.md) 類別所執行的媒體類型列舉值會使用版本號碼，使其本身與釘選同步。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




