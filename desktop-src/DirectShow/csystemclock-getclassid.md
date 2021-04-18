---
description: GetClassID 方法會抓取物件 (CLSID) 的類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: 'CSystemClock. GetClassID 方法 (Sysclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976281"
---
# <a name="csystemclockgetclassid-method"></a>CSystemClock. GetClassID 方法

方法會抓取 `GetClassID` 物件 (CLSID) 的類別識別碼。 這個方法會實 **IPersist：： GetClassID** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pClsID* 
</dt> <dd>

接收值 CLSID SystemClock 之變數的指標 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | CSystemClock 類別<br/>                                                                                                                                                              |
| 標頭<br/>  | <dl> <dt>Sysclock (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




