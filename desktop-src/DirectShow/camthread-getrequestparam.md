---
description: GetRequestParam 方法會抓取最新的要求。
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: 'CAMThread. GetRequestParam 方法 (Wxutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c511fdb68bb6ee9372530d9e19290342a57fbcc5817148613d20fd8afe029b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384918"
---
# <a name="camthreadgetrequestparam-method"></a>CAMThread. GetRequestParam 方法

方法會抓取 `GetRequestParam` 最新的要求。

## <a name="syntax"></a>語法


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回最近傳遞給 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法的參數值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




