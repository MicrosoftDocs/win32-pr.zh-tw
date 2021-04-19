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
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983117"
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

 

 




