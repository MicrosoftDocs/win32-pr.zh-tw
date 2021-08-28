---
description: SetSyncSource 方法會設定計時所使用的時鐘。
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: 'CCmdQueue. SetSyncSource 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3877fb52a1e2268d24974ee3575c712d27a107f4429398ada9de1ebf5e728675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757148"
---
# <a name="ccmdqueuesetsyncsource-method"></a>CCmdQueue. SetSyncSource 方法

`SetSyncSource`方法會設定計時所使用的時鐘。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIrc* 
</dt> <dd>

[**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CCmdQueue 類別**](ccmdqueue.md)
</dt> </dl>

 

 




