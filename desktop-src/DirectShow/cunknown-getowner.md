---
description: GetOwner 方法會抓取擁有元件的 IUnknown 介面指標。 針對匯總的元件，擁有者是外部元件。 否則，元件擁有本身。
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: 'CUnknown. GetOwner 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993221"
---
# <a name="cunknowngetowner-method"></a>CUnknown. GetOwner 方法

方法會抓取 `GetOwner` 擁有元件的 **IUnknown** 介面指標。 針對匯總的元件，擁有者是外部元件。 否則，元件擁有本身。

## <a name="syntax"></a>語法


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回控制 **IUnknown** 介面的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




