---
description: CUnknown。 CUnknown 函式-函數方法。
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: 'CUnknown. CUnknown (Combase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7d2f1b70202200c705394790bb4b1e8d81349b71f534cc36fba9a8baed65f03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998928"
---
# <a name="cunknowncunknown-constructor"></a>CUnknown. CUnknown 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含物件名稱的字串;用於 [**CBaseObject**](cbaseobject.md) 的函式以進行調試。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 IUnknown 介面。 否則，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

以零的參考計數來初始化物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




