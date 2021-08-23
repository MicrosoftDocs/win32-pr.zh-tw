---
description: Remove 方法會從佇列中移除 CDeferredCommand 物件。
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: 'CCmdQueue： Remove 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954577"
---
# <a name="ccmdqueueremove-method"></a>CCmdQueue 方法

`Remove`方法會從佇列中移除 [**CDeferredCommand**](cdeferredcommand.md)物件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCmd* 
</dt> <dd>

要從佇列中移除之 **CDeferredCommand** 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果在 \_ \_ \_ 佇列中找不到物件，則會傳回 VFW E （找不到）。 否則，會傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




