---
description: 將篩選的指標儲存為自訂 DirectShow 篩選準則的建立篩選屬性頁的一部分。
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 步驟 5。 將指標儲存至篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63becf4cb98f401a4810f0f9a2604ef65387a58d08d84b9f670c09b51fe9acd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078768"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a>步驟 5。 將指標儲存至篩選

覆寫 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法，將指標儲存至篩選。 下列範例會查詢篩選自訂 ISaturation 介面的 *pUnk* 參數：


```C++
HRESULT CGrayProp::OnConnect(IUnknown *pUnk)
{
    if (pUnk == NULL)
    {
        return E_POINTER;
    }
    ASSERT(m_pGray == NULL);
    return pUnk->QueryInterface(IID_ISaturation, 
        reinterpret_cast<void**>(&m_pGray));
}
```



下一 [步：步驟6。初始化對話方塊](step-6--initialize-the-dialog.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 



