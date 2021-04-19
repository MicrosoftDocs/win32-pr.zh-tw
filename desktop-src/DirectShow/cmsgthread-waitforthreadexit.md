---
description: 封鎖直到執行緒結束為止。
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: 'CMsgThread. WaitForThreadExit 方法 (Msgthrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990291"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>CMsgThread. WaitForThreadExit 方法

封鎖直到執行緒結束為止。

## <a name="syntax"></a>語法


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

執行緒所傳回之結束代碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 或 **FALSE**，其意義取決於提供覆寫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式和呼叫成員函式的類別。

## <a name="remarks"></a>備註

在完成衍生類別的終結之前，請確定背景工作執行緒已完全結束：否則，在您的動態連結程式庫 (DLL) 從進程的位址空間卸載之後，執行緒仍可能會執行。 即使要結束的唯一指令是單一傳回指令，但這會造成例外狀況。 確保執行緒已結束的唯一可靠方法，是使用傳送至 [**CMsgThread：:P utthreadmsg**](cmsgthread-putthreadmsg.md)) 成員函式的私下協商 [**CMsg**](cmsg.md)物件，來指示執行緒結束 (，然後再呼叫這個成員函式。 您應該在衍生類別的函式中進行這項作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Msgthrd (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMsgThread 類別**](cmsgthread.md)
</dt> </dl>

 

 




