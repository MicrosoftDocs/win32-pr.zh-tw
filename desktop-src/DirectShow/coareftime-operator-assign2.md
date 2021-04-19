---
description: 運算子會指派新的參考時間，並使用 ' rt [ref] ' 參數。
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. operator = method (Ctlutil .h) -rt [ref] 參數
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
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106976533"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>COARefTime. operator = method (Ctlutil .h) -rt [ref] 參數

這個運算子會指派新的參考時間。

## <a name="syntax"></a>語法


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rt* \[裁判\]
</dt> <dd>

參考 [**\_ 時間**](reference-time.md) 值的參考，此值會以 100-毫微秒單位來指定新的參考時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求

| 需求                    | 值                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Ctlutil (包含： .h)                                                                                    |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COARefTime 類別**](coareftime.md)
</dt> </dl>

 

 




