---
description: CurrentMediaType 方法會抓取目前 pin 連接的媒體類型。
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: 'CTransformInputPin. CurrentMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59feca88e896b2a81a352b693e57ceaa5388d452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992581"
---
# <a name="ctransforminputpincurrentmediatype-method"></a>CTransformInputPin. CurrentMediaType 方法

方法會抓取 `CurrentMediaType` 目前連接的媒體類型。

## <a name="syntax"></a>語法


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**CBasePin：： m \_ mt**](cbasepin-m-mt.md) 成員變數的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




