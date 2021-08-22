---
description: NotReady 方法會通知狀態轉換尚未完成。
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: 'CBaseRenderer. NotReady 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52fddcbd92544a109340697e5865f87e6c5f74a14b01543e768495b7717d8f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954827"
---
# <a name="cbaserenderernotready-method"></a>CBaseRenderer. NotReady 方法

`NotReady`方法會指示狀態轉換尚未完成。

## <a name="syntax"></a>語法


```C++
void NotReady();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法傳回 VFW \_ S \_ 狀態 \_ 中繼，表示篩選仍在轉換成目前的狀態。 每當狀態轉換暫止時，篩選準則就會呼叫這個方法。  (當篩選準則暫停時，就會發生這種情況，直到收到範例為止 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> <dt>

[**CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**就緒**](cbaserenderer-ready.md)
</dt> </dl>

 

 




