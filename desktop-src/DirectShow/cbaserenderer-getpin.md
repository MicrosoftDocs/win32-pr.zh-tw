---
description: GetPin 方法會抓取 pin。
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
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987018"
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

 

 




