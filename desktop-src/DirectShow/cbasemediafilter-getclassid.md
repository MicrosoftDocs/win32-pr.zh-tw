---
description: GetClassID 方法會捕獲類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: 'CBaseMediaFilter. GetClassID 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a733c3ef6e7098a556facb5258f567bdae0179ba4da133076b9bbc961cf0b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502918"
---
# <a name="cbasemediafiltergetclassid-method"></a>CBaseMediaFilter. GetClassID 方法

`GetClassID`方法會捕獲類別識別碼。 這個方法會實 **IPersist：： GetClassID** 方法。

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

接收類別識別碼之變數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 S \_ OK 或 E \_ 指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseMediaFilter 類別**](cbasemediafilter.md)
</dt> </dl>

 

 




