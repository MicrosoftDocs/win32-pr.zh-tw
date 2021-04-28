---
description: CMsgThread。 CMsgThread 函式-函數方法。
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: 'CMsgThread. CMsgThread (Msgthrd. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095366"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>CMsgThread. CMsgThread 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CMsgThread();
```



## <a name="parameters"></a>參數

這個函式沒有參數。

## <a name="remarks"></a>備註

建立訊息執行緒物件並不會自動建立執行緒。 您必須呼叫 [**CMsgThread：： CreateThread**](cmsgthread-createthread.md) 成員函式來建立執行緒。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




