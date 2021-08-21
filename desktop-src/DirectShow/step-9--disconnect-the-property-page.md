---
description: 步驟 9.
ms.assetid: 3e476422-ab76-4a2b-af9b-d9d065d79e5b
title: 步驟 9. 中斷屬性頁面的連線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf4bcb670b8a8f29334f7ecd41ebba37a915f724be70e5dbbbfd7abea9730be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526078"
---
# <a name="step-9-disconnect-the-property-page"></a>步驟 9. 中斷屬性頁面的連線

覆寫 [**CBasePropertyPage：： OnDisconnect**](cbasepropertypage-ondisconnect.md) 方法，以釋放您在 **OnConnect** 方法中取得的任何介面。 此外，如果使用者在不認可變更的情況下關閉屬性工作表，您應該在原始值變更時還原它們。 當使用者取消時，不會呼叫 "OnCancel" 方法，因此您需要追蹤使用者是否已呼叫 **OnApplyChanges**。 此範例會使用稍 \_ 早所述的 m lVal 變數：


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



下一 [步：步驟10。支援 COM 註冊](step-10--support-com-registration.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



