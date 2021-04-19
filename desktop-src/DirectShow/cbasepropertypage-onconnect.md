---
description: OnConnect 方法會提供 IUnknown 指標給與屬性頁相關聯的物件。
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: 'CBasePropertyPage. OnConnect 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984431"
---
# <a name="cbasepropertypageonconnect-method"></a>CBasePropertyPage. OnConnect 方法

`OnConnect`方法會提供 **IUnknown** 指標給與屬性頁相關聯的物件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pUnknown* 
</dt> <dd>

物件的 **IUnknown** 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

基底類別執行會傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBasePropertyPage：： SetObjects**](cbasepropertypage-setobjects.md)方法會呼叫 `OnConnect` 方法。 覆寫這個方法，將指標儲存至 *pUnknown* 所指定的物件。 您可以儲存 *pUnknown* 指標本身，或針對其他介面查詢該指標。 如果您儲存 *pUnknown* 指標，請在傳回之前呼叫 **AddRef** `OnConnect` 。

在 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法中，使用儲存的指標 (或指標) 來取得對話屬性的初始值。 在 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法中，將任何變更套用回物件。 釋放 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法中的所有指標。

## <a name="examples"></a>範例


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




