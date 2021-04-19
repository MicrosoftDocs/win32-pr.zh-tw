---
description: 這個運算子會將參考時間除以某個值。
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: 'COARefTime. operator/方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999415"
---
# <a name="coareftimeoperator-method"></a>COARefTime. operator/方法

這個運算子會將參考時間除以某個值。

## <a name="syntax"></a>語法


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*l* 
</dt> <dd>

因數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新的 **COARefTime** 物件，等於這個物件和 **l** 的商。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




