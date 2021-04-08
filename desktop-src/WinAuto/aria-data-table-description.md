---
title: ARIA 資料表格警告
description: ARIA 資料表格警告
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021970"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="114ad-104">ARIA 資料表格警告</span><span class="sxs-lookup"><span data-stu-id="114ad-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="114ad-105">Text</span><span class="sxs-lookup"><span data-stu-id="114ad-105">Text</span></span>

<span data-ttu-id="114ad-106">資料表包含資料，但沒有摘要或有效的 **aria describedby** 屬性。</span><span class="sxs-lookup"><span data-stu-id="114ad-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="114ad-107">類型</span><span class="sxs-lookup"><span data-stu-id="114ad-107">Type</span></span>

<span data-ttu-id="114ad-108">警告</span><span class="sxs-lookup"><span data-stu-id="114ad-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="114ad-109">描述</span><span class="sxs-lookup"><span data-stu-id="114ad-109">Description</span></span>

<span data-ttu-id="114ad-110">這項警告適用于具有多個資料格的 HTML 資料表。</span><span class="sxs-lookup"><span data-stu-id="114ad-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="114ad-111">它不會套用至資料表， `role="presentation"` 因為這些會被視為版面配置資料表。</span><span class="sxs-lookup"><span data-stu-id="114ad-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="114ad-112">此警告表示資料表已識別為數據表，但未定義可存取的描述。</span><span class="sxs-lookup"><span data-stu-id="114ad-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="114ad-113">並非所有的資料表都需要有可存取的描述。</span><span class="sxs-lookup"><span data-stu-id="114ad-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="114ad-114">如果使用者需要詳細資訊來瞭解資料表結構和內容，您應該定義可存取的描述。</span><span class="sxs-lookup"><span data-stu-id="114ad-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="114ad-115">若要解決這個警告，請使用 summary 屬性或 **aria describedby** 屬性定義資料表的可存取描述。</span><span class="sxs-lookup"><span data-stu-id="114ad-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="114ad-116">範例</span><span class="sxs-lookup"><span data-stu-id="114ad-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




