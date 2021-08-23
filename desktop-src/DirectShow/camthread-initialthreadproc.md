---
description: InitialThreadProc 方法會呼叫主要執行緒程式。
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: " (Wxutil 的 CAMThread.InitialThreadProc 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540298"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.InitialThreadProc 方法

`InitialThreadProc`方法會呼叫主要執行緒程式。

## <a name="syntax"></a>語法


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*光伏* 
</dt> <dd>

`this` 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CAMThread：： ThreadProc**](camthread-threadproc.md)所傳回的 **DWORD** 。 衍生的類別會定義此值。

## <a name="remarks"></a>備註

[**CAMThread：： Create**](camthread-create.md)方法會在建立執行緒時，針對執行緒程式使用這個方法。 它使用 `this` 指標做為執行緒引數。

這個方法會呼叫 [**CAMThread：： CoInitializeHelper**](camthread-coinitializehelper.md) 方法，然後再 ThreadProc。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CAMThread 類別**](camthread.md)
</dt> </dl>

 

 




