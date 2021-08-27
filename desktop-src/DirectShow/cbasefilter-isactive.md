---
description: IsActive 方法會判斷篩選目前是否正在使用中， (執行中或已暫停) 。
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: 'CBaseFilter. IsActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbbd9fedf94816d518ef9f8826542399d1d1e97f97137b2d86581d36c4a33e53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076638"
---
# <a name="cbasefilterisactive-method"></a>CBaseFilter. IsActive 方法

`IsActive`方法會判斷篩選目前是否為作用中， (執行中或已暫停) 。

## <a name="syntax"></a>語法


```C++
BOOL IsActive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果篩選已暫停或正在執行，則傳回 **TRUE** ; 如果已停止，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




