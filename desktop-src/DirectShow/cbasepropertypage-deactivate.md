---
description: 停用方法會終結對話方塊視窗。 這個方法會實 IPropertyPage：:D eactivate 方法。
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: CBasePropertyPage) 停用方法 (Cprop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5acb906a28087464f349aff3fdcdf367d7e3bceaa5a29cfa1cad4143b80e10c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526768"
---
# <a name="cbasepropertypagedeactivate-method"></a>CBasePropertyPage. Deactivate 方法

方法會終結 `Deactivate` 對話方塊視窗。 這個方法會實 **IPropertyPage：:D eactivate** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>            |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage::OnDeactivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




