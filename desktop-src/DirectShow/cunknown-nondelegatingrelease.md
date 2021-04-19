---
description: 遞減物件的參考計數。 這個方法會實 INonDelegatingUnknown：： NonDelegatingRelease 方法。
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: 'CUnknown. NonDelegatingRelease 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990954"
---
# <a name="cunknownnondelegatingrelease-method"></a>CUnknown. NonDelegatingRelease 方法

遞減物件的參考計數。 這個方法會實 **INonDelegatingUnknown：： NonDelegatingRelease** 方法。

## <a name="syntax"></a>語法


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回參考計數。

## <a name="remarks"></a>備註

當參考計數到達零時，物件就會刪除本身。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




