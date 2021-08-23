---
description: ObjectsActive 方法會抓取整個進程的作用中物件計數。
ms.assetid: adbc023a-22b7-44e9-b078-a26831f961cc
title: 'CBaseObject. ObjectsActive 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.ObjectsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea1b85303751531662123662c1af0e1a35799a780842e8b0bcbc912916c94976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640198"
---
# <a name="cbaseobjectobjectsactive-method"></a>CBaseObject. ObjectsActive 方法

方法會抓取 `ObjectsActive` 整個進程的作用中物件計數。

## <a name="syntax"></a>語法


```C++
static LONG ObjectsActive();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回使用中物件的數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseObject 類別**](cbaseobject.md)
</dt> </dl>

 

 




