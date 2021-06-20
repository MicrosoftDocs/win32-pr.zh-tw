---
description: 覆寫 CBasePropertyPage：： OnActivate 方法，在建立自訂 DirectShow 篩選的篩選屬性頁時，將對話方塊初始化。
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: 步驟 6. 初始化對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404491"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="c473f-104">步驟 6.</span><span class="sxs-lookup"><span data-stu-id="c473f-104">Step 6.</span></span> <span data-ttu-id="c473f-105">初始化對話方塊</span><span class="sxs-lookup"><span data-stu-id="c473f-105">Initialize the Dialog</span></span>

<span data-ttu-id="c473f-106">覆寫 [**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md) 方法，以初始化對話方塊。</span><span class="sxs-lookup"><span data-stu-id="c473f-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="c473f-107">在此範例中，屬性頁使用滑杆控制項，因此 **OnActivate** 的第一個步驟是初始化通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="c473f-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="c473f-108">方法接著會使用篩選的飽和度屬性目前的值，初始化滑杆控制項：</span><span class="sxs-lookup"><span data-stu-id="c473f-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


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



<span data-ttu-id="c473f-109">下一 [步：步驟7。處理視窗訊息](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="c473f-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c473f-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c473f-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c473f-111">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="c473f-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



