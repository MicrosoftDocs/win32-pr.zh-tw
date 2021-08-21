---
description: 當狀態切換為 [已暫停] 或 [執行中] 時，會呼叫使用中的方法。
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: 'CBaseRenderer 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df5ec659b5e76940ebf279e3feb8995d34380db0543d9eebcf42c1f3bff8c0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954967"
---
# <a name="cbaserendereractive-method"></a>CBaseRenderer 方法

`Active`當狀態切換為已暫停或正在執行時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

輸入的 pin 會從自己的 [**CRendererInputPin：： Active**](crendererinputpin-active.md) 方法呼叫這個方法。 這個方法不會在基類中執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




