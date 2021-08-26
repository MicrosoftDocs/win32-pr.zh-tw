---
description: 這個運算子會將參考時間乘以某個值。
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: 'COARefTime. operator * 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57060f3b0436422c34ba947c0025cc6796d534e16ff64be029e68ab140faa4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079348"
---
# <a name="coareftimeoperator-method"></a>COARefTime 運算子 \* 方法

這個運算子會將參考時間乘以某個值。

## <a name="syntax"></a>語法


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*l* 
</dt> <dd>

乘數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回新的 **COARefTime** 物件，這個物件等於這個物件和 **l** 的乘積。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




