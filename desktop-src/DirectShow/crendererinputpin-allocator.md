---
description: 配置器方法會捕獲記憶體配置器的指標。
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: 'CRendererInputPin 配置器方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987151"
---
# <a name="crendererinputpinallocator-method"></a>CRendererInputPin 配置器方法

方法會捕獲記憶體配置器的 `Allocator` 指標。

## <a name="syntax"></a>語法


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標，或 **Null**。

## <a name="remarks"></a>備註

這個方法會傳回 [**CBaseInputPin：： m \_ pAllocator**](cbaseinputpin-m-pallocator.md) 成員變數。 方法不會遞增介面上的參考計數。 這個方法完全是存取子方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 




