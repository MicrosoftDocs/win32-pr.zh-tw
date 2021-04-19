---
description: 函式方法。
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: 'CTransInPlaceFilter. CTransInPlaceFilter (Transip. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990821"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>CTransInPlaceFilter. CTransInPlaceFilter 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
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

</dd> <dt>

*phr* 
</dt> <dd>

忽略。

</dd> <dt>

*bModifiesData* 
</dt> <dd>

指定篩選是否修改輸入資料的布林值。 若 **為 TRUE**，則篩選準則會修改資料。 否則，篩選準則會將未變更的資料傳遞給下游。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceFilter 類別**](ctransinplacefilter.md)
</dt> </dl>

 

 




