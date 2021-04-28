---
description: CTransformInputPin. BreakConnect 方法-BreakConnect 方法會釋放連接的 pin。
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: 'CTransformInputPin. BreakConnect 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085016"
---
# <a name="ctransforminputpinbreakconnect-method"></a>CTransformInputPin. BreakConnect 方法

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

這個方法會覆寫 [**CBaseInputPin：： BreakConnect**](cbaseinputpin-breakconnect.md) 方法。 它會呼叫篩選器的 [**CTransformFilter：： BreakConnect**](ctransformfilter-breakconnect.md) 方法，它會 \_ 在基類中傳回 s OK。 衍生的類別可以覆寫 **CTransformFilter：： BreakConnect** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




