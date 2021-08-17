---
description: CBaseRenderer. GetPin 方法-GetPin 方法會抓取 pin。
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: 'CBaseRenderer. GetPin 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822699"
---
# <a name="cbaserenderergetpin-method"></a>CBaseRenderer. GetPin 方法

方法會抓取 `GetPin` pin。

## <a name="syntax"></a>語法


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*n* 
</dt> <dd>

指定之 pin 的編號。 必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CBaseRenderer：： m \_ pInputPin**](cbaserenderer-m-pinputpin.md) 指標。

## <a name="remarks"></a>備註

這個方法會實 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法，這是 **CBaseFilter** 類別中的純虛擬。 篩選僅支援輸入 pin)  (一個 pin。 第一次呼叫這個方法時，它會將 pin 建立為新的 [**CRendererInputPin**](crendererinputpin.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




