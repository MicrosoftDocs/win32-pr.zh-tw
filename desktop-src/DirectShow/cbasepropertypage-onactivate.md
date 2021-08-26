---
description: 當屬性頁啟用時，會呼叫 OnActivate 方法。
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: 'CBasePropertyPage. OnActivate 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052568"
---
# <a name="cbasepropertypageonactivate-method"></a>CBasePropertyPage. OnActivate 方法

`OnActivate`當屬性頁啟用時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

基底類別執行會傳回 S \_ OK。

## <a name="remarks"></a>備註

[**CBasePropertyPage：： Activate**](cbasepropertypage-activate.md)方法會呼叫 `OnActivate` 方法。 在您的衍生類別中，覆寫 `OnActivate` 以初始化對話方塊。

## <a name="examples"></a>範例

下列範例會初始化 [執行] 控制項。 此範例假設 **m \_ pOwningFilter** 是與屬性頁相關聯之篩選準則的自訂介面指標。  (使用 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法來初始化這類指標。 ) 


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
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

 

 




