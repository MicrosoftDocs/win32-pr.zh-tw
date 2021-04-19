---
description: 函式方法。
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: 'CBasePropertyPage. CBasePropertyPage (Cprop. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994580"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>CBasePropertyPage. CBasePropertyPage 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

字串，包含物件的名稱，用於進行調試。 如需詳細資訊，請參閱 [**CBaseObject：： CBaseObject**](cbaseobject-cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

匯總 **IUnknown** 介面的指標。

</dd> <dt>

*DialogId* 
</dt> <dd>

對話方塊的資源識別碼。

</dd> <dt>

*TitleId* 
</dt> <dd>

包含對話方塊標題之字串的資源識別碼。

</dd> </dl>

## <a name="examples"></a>範例


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




