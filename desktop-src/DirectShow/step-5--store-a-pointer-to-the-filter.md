---
description: 將篩選準則儲存為自訂 DirectShow 篩選準則的建立篩選屬性頁的一部分。
ms.assetid: 7c715129-5bdf-468f-96cd-a46ab9c97f4c
title: 步驟 5。 將指標儲存至篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa1e98e98fcc0f41d07774b8a2d1ab93dea8d0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406791"
---
# <a name="step-5-store-a-pointer-to-the-filter"></a><span data-ttu-id="827ab-104">步驟 5。</span><span class="sxs-lookup"><span data-stu-id="827ab-104">Step 5.</span></span> <span data-ttu-id="827ab-105">將指標儲存至篩選</span><span class="sxs-lookup"><span data-stu-id="827ab-105">Store a Pointer to the Filter</span></span>

<span data-ttu-id="827ab-106">覆寫 [**CBasePropertyPage：： OnConnect**](cbasepropertypage-onconnect.md) 方法，將指標儲存至篩選。</span><span class="sxs-lookup"><span data-stu-id="827ab-106">Override the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to store a pointer to the filter.</span></span> <span data-ttu-id="827ab-107">下列範例會查詢篩選自訂 ISaturation 介面的 *pUnk* 參數：</span><span class="sxs-lookup"><span data-stu-id="827ab-107">The following example queries the *pUnk* parameter for the filter's custom ISaturation interface:</span></span>


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



<span data-ttu-id="827ab-108">下一 [步：步驟6。初始化對話方塊](step-6--initialize-the-dialog.md)。</span><span class="sxs-lookup"><span data-stu-id="827ab-108">Next: [Step 6. Initialize the Dialog](step-6--initialize-the-dialog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="827ab-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="827ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="827ab-110">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="827ab-110">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



