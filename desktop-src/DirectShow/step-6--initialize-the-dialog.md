---
description: 步驟 6.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: 步驟 6. 初始化對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992077"
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

 

 



