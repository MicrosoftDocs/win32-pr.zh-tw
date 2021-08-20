---
description: 當篩選開始進行串流處理時，會呼叫 OnStartStreaming 方法。
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: 'CBaseRenderer. OnStartStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b0f050222b0ca6a88c7cf1d9348597e4d7b68f2a2ed431b4f6843afe97efd5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157671"
---
# <a name="cbaserendereronstartstreaming-method"></a>CBaseRenderer. OnStartStreaming 方法

`OnStartStreaming`當篩選開始進行串流處理時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBaseRenderer：： StartStreaming**](cbaserenderer-startstreaming.md)方法會呼叫這個方法。 它不會在基類中執行任何動作，但衍生類別可以覆寫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




