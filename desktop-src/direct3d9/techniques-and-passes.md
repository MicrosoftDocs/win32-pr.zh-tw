---
description: 技術可提供轉譯肌肉。 技術會封裝決定轉譯樣式的效果狀態。 一項技術是由一或多個階段所組成。
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: " (Direct3D 9) 的技術和傳遞"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973557"
---
# <a name="techniques-and-passes-direct3d-9"></a><span data-ttu-id="f0174-105"> (Direct3D 9) 的技術和傳遞</span><span class="sxs-lookup"><span data-stu-id="f0174-105">Techniques and Passes (Direct3D 9)</span></span>

<span data-ttu-id="f0174-106">技術可提供轉譯肌肉。</span><span class="sxs-lookup"><span data-stu-id="f0174-106">Techniques provide the rendering muscle.</span></span> <span data-ttu-id="f0174-107">技術會封裝決定轉譯樣式的效果狀態。</span><span class="sxs-lookup"><span data-stu-id="f0174-107">A technique encapsulates the effect state that determines a rendering style.</span></span> <span data-ttu-id="f0174-108">一項技術是由一或多個階段所組成。</span><span class="sxs-lookup"><span data-stu-id="f0174-108">A technique is made up of one or more passes.</span></span>

## <a name="techniques"></a><span data-ttu-id="f0174-109">技術</span><span class="sxs-lookup"><span data-stu-id="f0174-109">Techniques</span></span>

<span data-ttu-id="f0174-110">呼叫技術的語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="f0174-110">The syntax for calling a technique is as follows:</span></span>


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



<span data-ttu-id="f0174-111">其中：</span><span class="sxs-lookup"><span data-stu-id="f0174-111">Where:</span></span>

-   <span data-ttu-id="f0174-112">識別碼是選擇性的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="f0174-112">id is an optional unique name.</span></span>
-   <span data-ttu-id="f0174-113">批註是零或多個選擇性的使用者特定資訊。</span><span class="sxs-lookup"><span data-stu-id="f0174-113">annotation is zero or more optional pieces of user-specific information.</span></span> <span data-ttu-id="f0174-114">請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="f0174-114">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="f0174-115">pass (es) 為零或多個行程。</span><span class="sxs-lookup"><span data-stu-id="f0174-115">pass(es) is zero or more passes.</span></span> <span data-ttu-id="f0174-116">每個階段都包含狀態指派。</span><span class="sxs-lookup"><span data-stu-id="f0174-116">Each pass contains state assignments.</span></span> <span data-ttu-id="f0174-117">請參閱下文。</span><span class="sxs-lookup"><span data-stu-id="f0174-117">See below.</span></span>

## <a name="passes"></a><span data-ttu-id="f0174-118">通過</span><span class="sxs-lookup"><span data-stu-id="f0174-118">Passes</span></span>

<span data-ttu-id="f0174-119">Pass 包含轉譯所需的狀態指派。</span><span class="sxs-lookup"><span data-stu-id="f0174-119">A pass contains the state assignments required to render.</span></span>


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



<span data-ttu-id="f0174-120">其中：</span><span class="sxs-lookup"><span data-stu-id="f0174-120">Where:</span></span>

-   <span data-ttu-id="f0174-121">識別碼是選擇性的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="f0174-121">id is an optional unique name.</span></span>
-   <span data-ttu-id="f0174-122">批註是一或多個選擇性的使用者特定資訊。</span><span class="sxs-lookup"><span data-stu-id="f0174-122">annotation is one or more optional piece of user-specific information.</span></span> <span data-ttu-id="f0174-123">請參閱 [使用 \_ 批註將資訊新增至效果參數](using-an-effect.md)。</span><span class="sxs-lookup"><span data-stu-id="f0174-123">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>
-   <span data-ttu-id="f0174-124">指派 (s) 指派零個以上的狀態值，或評估一或多個運算式。</span><span class="sxs-lookup"><span data-stu-id="f0174-124">assignment(s) assigns zero or more state values, or evaluates one or more expressions.</span></span> <span data-ttu-id="f0174-125">請參閱 [ (direct3d 9) ](effect-states.md) 和 [運算式 (direct3d 9) ](expressions.md)的效果狀態。</span><span class="sxs-lookup"><span data-stu-id="f0174-125">See [Effect States (Direct3D 9)](effect-states.md) and [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="f0174-126">將一組重複指派中的最後一項指派傳遞給相同的狀態，即會略過全部。</span><span class="sxs-lookup"><span data-stu-id="f0174-126">Passes ignore all but the last assignment in a set of repeated assignments to the same state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0174-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0174-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0174-128">效果格式</span><span class="sxs-lookup"><span data-stu-id="f0174-128">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



