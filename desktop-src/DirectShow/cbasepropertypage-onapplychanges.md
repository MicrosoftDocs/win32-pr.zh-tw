---
description: 當使用者將變更套用至屬性頁時，會呼叫 OnApplyChanges 方法。
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: 'CBasePropertyPage. OnApplyChanges 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823104"
---
# <a name="cbasepropertypageonapplychanges-method"></a>CBasePropertyPage. OnApplyChanges 方法

`OnApplyChanges`當使用者將變更套用至屬性頁時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

基底類別執行會傳回 S \_ OK。

## <a name="remarks"></a>備註

[](cbasepropertypage-apply.md) `OnApplyChanges` 如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md)旗標為 **TRUE**，則 CBasePropertyPage：： Apply 方法呼叫。 覆寫 `OnApplyChanges` 以處理變更，並將 **m \_ bDirty** 重設為 **FALSE**。

## <a name="examples"></a>範例


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
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

 

 




