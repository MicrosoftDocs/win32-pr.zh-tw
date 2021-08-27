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
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103158"
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

 

 




