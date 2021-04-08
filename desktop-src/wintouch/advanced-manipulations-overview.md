---
title: Advanced 操作總覽
description: 本節說明適用于應用程式的 advanced 操作。
ms.assetid: a0c3fecb-d3c7-4f12-90be-5f77f4f5883e
keywords:
- Windows Touch，操作
- Windows Touch，advanced 操作
- Windows Touch，複雜的操作
- Windows Touch，擴充
- Windows Touch，advanced 擴充
- Windows Touch，旋轉
- Windows Touch，先進的旋轉
- Windows Touch，翻譯
- Windows Touch，advanced 翻譯
- 操作，advanced
- 操作，複雜
- 操作，擴充
- 操作，advanced 擴充
- 操作，旋轉
- 操作，先進的旋轉
- 操作，轉譯
- 操作，advanced 翻譯
- 展開，advanced
- 旋轉，advanced
- 翻譯，advanced
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f58a5dffb3c2d11e07a8c6495ec777579916481
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020936"
---
# <a name="advanced-manipulations-overview"></a><span data-ttu-id="148b2-123">Advanced 操作總覽</span><span class="sxs-lookup"><span data-stu-id="148b2-123">Advanced Manipulations Overview</span></span>

<span data-ttu-id="148b2-124">本節說明適用于應用程式的 advanced 操作。</span><span class="sxs-lookup"><span data-stu-id="148b2-124">This section explains advanced manipulations for applications.</span></span>

<span data-ttu-id="148b2-125">基於可用性的考慮，您可能會想要在應用程式中加入複雜的操作，讓物件能夠以精細的細微性來操作。</span><span class="sxs-lookup"><span data-stu-id="148b2-125">For usability purposes, you may want to add complex manipulations to your application so that objects can be manipulated with a fine degree of granularity.</span></span> <span data-ttu-id="148b2-126">下列各節說明 advanced 操作。</span><span class="sxs-lookup"><span data-stu-id="148b2-126">The following sections describe advanced manipulations.</span></span>

### <a name="advanced-expansion"></a><span data-ttu-id="148b2-127">Advanced 擴充</span><span class="sxs-lookup"><span data-stu-id="148b2-127">Advanced Expansion</span></span>

<span data-ttu-id="148b2-128">下圖顯示兩個擴充的解釋。</span><span class="sxs-lookup"><span data-stu-id="148b2-128">The following illustration shows two interpretations of expansion.</span></span>

![圖例顯示物件中心點周圍的簡單展開，以及圍繞操作中心點的先進展開](images/expansion.png)

<span data-ttu-id="148b2-130">例如，簡單的展開範例中，物件會圍繞其中心點展開。</span><span class="sxs-lookup"><span data-stu-id="148b2-130">In example A, the simple expansion example, the object is expanded around its center point.</span></span> <span data-ttu-id="148b2-131">在 B 範例中，物件是在操作中心點周圍展開。</span><span class="sxs-lookup"><span data-stu-id="148b2-131">In example B, the object is expanded around the center point of the manipulation.</span></span>

### <a name="advanced-rotation"></a><span data-ttu-id="148b2-132">先進旋轉</span><span class="sxs-lookup"><span data-stu-id="148b2-132">Advanced Rotation</span></span>

<span data-ttu-id="148b2-133">下圖顯示兩個旋轉的解釋。</span><span class="sxs-lookup"><span data-stu-id="148b2-133">The following illustration shows two interpretations of rotation.</span></span>

![顯示兩種類型的單一手指旋轉的圖例：圍繞在中央或邊緣，邊緣都牽涉到旋轉和平移](images/rotation.png)

<span data-ttu-id="148b2-135">例如，簡單的旋轉範例中，物件會圍繞其中心點旋轉。</span><span class="sxs-lookup"><span data-stu-id="148b2-135">In example A, the simple rotation example, the object is rotated around its center point.</span></span> <span data-ttu-id="148b2-136">在 B 範例中，物件會圍繞操作的中心點旋轉。</span><span class="sxs-lookup"><span data-stu-id="148b2-136">In example B, the object is rotated around the center point of the manipulation.</span></span> <span data-ttu-id="148b2-137">如需複雜旋轉的詳細資訊，請參閱 [Advanced 輪替](advanced-rotation.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="148b2-137">For more information on complex rotation, see the [Advanced Rotation](advanced-rotation.md) section.</span></span>

## <a name="advanced-translation"></a><span data-ttu-id="148b2-138">Advanced 翻譯</span><span class="sxs-lookup"><span data-stu-id="148b2-138">Advanced Translation</span></span>

<span data-ttu-id="148b2-139">下圖顯示兩個轉譯的解釋。</span><span class="sxs-lookup"><span data-stu-id="148b2-139">The following illustration shows two interpretations of translation.</span></span>

![顯示簡單轉譯的圖例，其中的物件不需要旋轉，而是包含移動和旋轉的先進轉譯](images/translation.png)

<span data-ttu-id="148b2-141">在範例 A 中，簡單的轉譯範例會移動物件，而不會旋轉。</span><span class="sxs-lookup"><span data-stu-id="148b2-141">In example A, the simple translation example, the object is moved without rotation.</span></span> <span data-ttu-id="148b2-142">在 B 範例中，物件會在轉譯期間旋轉，視物件接觸點的位置而定。</span><span class="sxs-lookup"><span data-stu-id="148b2-142">In example B, the object is rotated during the translation depending on where the object contact point is.</span></span> <span data-ttu-id="148b2-143">如果您啟用單一手指旋轉（如 [單一手指旋轉](single-finger-rotation.md)所述），您可以啟用複雜轉譯。</span><span class="sxs-lookup"><span data-stu-id="148b2-143">If you enable single-finger rotation as described in [Single-Finger Rotation](single-finger-rotation.md), you can enable complex translation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="148b2-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="148b2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148b2-145">操作</span><span class="sxs-lookup"><span data-stu-id="148b2-145">Manipulations</span></span>](getting-started-with-manipulations.md)
</dt> </dl>

 

 




