---
description: AlignDown 方法會將值截斷為指定的對齊界限。
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: 'CPullPin. AlignDown 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdf16f3759bb7637fa243ce98bc4886b65e31d25bf62f5e9f581064d3741ea1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585348"
---
# <a name="cpullpinaligndown-method"></a>CPullPin. AlignDown 方法

方法會將 `AlignDown` 值截斷為指定的對齊界限。

## <a name="syntax"></a>語法


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*將* 
</dt> <dd>

指定要對齊的數位。

</dd> <dt>

*lAlign* 
</dt> <dd>

指定對齊界限。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回對齊的結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pullpin。h</dt> </dl>                                                                                                       |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPullPin 類別**](cpullpin.md)
</dt> </dl>

 

 




