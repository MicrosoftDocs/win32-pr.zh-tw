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
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992373"
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

 

 




