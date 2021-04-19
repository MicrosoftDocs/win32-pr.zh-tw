---
description: 參考 \_ 時間 () 運算子會將物件轉換為參考 \_ 時間資料類型。
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: CRefTime (Reftime) 的運算子 REFERENCE_TIME 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992952"
---
# <a name="creftimeoperator-reference_time-method"></a>CRefTime。 operator 參考 \_ 時間方法

運算子會將 `REFERENCE_TIME()` 物件轉換為 [**參考 \_ 時間**](reference-time.md) 資料類型。

## <a name="syntax"></a>語法


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CRefTime：： m \_ 時間**](creftime-m-time.md)的值。

## <a name="remarks"></a>備註

下列範例示範如何使用這個 cast 運算子：


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Reftime (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




