---
description: CheckRequest 方法會檢查是否有線程要求，而不會封鎖。
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: 'CSourceStream. CheckRequest 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bb77358ec579415439c2832b00255e7ffeb3c7eba0e387bfa0522a4a5109669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073312"
---
# <a name="csourcestreamcheckrequest-method"></a>CSourceStream. CheckRequest 方法

`CheckRequest`方法會檢查是否有線程要求，而不會封鎖。

## <a name="syntax"></a>語法


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCom* 
</dt> <dd>

變數的指標，此變數會接收最後呼叫 [**CAMThread：： CallWorker**](camthread-callworker.md) 方法時所傳遞的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果有暫止的要求，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CAMThread：： CheckRequest**](camthread-checkrequest.md) 方法，以執行類型檢查。 **CSourceStream** 類別會定義 *pCom* 參數的下列列舉型別：


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




