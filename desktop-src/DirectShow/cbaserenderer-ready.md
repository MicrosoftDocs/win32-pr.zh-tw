---
description: Ready 方法表示狀態轉換已完成。
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: 'CBaseRenderer： Ready 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a1870af825f2a33236d0fd86d0f730e0013df59297fec5cdaa2baf46a2b773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757518"
---
# <a name="cbaserendererready-method"></a>CBaseRenderer Ready 方法

`Ready`方法會指示狀態轉換已完成。

## <a name="syntax"></a>語法


```C++
void Ready();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法傳回 S \_ OK，表示篩選已完成轉換為目前的狀態。 篩選準則會在每次完成狀態轉換時呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer：： NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 




