---
description: OnStopStreaming 方法會在串流結束時呼叫，以修正屬性頁報表的時間。
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: 'CBaseVideoRenderer. OnStopStreaming 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990110"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>CBaseVideoRenderer. OnStopStreaming 方法

在 `OnStopStreaming` 串流結束時呼叫方法，以修正屬性頁報表的時間。

## <a name="syntax"></a>語法


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

這個成員函式會被呼叫兩次，一次在暫停時，當資料流程實際上停止時。

此成員函式會覆寫 [**CBaseRenderer：： OnStopStreaming**](cbaserenderer-onstopstreaming.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




