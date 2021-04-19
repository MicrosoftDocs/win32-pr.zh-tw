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
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999346"
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

 

 




