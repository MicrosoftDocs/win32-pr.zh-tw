---
title: Echo 範例屬性
description: Echo 範例屬性
ms.assetid: 16f6f963-d746-42dc-872f-6f4db296cab9
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ae368a75817320e346dab7e3061fb6b3d7d490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372379"
---
# <a name="echo-sample-properties"></a><span data-ttu-id="fd5c0-108">Echo 範例屬性</span><span class="sxs-lookup"><span data-stu-id="fd5c0-108">Echo Sample Properties</span></span>

<span data-ttu-id="fd5c0-109">Echo 範例會公開兩個屬性：延遲時間和效果層級 (濕混合) 。</span><span class="sxs-lookup"><span data-stu-id="fd5c0-109">The Echo sample exposes two properties: the delay time and the effect level (wet mix).</span></span> <span data-ttu-id="fd5c0-110">「幹信號」層級 (試混合) 的值一律衍生自濕混合值。</span><span class="sxs-lookup"><span data-stu-id="fd5c0-110">The value for the dry signal level (dry mix) is always derived from the wet mix value.</span></span> <span data-ttu-id="fd5c0-111">您需要修改現有的程式碼，並新增一些新的程式碼，使這些屬性可供存取。</span><span class="sxs-lookup"><span data-stu-id="fd5c0-111">You need to modify existing code and add some new code to make these properties accessible.</span></span>

<span data-ttu-id="fd5c0-112">下列各節說明如何修改屬性程式碼：</span><span class="sxs-lookup"><span data-stu-id="fd5c0-112">The following sections explain how to modify the properties code:</span></span>

-   [<span data-ttu-id="fd5c0-113">屬性的運作方式</span><span class="sxs-lookup"><span data-stu-id="fd5c0-113">How Properties Work</span></span>](how-properties-work.md)
-   [<span data-ttu-id="fd5c0-114">用來儲存屬性的變數</span><span class="sxs-lookup"><span data-stu-id="fd5c0-114">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="fd5c0-115">修改尺規屬性</span><span class="sxs-lookup"><span data-stu-id="fd5c0-115">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="fd5c0-116">新增濕混合屬性</span><span class="sxs-lookup"><span data-stu-id="fd5c0-116">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="fd5c0-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd5c0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd5c0-118">**Echo 範例**</span><span class="sxs-lookup"><span data-stu-id="fd5c0-118">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




