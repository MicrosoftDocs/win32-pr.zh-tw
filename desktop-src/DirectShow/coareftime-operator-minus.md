---
description: 這個運算子會從另一個參考時間減去另一個參考時間。
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime) 方法 (Ctlutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da8de864f344321cc5dca801782aab1f8476eb91608b42577cca6a34c625e153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073822"
---
# <a name="coareftimeoperator--method"></a>COARefTime 運算子-方法

這個運算子會從另一個參考時間減去另一個參考時間。

## <a name="syntax"></a>語法


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

要減去之 **COARefTime** 物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回等於參考時間差異的新 **COARefTime** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




