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
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979897"
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

 

 




