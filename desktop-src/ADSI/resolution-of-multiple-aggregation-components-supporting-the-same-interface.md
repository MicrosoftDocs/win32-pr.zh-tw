---
title: 支援相同介面的多個匯總元件的解析
description: 這種情況很罕見，這兩個延伸模組會對 ADSI 公開相同的介面。
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- 多個支援相同介面 ADSI 之匯總元件的解析
- 多個支援相同介面 ADSI 之匯總元件的解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967596"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="37e87-105">支援相同介面的多個匯總元件的解析</span><span class="sxs-lookup"><span data-stu-id="37e87-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="37e87-106">這種情況很罕見，這兩個延伸模組會對 ADSI 公開相同的介面。</span><span class="sxs-lookup"><span data-stu-id="37e87-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="37e87-107">如果發生這種情況，則適用下列規則：</span><span class="sxs-lookup"><span data-stu-id="37e87-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="37e87-108">如果匯總工具 (ADSI) 和任何擴充物件都支援介面（例如 **IMyInterface**），則 **QueryInterface** 一律會傳回 **IMyInterface** for adsi。</span><span class="sxs-lookup"><span data-stu-id="37e87-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="37e87-109">如果匯總工具 (ADSI) 不支援介面（例如 **IMyInterface**），但有一個以上的擴充物件支援， **QueryInterface** 會傳回登錄中所列的第一個擴充物件的 **IMyInterface** ，以支援該介面。</span><span class="sxs-lookup"><span data-stu-id="37e87-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="37e87-110">請注意，登錄中的元件順序也會影響自動化中名稱衝突的解析。</span><span class="sxs-lookup"><span data-stu-id="37e87-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="37e87-111">如需詳細資訊，請參閱 [擴充功能的自動化中的函數/屬性名稱衝突的解決方式](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="37e87-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 




