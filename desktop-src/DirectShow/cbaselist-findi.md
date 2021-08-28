---
description: FindI 方法會抓取保留指定專案的第一個位置。
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: 'CBaseList. FindI 方法 (Wxlist .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8bdd89de7e28c5645cf8a418a8472d484f891a499f11e238b80af5f7062ff4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635448"
---
# <a name="cbaselistfindi-method"></a>CBaseList. FindI 方法

`FindI`方法會抓取保留指定專案的第一個位置。

## <a name="syntax"></a>語法


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObj* 
</dt> <dd>

專案的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回位置值，如果專案不在清單中，則 **為 Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxlist (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseList 類別**](cbaselist.md)
</dt> </dl>

 

 




