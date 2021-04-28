---
description: CTransformInputPin. CurrentMediaType 方法-CurrentMediaType 方法會抓取目前 pin 連接的媒體類型。
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
ms.openlocfilehash: 011f4eeda7f4a278baeceeadc7c21a822ae02b74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084986"
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



 

 




