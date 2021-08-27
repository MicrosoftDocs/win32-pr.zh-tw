---
description: CVideoTransformFilter。 CVideoTransformFilter 函式-函數方法。
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: 'CVideoTransformFilter. CVideoTransformFilter (Vtrans. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1db2b665a1525f1352844a2963bd44a761a080a058154419b3320f7113aa3740
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086878"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a>CVideoTransformFilter. CVideoTransformFilter 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

包含篩選的偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject：： CBaseObject**](cbaseobject-cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*Clsid* 
</dt> <dd>

篩選準則的類別識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Vtrans (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CVideoTransformFilter 類別**](cvideotransformfilter.md)
</dt> </dl>

 

 




