---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673768"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="0f9cb-103">IAgentPropertySheet::SetPage</span><span class="sxs-lookup"><span data-stu-id="0f9cb-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="0f9cb-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0f9cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="0f9cb-105">設定 Microsoft Agent 屬性工作表的目前頁面。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="0f9cb-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0f9cb-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="0f9cb-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="0f9cb-108">設定屬性目前頁面的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="0f9cb-109">參數可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="0f9cb-110">**詞性**</span><span class="sxs-lookup"><span data-stu-id="0f9cb-110">**"Speech"**</span></span>    | <span data-ttu-id="0f9cb-111">語音輸入頁面。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-111">The Speech Input page.</span></span> |
| <span data-ttu-id="0f9cb-112">**出**</span><span class="sxs-lookup"><span data-stu-id="0f9cb-112">**"Output"**</span></span>    | <span data-ttu-id="0f9cb-113">輸出頁面。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-113">The Output page.</span></span>       |
| <span data-ttu-id="0f9cb-114">**版權法**</span><span class="sxs-lookup"><span data-stu-id="0f9cb-114">**"Copyright"**</span></span> | <span data-ttu-id="0f9cb-115">著作權頁面。</span><span class="sxs-lookup"><span data-stu-id="0f9cb-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0f9cb-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f9cb-116">See Also</span></span>

[<span data-ttu-id="0f9cb-117">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="0f9cb-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




