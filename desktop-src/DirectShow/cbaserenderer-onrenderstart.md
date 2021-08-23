---
description: 當轉譯即將開始時，會呼叫 OnRenderStart 方法。
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: 'CBaseRenderer. OnRenderStart 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626dc1dbcb82aeec94ebe514e686d197cb17bbdd7807ac38057412617182bf55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157651"
---
# <a name="cbaserendereronrenderstart-method"></a>CBaseRenderer. OnRenderStart 方法

當轉譯即將 `OnRenderStart` 開始時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**CBaseRenderer：： Render**](cbaserenderer-render.md)方法會呼叫這個方法。 它不會在基類中執行任何動作，但衍生類別可以覆寫它。例如，收集品質控制資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




