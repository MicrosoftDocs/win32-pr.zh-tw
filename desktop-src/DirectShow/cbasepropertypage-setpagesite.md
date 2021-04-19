---
description: SetPageSite 方法會初始化屬性頁，並提供屬性框架的 IPropertyPageSite 介面指標。 這個方法會實 IPropertyPage：： SetPageSite 方法。
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: 'CBasePropertyPage. SetPageSite 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999126"
---
# <a name="cbasepropertypagesetpagesite-method"></a>CBasePropertyPage. SetPageSite 方法

`SetPageSite`方法會初始化屬性頁，並提供屬性框架 **IPropertyPageSite** 介面的指標。 這個方法會實 **IPropertyPage：： SetPageSite** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pPageSite* 
</dt> <dd>

**IPropertyPageSite** 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>            |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/> |



 

## <a name="remarks"></a>備註

方法會將 *pPageSite* 指標儲存在 [**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) 成員變數中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




