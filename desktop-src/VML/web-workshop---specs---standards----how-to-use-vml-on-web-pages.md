---
title: 如何在網頁上使用 VML
description: 如何在網頁上使用 VML
ms.assetid: ae20b789-1890-4560-bcc0-536f126c5a41
keywords:
- Vector Markup Language (VML) 、網路研討會
- " (Vector Markup Language) 的網路研討會"
- 向量圖形，網路研討會
- Vector Markup Language (VML) 、設計網頁
- VML (Vector Markup Language) ，設計網頁
- 向量圖形，設計網頁
- 設計網頁、VML 工作
- 網路研討會，VML 工作
- '設計網頁、Vector Markup Language (VML) '
- '網路研討會，Vector Markup Language (VML) '
- 'Vector Markup Language (VML) ，全球資訊網協會 (W3C) '
- 'VML (Vector Markup Language) ，全球資訊網協會 (W3C) '
- '向量圖形，全球資訊網協會 (W3C) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189353fd5a6c50ffbdcf3fe2ad3efe7e82b8e219
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106991294"
---
# <a name="how-to-use-vml-on-webpages"></a><span data-ttu-id="6cd46-116">如何在網頁上使用 VML</span><span class="sxs-lookup"><span data-stu-id="6cd46-116">How to Use VML on Webpages</span></span>

<span data-ttu-id="6cd46-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="6cd46-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6cd46-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="6cd46-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6cd46-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="6cd46-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6cd46-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="6cd46-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6cd46-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="6cd46-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6cd46-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="6cd46-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6cd46-123">本檔補充提交至全球資訊網協會 (W3C) [Vector Markup Language (VML) 規格](https://www.w3.org/TR/NOTE-datetime.html) 。</span><span class="sxs-lookup"><span data-stu-id="6cd46-123">This document supplements the [Vector Markup Language (VML) specification](https://www.w3.org/TR/NOTE-datetime.html) that was submitted to the World Wide Web Consortium (W3C).</span></span> <span data-ttu-id="6cd46-124">使用此檔和完整的 VML 規格時，您應該能夠使用 VML 來設計網頁。</span><span class="sxs-lookup"><span data-stu-id="6cd46-124">With this document and the complete VML specification, you should be able to use VML to design webpages.</span></span> <span data-ttu-id="6cd46-125">我們假設您已經具備 HTML 的實用知識。</span><span class="sxs-lookup"><span data-stu-id="6cd46-125">We have assumed that you already have a working knowledge of HTML.</span></span>

## <a name="part-i-basic-topics"></a><span data-ttu-id="6cd46-126">第 I 部分：基本主題</span><span class="sxs-lookup"><span data-stu-id="6cd46-126">Part I: Basic Topics</span></span>

-   [<span data-ttu-id="6cd46-127">繪製基本圖形</span><span class="sxs-lookup"><span data-stu-id="6cd46-127">Drawing Basic Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----drawing-basic-shapes.md)
-   [<span data-ttu-id="6cd46-128">使用預先定義的圖形</span><span class="sxs-lookup"><span data-stu-id="6cd46-128">Using Predefined Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----using-predefined-shapes.md)
-   [<span data-ttu-id="6cd46-129">著色圖形</span><span class="sxs-lookup"><span data-stu-id="6cd46-129">Coloring Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----coloring-shapes.md)
-   [<span data-ttu-id="6cd46-130">調整形狀</span><span class="sxs-lookup"><span data-stu-id="6cd46-130">Scaling Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md)
-   [<span data-ttu-id="6cd46-131">定點陣圖形</span><span class="sxs-lookup"><span data-stu-id="6cd46-131">Positioning Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----positioning-shapes.md)
-   [<span data-ttu-id="6cd46-132">將圖形分組</span><span class="sxs-lookup"><span data-stu-id="6cd46-132">Grouping Shapes</span></span>](web-workshop---how-to-use-vml-on-web-pages----grouping-shapes.md)

## <a name="part-ii-advanced-topics"></a><span data-ttu-id="6cd46-133">第 II 部分： Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="6cd46-133">Part II: Advanced Topics</span></span>

-   [<span data-ttu-id="6cd46-134">使用 Shapetype 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-134">Using the Shapetype Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shapetype--element.md)
-   [<span data-ttu-id="6cd46-135">使用 Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-135">Using the Stroke Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----stroke--element.md)
-   [<span data-ttu-id="6cd46-136">使用 Fill 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-136">Using the Fill Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)
-   [<span data-ttu-id="6cd46-137">使用 Image 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-137">Using the Image Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----image--element.md)
-   [<span data-ttu-id="6cd46-138">使用 Background 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-138">Using the Background Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----background--element.md)
-   [<span data-ttu-id="6cd46-139">使用 Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-139">Using the Shadow Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----shadow--element.md)
-   [<span data-ttu-id="6cd46-140">使用 Path 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-140">Using the Path Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----path--element.md)
-   [<span data-ttu-id="6cd46-141">使用 Textbox 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-141">Using the Textbox Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textbox--element.md)
-   [<span data-ttu-id="6cd46-142">使用本機座標空間</span><span class="sxs-lookup"><span data-stu-id="6cd46-142">Using Local Coordinate Space</span></span>](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md)
-   [<span data-ttu-id="6cd46-143">使用公式元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-143">Using the Formulas Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----formulas--element.md)
-   [<span data-ttu-id="6cd46-144">使用 Handles 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-144">Using the Handles Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----handles--element.md)
-   [<span data-ttu-id="6cd46-145">使用 Textpath 元素</span><span class="sxs-lookup"><span data-stu-id="6cd46-145">Using the Textpath Element</span></span>](web-workshop---how-to-use-vml-on-web-pages-----textpath--element.md)

> [!Note]  
> <span data-ttu-id="6cd46-146">本參考中提供的範例是針對 Internet Explorer 所設計。</span><span class="sxs-lookup"><span data-stu-id="6cd46-146">The samples provided in this reference are designed for Internet Explorer.</span></span> <span data-ttu-id="6cd46-147">我們也盡可能提供圖例。</span><span class="sxs-lookup"><span data-stu-id="6cd46-147">We have also provided illustrations where possible.</span></span>

 

 

 