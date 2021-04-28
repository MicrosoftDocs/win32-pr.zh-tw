---
description: CTransInPlaceOutputPin. PeekAllocator 方法-PeekAllocator 方法會傳回釘選配置器的指標。 方法不會遞增介面上的參考計數。
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: 'CTransInPlaceOutputPin. PeekAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084596"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>CTransInPlaceOutputPin. PeekAllocator 方法

方法會傳回釘選配置器的 `PeekAllocator` 指標。 方法不會遞增介面上的參考計數。

## <a name="syntax"></a>語法


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBaseOutputPin：： m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) 成員變數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




