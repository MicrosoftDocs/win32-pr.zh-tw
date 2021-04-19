---
description: = 運算子會指派新的參考時間。 這個方法使用 *ll* 參數。
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. operator = method (Reftime. h) -ll 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106993704"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a>CRefTime. operator = method (Reftime. h) -ll 參數

= 運算子會指派新的參考時間。

## <a name="syntax"></a>語法


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*將* 
</dt> <dd>

新的參考時間，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | Reftime (包含： .h)                                                                                    |
| 程式庫 |  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |



 

 




