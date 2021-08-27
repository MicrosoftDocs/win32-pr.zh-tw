---
description: DoRenderSample 方法會呈現範例。
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: 'CBaseRenderer. DoRenderSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef91e7ad27d008f5dfdb83e5642ecba8ec68bc424824dca9c8aa068ec055f24f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076428"
---
# <a name="cbaserendererdorendersample-method"></a>CBaseRenderer. DoRenderSample 方法

`DoRenderSample`方法會呈現範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

衍生的類別必須執行此方法。 行為完全取決於所要執行之篩選的類型。 例如，影片轉譯器會繪製範例中所包含的影片影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




