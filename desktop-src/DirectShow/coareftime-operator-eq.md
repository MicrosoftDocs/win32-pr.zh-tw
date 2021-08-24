---
description: 這個運算子會測試兩個參考時間是否相等。
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: 'COARefTime： operator = = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36951e2a2d0f82d73106f5b78ef9eb7e0b067c34dc4db3fd72521f48d8d4beb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831818"
---
# <a name="coareftimeoperator-method"></a>COARefTime. operator = = 方法

這個運算子會測試兩個參考時間是否相等。

## <a name="syntax"></a>語法


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

要比較的 **COARefTime** 物件參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果兩個物件相等，則傳回 **TRUE** 。 否則，會傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




