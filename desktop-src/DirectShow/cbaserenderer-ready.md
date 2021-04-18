---
description: Ready 方法表示狀態轉換已完成。
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: 'CBaseRenderer： Ready 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976264"
---
# <a name="cbaserendererready-method"></a>CBaseRenderer Ready 方法

`Ready`方法會指示狀態轉換已完成。

## <a name="syntax"></a>語法


```C++
void Ready();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會使 [**CBaseRenderer：： >getstate**](cbaserenderer-getstate.md) 方法傳回 S \_ OK，表示篩選已完成轉換為目前的狀態。 篩選準則會在每次完成狀態轉換時呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::CheckReady**](cbaserenderer-checkready.md)
</dt> <dt>

[**CBaseRenderer：： NotReady**](cbaserenderer-notready.md)
</dt> </dl>

 

 




