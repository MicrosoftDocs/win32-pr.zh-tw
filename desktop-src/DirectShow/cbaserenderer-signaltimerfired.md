---
description: SignalTimerFired 方法會清除用來排程轉譯的計時器識別碼。
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: 'CBaseRenderer. SignalTimerFired 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998642"
---
# <a name="cbaserenderersignaltimerfired-method"></a>CBaseRenderer. SignalTimerFired 方法

`SignalTimerFired`方法會清除用來排程轉譯的計時器識別碼。

## <a name="syntax"></a>語法


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當轉譯計時器啟動時，篩選會呼叫這個方法 (請參閱 [**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) 或當計時器取消時 (參閱 [**CBaseRenderer：： CancelNotification**](cbaserenderer-cancelnotification.md)) 。 方法會將 [**CBaseRenderer：： m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) 成員變數重設為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




