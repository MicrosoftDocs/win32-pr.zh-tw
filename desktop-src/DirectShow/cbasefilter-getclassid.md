---
description: GetClassID 方法會捕獲篩選準則的類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: 'CBaseFilter. GetClassID 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977551"
---
# <a name="cbasefiltergetclassid-method"></a>CBaseFilter. GetClassID 方法

方法會抓取 `GetClassID` 篩選準則的類別識別碼。 這個方法會實 **IPersist：： GetClassID** 方法。

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

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 




