---
description: IsPageDirty 方法會指出屬性頁面在啟動後，或自最近一次呼叫 IPropertyPage：： Apply 之後是否已變更。 這個方法會實 IPropertyPage：： IsPageDirty 方法。
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: 'CBasePropertyPage. IsPageDirty 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990732"
---
# <a name="cbasepropertypageispagedirty-method"></a>CBasePropertyPage. IsPageDirty 方法

`IsPageDirty`方法會指出屬性頁面在啟動後，或自最近一次呼叫 **IPropertyPage：： Apply** 之後是否已變更。 這個方法會實 **IPropertyPage：： IsPageDirty** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md)為 **TRUE**，則傳回 s OK， \_ 否則傳回 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




