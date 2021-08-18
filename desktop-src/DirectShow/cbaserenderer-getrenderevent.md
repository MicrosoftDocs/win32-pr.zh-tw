---
description: GetRenderEvent 方法會捕獲排程轉譯的事件。
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: 'CBaseRenderer. GetRenderEvent 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b4adc030e172a3d66d501e745ca9e3d1062fc1551bccb504fff36328d00bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822655"
---
# <a name="cbaserenderergetrenderevent-method"></a>CBaseRenderer. GetRenderEvent 方法

`GetRenderEvent`方法會捕獲排程轉譯的事件。

## <a name="syntax"></a>語法


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseRenderer：： m \_ RenderEvent**](cbaserenderer-m-renderevent.md) 事件的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




