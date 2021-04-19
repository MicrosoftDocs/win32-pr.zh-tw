---
description: ConnectedIMemInputPin 方法會抓取下游輸入圖釘的指標。 這個方法會傳回 CBaseOutputPin：： m \_ pInputPin 成員變數。
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: 'CTransInPlaceOutputPin. ConnectedIMemInputPin 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977466"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>CTransInPlaceOutputPin. ConnectedIMemInputPin 方法

方法會抓取 `ConnectedIMemInputPin` 下游輸入圖釘的指標。 這個方法會傳回 [**CBaseOutputPin：： m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) 成員變數。

## <a name="syntax"></a>語法


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下游輸入釘選上 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceOutputPin 類別**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




