---
description: Insert 方法會將 CDeferredCommand 物件新增至佇列。
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: 'CCmdQueue： Insert 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757318"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue. Insert 方法

`Insert`方法會將 [**CDeferredCommand**](cdeferredcommand.md)物件新增至佇列。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCmd* 
</dt> <dd>

要加入至佇列之 **CDeferredCommand** 物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_在預設的執行中傳回 S OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




