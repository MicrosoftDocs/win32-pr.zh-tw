---
description: 當篩選準則在暫停時收到範例時，會呼叫 OnReceiveFirstSample 方法。
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: 'CBaseRenderer. OnReceiveFirstSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 882a356f47aa146ec8ba1b06d7af43235c8213334c0d82d0a241c590654bf2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157698"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>CBaseRenderer. OnReceiveFirstSample 方法

`OnReceiveFirstSample`當篩選準則在暫停時收到範例時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual void OnReceiveFirstSample(
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

[**CBaseRenderer：： Receive 方法會**](cbaserenderer-receive.md)呼叫這個方法。 它不會在基類中執行任何動作，但衍生類別可以覆寫它。 此方法主要用於影片轉譯器。 當影片轉譯器暫停時，通常會將第一個範例顯示為靜止影像。

在暫停時搜尋圖形也會導致呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




