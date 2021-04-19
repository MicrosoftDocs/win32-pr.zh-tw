---
description: 當篩選完成等候樣本的呈現時間時，就會呼叫 OnWaitEnd 方法。
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: 'CBaseRenderer. OnWaitEnd 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996308"
---
# <a name="cbaserendereronwaitend-method"></a>CBaseRenderer. OnWaitEnd 方法

`OnWaitEnd`當篩選完成等候樣本的呈現時間時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**CBaseRenderer：： WaitForRenderTime**](cbaserenderer-waitforrendertime.md)方法會在完成等候樣本的呈現時間時呼叫這個方法。 這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。

如果您正在執行品質控制，您可能會覆寫此方法以及 [**CBaseRenderer：： OnWaitStart**](cbaserenderer-onwaitstart.md) 方法。 您可以使用這些方法來追蹤篩選器的效能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




