---
description: CCritSec. ~ CCritSec 的函式-函式方法。
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: 'CCritSec. ~ CCritSec (Wxutil 的函式) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095806"
---
# <a name="ccritsecccritsec-destructor"></a>CCritSec. ~ CCritSec 的函式

函式方法。

## <a name="syntax"></a>語法


```C++
~CCritSec();
```



## <a name="remarks"></a>備註

這個方法會呼叫 [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) 函數來刪除重要區段。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCritSec 類別**](ccritsec.md)
</dt> </dl>

 

