---
description: CBaseFilter. GetPinCount 方法-GetPinCount 方法會抓取釘選數目。
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: 'CBaseFilter. GetPinCount 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7d136b5b3bbdcd8a6b21fcbd9f854de7a78a91be87a199c990e294ce8b28fb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640478"
---
# <a name="cbasefiltergetpincount-method"></a>CBaseFilter. GetPinCount 方法

方法會抓取 `GetPinCount` 釘選數目。

## <a name="syntax"></a>語法


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回釘選數目。

## <a name="remarks"></a>備註

衍生的類別必須執行此純虛擬方法。 傳回此篩選器目前可用的 pin 數目。 篩選可以動態建立或終結圖釘。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




