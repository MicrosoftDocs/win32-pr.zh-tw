---
description: CTransformOutputPin. CurrentMediaType 方法-CurrentMediaType 方法會抓取目前 pin 連接的媒體類型。
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: 'CTransformOutputPin. CurrentMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094906"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a>CTransformOutputPin. CurrentMediaType 方法

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



 

 




