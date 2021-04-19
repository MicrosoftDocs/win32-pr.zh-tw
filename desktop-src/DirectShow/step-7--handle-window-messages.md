---
description: 步驟 7：
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: 步驟 7： 處理視窗訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987311"
---
# <a name="step-7-handle-window-messages"></a>步驟 7： 處理視窗訊息

覆寫 [**CBasePropertyPage：： OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) 方法，以更新對話方塊控制項以回應使用者輸入。 如果您未處理特定訊息，請在父類別上呼叫 **OnReceiveMessage** 方法。 每當使用者變更屬性時，請執行下列動作：

-   將 [屬性] 頁面的 **m \_ bDirty** 變數設定為 [ **TRUE**]。
-   使用 PROPPAGESTATUS 中途旗標，呼叫屬性框架的 **IPropertyPageSite：： OnStatusChange** 方法 \_ 。 此旗標會通知屬性框架應該 **啟用 [套用** ] 按鈕。 [**CBasePropertyPage：： m \_ pPageSite**](cbasepropertypage-m-ppagesite.md)成員會保存 **IPropertyPageSite** 介面的指標。

若要簡化這個步驟，您可以將下列 helper 函式新增至您的屬性頁：


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



只要使用者動作變更屬性，就會在 **OnReceiveMessage** 內呼叫這個私用方法，如下列範例所示：


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



此範例中的屬性頁面有兩個控制項：滑動軸和 [ **還原為預設值** ] 按鈕。 如果使用者滾動滑動軸，屬性頁會設定篩選準則的飽和度值。 如果使用者按一下按鈕，屬性頁會還原篩選的預設飽和度值。 在每個案例中，m \_ lNewVal 會保留目前的值，而 m \_ lVal 會保留原始值。 在 \_ 使用者認可變更之前，不會更新 m lVal 的值，這會在使用者按一下屬性框架上的 [  **確定]** 或 [套用] 按鈕時發生。

下一 [步：步驟8。套用屬性變更](step-8--apply-property-changes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



