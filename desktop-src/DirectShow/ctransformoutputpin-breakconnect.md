---
description: CTransformOutputPin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: 'CTransformOutputPin. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084956"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>CTransformOutputPin. BreakConnect 方法

`BreakConnect`方法會從連接釋放 pin。

## <a name="syntax"></a>語法


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或其他 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseOutputPin：： BreakConnect**](cbaseoutputpin-breakconnect.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： BreakConnect**](ctransformfilter-breakconnect.md) 方法，它會 \_ 在基類中傳回 s OK。 衍生的類別可以覆寫 **CTransformFilter：： BreakConnect** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




