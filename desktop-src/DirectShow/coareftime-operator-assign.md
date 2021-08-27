---
description: 這個運算子會指派新的參考時間。
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: 'COARefTime： operator = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31784a008a2074156c69abf868739ec27c459dabdba1437397780086d28f9847
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084458"
---
# <a name="coareftimeoperator-method-ctlutilh"></a>COARefTime： operator = 方法 (Ctlutil .h) 

這個運算子會指派新的參考時間。

## <a name="syntax"></a>語法


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rd* \[裁判\]
</dt> <dd>

參考 **雙精度浮點數** ，指定新的參考時間（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




