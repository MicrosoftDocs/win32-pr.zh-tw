---
description: ResetMediaTime 方法會將快取的時間戳記重設為零。
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: 'CRendererPosPassThru. ResetMediaTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999201"
---
# <a name="crendererpospassthruresetmediatime-method"></a>CRendererPosPassThru. ResetMediaTime 方法

方法會將快取 `ResetMediaTime` 的時間戳記重設為零。

## <a name="syntax"></a>語法


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

每當 [**CRendererPosPassThru：： RegisterMediaTime**](crendererpospassthru-registermediatime.md) 方法所快取的時間戳記變成無效時，篩選準則就會呼叫這個方法。 具體而言，它應該呼叫這個方法來回應 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 和 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。

呼叫這個方法之後， [**CRendererPosPassThru：： GetMediaTime**](crendererpospassthru-getmediatime.md) 方法會針對開始和結束時間傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




