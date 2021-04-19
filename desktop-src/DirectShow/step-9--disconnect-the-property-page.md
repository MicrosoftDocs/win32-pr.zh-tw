---
description: 步驟 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: 步驟 9. 中斷屬性頁面的連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59c620179e95afa3f1b949ed40cbfc3a2bca11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988940"
---
# <a name="step-9-disconnect-the-property-page"></a><span data-ttu-id="3ba07-104">步驟 9.</span><span class="sxs-lookup"><span data-stu-id="3ba07-104">Step 9.</span></span> <span data-ttu-id="3ba07-105">中斷屬性頁面的連線</span><span class="sxs-lookup"><span data-stu-id="3ba07-105">Disconnect the Property Page</span></span>

<span data-ttu-id="3ba07-106">覆寫 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法，以釋放您在 **OnConnect** 方法中取得的任何介面。</span><span class="sxs-lookup"><span data-stu-id="3ba07-106">Override the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method to release any interfaces that you obtained in the **OnConnect** method.</span></span> <span data-ttu-id="3ba07-107">此外，如果使用者在不認可變更的情況下關閉屬性工作表，您應該在原始值變更時還原它們。</span><span class="sxs-lookup"><span data-stu-id="3ba07-107">Also, if the user dismisses the property sheet without committing the changes, you should restore the original values if they have changed.</span></span> <span data-ttu-id="3ba07-108">當使用者取消時，不會呼叫 "OnCancel" 方法，因此您需要追蹤使用者是否已呼叫 **OnApplyChanges**。</span><span class="sxs-lookup"><span data-stu-id="3ba07-108">There is no "OnCancel" method that gets called when the user cancels, so you need to keep track of whether the user has called **OnApplyChanges**.</span></span> <span data-ttu-id="3ba07-109">此範例會使用稍 \_ 早所述的 m lVal 變數：</span><span class="sxs-lookup"><span data-stu-id="3ba07-109">This example uses the m\_lVal variable, described earlier:</span></span>


```C++
HRESULT CGrayProp::OnDisconnect(void)
{
    if (m_pGray)
    {
        // If the user clicked OK, m_lVal holds the new value.
        // Otherwise, if the user clicked Cancel, m_lVal is the old value.
        m_pGray->SetSaturation(m_lVal);  
        m_pGray->Release();
        m_pGray = NULL;
    }
    return S_OK;
}
```



<span data-ttu-id="3ba07-110">下一 [步：步驟10。支援 COM 註冊](step-10--support-com-registration.md)</span><span class="sxs-lookup"><span data-stu-id="3ba07-110">Next: [Step 10. Support COM Registration](step-10--support-com-registration.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ba07-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ba07-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ba07-112">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="3ba07-112">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



