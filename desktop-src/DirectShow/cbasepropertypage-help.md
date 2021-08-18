---
description: Help 方法會叫用屬性頁說明。 這個方法會實 IPropertyPage：： Help 方法。
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: 'CBasePropertyPage： Help 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e2f97f7edd1e719eb44ff1d41929d7cb3864d8117eabb383b4318688adfa537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955087"
---
# <a name="cbasepropertypagehelp-method"></a>CBasePropertyPage. Help 方法

方法會叫用 `Help` 屬性頁說明。 這個方法會實 **IPropertyPage：： Help** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszHelpDir* 
</dt> <dd>

在登錄中屬性頁的 CLSID 資訊中， **HelpDir** 索引鍵下之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 E \_ >notimpl。

## <a name="remarks"></a>備註

在基類中，方法一律會傳回 E \_ >notimpl。 當方法失敗時，框架會呼叫 **IPropertyPage：： GetPageInfo** 來取得說明檔和內容識別碼的名稱。 根據預設，這些都是 **Null**。 為了提供協助，衍生類別可以覆寫 `Help` 方法或 [**CBasePropertyPage：： GetPageInfo**](cbasepropertypage-getpageinfo.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




