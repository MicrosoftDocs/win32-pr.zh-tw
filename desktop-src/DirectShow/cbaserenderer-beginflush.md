---
description: CBaseRenderer. BeginFlush 方法-BeginFlush 方法開始進行清除作業。
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: 'CBaseRenderer. BeginFlush 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70823dcc9b965aa45a7012a4c9a0210bbf77ac942d59e1ad09e028eae24a40a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158076"
---
# <a name="cbaserendererbeginflush-method"></a>CBaseRenderer. BeginFlush 方法

`BeginFlush`方法會開始清除作業。

## <a name="syntax"></a>語法


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

當篩選準則的輸入 pin 收到 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法的呼叫時，會呼叫這個方法。 此篩選會釋放串流執行緒，並釋放其保留的任何範例以供轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




