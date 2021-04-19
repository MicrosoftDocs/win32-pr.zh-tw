---
description: 步驟 8。
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 步驟 8。 套用屬性變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001741"
---
# <a name="step-8-apply-property-changes"></a><span data-ttu-id="b7e60-104">步驟 8。</span><span class="sxs-lookup"><span data-stu-id="b7e60-104">Step 8.</span></span> <span data-ttu-id="b7e60-105">套用屬性變更</span><span class="sxs-lookup"><span data-stu-id="b7e60-105">Apply Property Changes</span></span>

<span data-ttu-id="b7e60-106">覆寫 [**CBasePropertyPage：： OnApplyChanges**](cbasepropertypage-onapplychanges.md) 方法，以認可任何屬性變更。</span><span class="sxs-lookup"><span data-stu-id="b7e60-106">Override the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method to commit any property changes.</span></span> <span data-ttu-id="b7e60-107">在此範例中， \_ 每當使用者滾動滑動軸時，就會更新 m lNewVal 變數。</span><span class="sxs-lookup"><span data-stu-id="b7e60-107">In this example, the m\_lNewVal variable is updated whenever the user scrolls the slider bar.</span></span> <span data-ttu-id="b7e60-108">**OnApplyChanges** 方法會將此值複製到 m \_ lVal 變數，並覆寫原始值：</span><span class="sxs-lookup"><span data-stu-id="b7e60-108">The **OnApplyChanges** method copies this value into the m\_lVal variable, overwriting the original value:</span></span>


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



<span data-ttu-id="b7e60-109">下一 [步：步驟9。中斷屬性頁面的連接](step-9--disconnect-the-property-page.md)。</span><span class="sxs-lookup"><span data-stu-id="b7e60-109">Next: [Step 9. Disconnect the Property Page](step-9--disconnect-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7e60-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7e60-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7e60-111">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="b7e60-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



