---
description: 當屬性頁應該釋放相關聯的物件時，就會呼叫 OnDisconnect 方法。
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: 'CBasePropertyPage. OnDisconnect 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8231ce81ef6cc2d593e26c99ba9f285fc2f7b9215349b6ec0eb73661cc8a969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000810"
---
# <a name="cbasepropertypageondisconnect-method"></a>CBasePropertyPage. OnDisconnect 方法

`OnDisconnect`當屬性頁應該釋放相關聯的物件時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

基底類別執行會傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBasePropertyPage：： SetObjects**](cbasepropertypage-setobjects.md)方法會呼叫 `OnDisconnect` 方法。 覆寫 `OnDisconnect` 以釋放在 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法中取得的任何指標。

## <a name="examples"></a>範例


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
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

 

 




