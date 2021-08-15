---
description: GetPageInfo 方法會抓取屬性頁的相關資訊。 這個方法會實 IPropertyPage：： GetPageInfo 方法。
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: 'CBasePropertyPage. GetPageInfo 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: badb0678faa85b70dfa848bba7538319b905feea440339e24285f3d64b59d61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823158"
---
# <a name="cbasepropertypagegetpageinfo-method"></a>CBasePropertyPage. GetPageInfo 方法

方法會抓取 `GetPageInfo` 屬性頁的相關資訊。 這個方法會實 **IPropertyPage：： GetPageInfo** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPageInfo* 
</dt> <dd>

呼叫端配置之 **PROPPAGEINFO** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                   | Description                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




