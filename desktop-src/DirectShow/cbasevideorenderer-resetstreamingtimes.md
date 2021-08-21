---
description: ResetStreamingTimes 方法會重設控制串流的所有時間。
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: 'CBaseVideoRenderer. ResetStreamingTimes 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bebf6f827cac883660b383b76f3a6ead7987e9fb468d0fd6f14205f59ad4d530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074772"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>CBaseVideoRenderer. ResetStreamingTimes 方法

`ResetStreamingTimes`方法會重設控制串流的所有時間。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

系統會設定時間，讓框架一開始不會被捨棄，因此會繪製第一個畫面格。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




