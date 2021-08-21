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
ms.openlocfilehash: 180cce9bc0d52c6e11bbd90b64cfe7d57d4dcc99eada3a794f924df6857c4698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076178"
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

 

 




