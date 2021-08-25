---
description: CTransformFilter。 CTransformFilter 函式-函數方法。
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: 'CTransformFilter. CTransformFilter (Transfrm. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44061a753ef61c784298fe23e70f21fe410a9f0ad5f360acc10cb1fd16dd5f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907687"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>CTransformFilter. CTransformFilter 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObjectName* 
</dt> <dd>

包含篩選的偵錯工具名稱的字串。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*lpUnk* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*Clsid* 
</dt> <dd>

篩選準則的類別識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

此函式不會建立篩選器的釘選。 這是在第一次呼叫 [**GetPin**](ctransformfilter-getpin.md) 方法期間發生的。 此函數會將 [**m \_ pInput**](ctransformfilter-m-pinput.md) 和 [**m \_ POutput**](ctransformfilter-m-poutput.md) 成員變數初始化為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransformFilter 類別**](ctransformfilter.md)
</dt> </dl>

 

 




