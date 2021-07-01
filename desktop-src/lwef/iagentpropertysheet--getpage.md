---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119863"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="d4ca9-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="d4ca9-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="d4ca9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d4ca9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="d4ca9-105">抓取 Microsoft Agent 屬性工作表的目前頁面。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="d4ca9-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d4ca9-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="d4ca9-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="d4ca9-108">如果視窗未開啟) ，則為接收屬性工作表目前頁面 (上次查看頁面的變數位址。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="d4ca9-109">參數可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d4ca9-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="d4ca9-110">描述</span><span class="sxs-lookup"><span data-stu-id="d4ca9-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="d4ca9-111">**詞性**</span><span class="sxs-lookup"><span data-stu-id="d4ca9-111">**"Speech"**</span></span>    | <span data-ttu-id="d4ca9-112">語音輸入頁面。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-112">The Speech Input page.</span></span> |
| <span data-ttu-id="d4ca9-113">**出**</span><span class="sxs-lookup"><span data-stu-id="d4ca9-113">**"Output"**</span></span>    | <span data-ttu-id="d4ca9-114">輸出頁面。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-114">The Output page.</span></span>       |
| <span data-ttu-id="d4ca9-115">**版權法**</span><span class="sxs-lookup"><span data-stu-id="d4ca9-115">**"Copyright"**</span></span> | <span data-ttu-id="d4ca9-116">著作權頁面。</span><span class="sxs-lookup"><span data-stu-id="d4ca9-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d4ca9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ca9-117">See Also</span></span>

[<span data-ttu-id="d4ca9-118">**IAgentPropertySheet::SetPage**</span><span class="sxs-lookup"><span data-stu-id="d4ca9-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




