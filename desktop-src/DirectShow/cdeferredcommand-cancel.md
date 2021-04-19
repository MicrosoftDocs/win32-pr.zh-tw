---
description: Cancel 方法會取消先前已排入佇列的 CDeferredCommand：： Invoke 要求。
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: 'CDeferredCommand. Cancel 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984875"
---
# <a name="cdeferredcommandcancel-method"></a>CDeferredCommand. Cancel 方法

`Cancel`方法會取消先前已排入佇列的 [**CDeferredCommand：： Invoke**](cdeferredcommand-invoke.md)要求。

## <a name="syntax"></a>語法


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_ \_ \_ 如果 **m \_ pQueue** 為 **Null**，則傳回 VFW E 已取消。 如果呼叫產生錯誤，則從 [**CCmdQueue：： Remove**](ccmdqueue-remove.md)傳回 **HRESULT** 。 \_如果成功，則傳回 S OK。

## <a name="remarks"></a>備註

此成員函式會實 [**IDeferredCommand：： Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 




