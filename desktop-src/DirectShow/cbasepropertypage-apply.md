---
description: Apply 方法會將目前的屬性頁值套用至與屬性頁相關聯的物件。 這個方法會實 IPropertyPage：： Apply 方法。
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: 'CBasePropertyPage 將方法套用 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9350aa7aaa4e2bfdcb72385d26b09b9d7a9bdf33deb05e273b0663485da1a5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823228"
---
# <a name="cbasepropertypageapply-method"></a>CBasePropertyPage. Apply 方法

`Apply`方法會將目前的屬性頁值套用至與屬性頁相關聯的物件。 這個方法會實 **IPropertyPage：： Apply** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Apply();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                  | 描述                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>            |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/> |



 

## <a name="remarks"></a>備註

如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md) 旗標為 **TRUE**，這個方法會呼叫 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法。 覆寫 **OnApplyChanges** 以將變更套用至物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> </dl>

 

 




