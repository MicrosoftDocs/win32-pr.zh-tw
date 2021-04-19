---
description: 函式方法。
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: 'CCritSec. CCritSec (Wxutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996522"
---
# <a name="ccritsecccritsec-constructor"></a>CCritSec. CCritSec 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CCritSec();
```



## <a name="parameters"></a>參數

這個函式沒有參數。

## <a name="remarks"></a>備註

這個方法會呼叫 [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) 函數，以初始化重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

