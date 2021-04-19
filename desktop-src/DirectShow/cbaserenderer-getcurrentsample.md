---
description: GetCurrentSample 方法會抓取目前的範例。
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: 'CBaseRenderer. GetCurrentSample 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48c42ff02b22d30138fcad7d1e8af5e57a391b99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987175"
---
# <a name="cbaserenderergetcurrentsample-method"></a>CBaseRenderer. GetCurrentSample 方法

方法會抓取 `GetCurrentSample` 目前的範例。

## <a name="syntax"></a>語法


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標，如果沒有可用的範例，則傳回 **Null** 。

## <a name="remarks"></a>備註

除非方法傳回 **Null**，否則方法會先在 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample)指標上呼叫 **AddRef** ，然後再將它傳回。 呼叫端必須釋放指標。 藉由隱含方式 (，您必須將傳回值指派給變數，以便您可以在稍後釋放它。 ) 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




