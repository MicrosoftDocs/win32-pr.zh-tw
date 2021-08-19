---
description: 覆寫 CBasePropertyPage：： OnActivate 方法，在建立自訂 DirectShow 篩選的篩選屬性頁時，將對話方塊初始化。
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: 步驟 6. 初始化對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102308"
---
# <a name="step-6-initialize-the-dialog"></a>步驟 6. 初始化對話方塊

覆寫 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法，以初始化對話方塊。 在此範例中，屬性頁使用滑杆控制項，因此 **OnActivate** 的第一個步驟是初始化通用控制項程式庫。 方法接著會使用篩選的飽和度屬性目前的值，初始化滑杆控制項：


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



下一 [步：步驟7。處理視窗訊息](step-7--handle-window-messages.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



