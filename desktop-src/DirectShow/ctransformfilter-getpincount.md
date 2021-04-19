---
description: GetPinCount 方法會抓取篩選上的釘選數目。
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: 'CTransformFilter. GetPinCount 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990747"
---
# <a name="ctransformfiltergetpincount-method"></a>CTransformFilter. GetPinCount 方法

方法會抓取 `GetPinCount` 篩選上的釘選數目。

## <a name="syntax"></a>語法


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回2。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：： GetPinCount**](cbasefilter-getpincount.md) 方法。 **CTransformFilter** 類別只支援一個輸入 pin 和一個輸出圖釘。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




