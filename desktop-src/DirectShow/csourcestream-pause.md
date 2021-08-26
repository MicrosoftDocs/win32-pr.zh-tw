---
description: Pause 方法會通知串流執行緒成為使用中狀態。
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: 'CSourceStream： Pause 方法 (Source. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079308"
---
# <a name="csourcestreampause-method"></a>CSourceStream. Pause 方法

`Pause`方法會通知串流執行緒成為使用中。

## <a name="syntax"></a>語法


```C++
HRESULT Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 \_ [OK] 或 [E 未 \_ 預期]。

## <a name="remarks"></a>備註

[**CSourceStream：： Active**](csourcestream-active.md)方法會呼叫這個方法。 當 [**CSourceStream：： ThreadProc**](csourcestream-threadproc.md) 方法收到此要求時，它會呼叫 [**CSourceStream：:D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 




