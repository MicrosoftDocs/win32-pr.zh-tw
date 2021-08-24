---
description: EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會實 IPin：： EndOfStream 方法。 請只對輸入圖釘呼叫這個方法。
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: 'CBasePin. EndOfStream 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9e1549000be728da0118323303a60a23a5930ad68d3c7d2d2b6c9c92d54c3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916428"
---
# <a name="cbasepinendofstream-method"></a>CBasePin. EndOfStream 方法

`EndOfStream`方法會通知 pin，不需要任何其他資料。 這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。 請只對輸入圖釘呼叫這個方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

篩選準則應該將下游的結束資料流程通知傳遞至連線篩選的輸入接點。 如果篩選器是轉譯器，則應該將 [**EC \_ 完成**](ec-complete.md) 事件通知張貼至篩選圖形管理員。 如需詳細資訊，請參閱[篩選 Graph 中的資料 Flow](data-flow-in-the-filter-graph.md)。

在基類中，此方法不會執行任何動作。 衍生類別應該覆寫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 




