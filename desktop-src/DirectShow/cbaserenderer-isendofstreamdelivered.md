---
description: IsEndOfStreamDelivered 方法會查詢是否已將 EC \_ 完成事件傳遞至篩選圖形管理員。
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: 'CBaseRenderer. IsEndOfStreamDelivered 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989687"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>CBaseRenderer. IsEndOfStreamDelivered 方法

`IsEndOfStreamDelivered`方法會查詢是否已將 EC \_ 完成事件傳遞至篩選圖形管理員。

## <a name="syntax"></a>語法


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseRenderer：： m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




