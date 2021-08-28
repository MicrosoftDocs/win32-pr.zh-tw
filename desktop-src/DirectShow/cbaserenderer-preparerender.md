---
description: 在篩選器呈現範例之前，會呼叫 PrepareRender 方法。
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: 'CBaseRenderer. PrepareRender 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3443d3344d24d6f121e2c236b9742a44a97e06414ab264953c29ad004e38d7dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872198"
---
# <a name="cbaserendererpreparerender-method"></a>CBaseRenderer. PrepareRender 方法

在 `PrepareRender` 篩選器呈現範例之前，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

篩選準則會在呼叫 [**CBaseRenderer：： OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) 方法或 [**CBaseRenderer：： Render**](cbaserenderer-render.md) 方法之前呼叫這個方法。 `PrepareRender` 不會在基類中執行任何動作。 衍生類別可以覆寫它，以執行轉譯之前所需的任何動作。 例如，影片轉譯器可以覆寫這個方法，以實現其調色板。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




