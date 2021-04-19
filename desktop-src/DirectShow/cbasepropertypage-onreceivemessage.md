---
description: 當對話方塊收到訊息時，就會呼叫 OnReceiveMessage 方法。
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: 'CBasePropertyPage. OnReceiveMessage 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978612"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>CBasePropertyPage. OnReceiveMessage 方法

`OnReceiveMessage`當對話方塊收到訊息時，就會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

視窗的控制碼。

</dd> <dt>

*uMsg* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

第一個訊息參數。

</dd> <dt>

*lParam* 
</dt> <dd>

第二個訊息參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回布林值。 對話方塊程式會傳回此值;如需詳細資訊，請參閱 Platform SDK 檔。

## <a name="remarks"></a>備註

基底類別的實 **DefWindowProc** 呼叫。 覆寫這個方法，以處理與對話方塊控制項相關的訊息。 如果覆寫方法未處理特定訊息，則應該呼叫基類方法。

如果使用者透過對話方塊控制項變更任何屬性，請將 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md) 旗標設定為 **TRUE**。 然後呼叫 [**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)指標上的 **IPropertyPageSite：： OnStatusChange** 方法來通知框架。

## <a name="examples"></a>範例

下列範例會藉由更新成員變數（假設要在衍生類別中定義）來回應按鈕點擊。 此範例也會顯示用於設定屬性頁變更狀態的 helper 函式。


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
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

 

 




