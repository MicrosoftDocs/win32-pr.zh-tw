---
description: 當篩選開始等候樣本的呈現時間時，會呼叫 OnWaitStart 方法。
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: 'CBaseRenderer. OnWaitStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822645"
---
# <a name="cbaserendereronwaitstart-method"></a>CBaseRenderer. OnWaitStart 方法

`OnWaitStart`當篩選準則開始等候樣本的呈現時間時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)方法會在開始等候樣本的呈現時間時呼叫這個方法。 這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

如果您正在執行品質控制，您可能會覆寫此方法以及 [**CBaseRenderer：： OnWaitEnd**](cbaserenderer-onwaitend.md) 方法。 您可以使用這些方法來追蹤篩選器的效能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




