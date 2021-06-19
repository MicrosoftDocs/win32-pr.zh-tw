---
title: 將圖形分組
description: 本文描述如何在 VML 中將圖形分組，這是 Windows Internet Explorer 9 所淘汰的功能。
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- 網路研討會，群組圖形
- 設計網頁、群組圖形
- Vector Markup Language (VML) 、群組圖形
- VML (Vector Markup Language) 、群組圖案
- 向量圖形，群組圖形
- VML 圖形，群組
- 將圖形分組
- Vector Markup Language (VML) 、group 元素
- VML (Vector Markup Language) ，group 元素
- 向量圖形、群組元素
- 群組元素
- VML 元素、群組
- Vector Markup Language (VML) 、本機座標空間
- VML (Vector Markup Language) ，區域座標空間
- 向量圖形，區域座標空間
- 本機座標空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407701"
---
# <a name="grouping-shapes"></a><span data-ttu-id="91245-119">將圖形分組</span><span class="sxs-lookup"><span data-stu-id="91245-119">Grouping Shapes</span></span>

<span data-ttu-id="91245-120">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="91245-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="91245-121">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="91245-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="91245-122">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="91245-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="91245-123">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="91245-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="91245-124">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="91245-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="91245-125">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="91245-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="91245-126">如您所學到的，您可以使用 VML 輕鬆地繪製個別的圖案。</span><span class="sxs-lookup"><span data-stu-id="91245-126">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="91245-127">在本節中，我們將說明將圖形群組在一起的優點，以及如何將圖形分組。</span><span class="sxs-lookup"><span data-stu-id="91245-127">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="91245-128">如果您有許多需要調整、移動或旋轉的圖形，您會發現為每個圖形個別設定屬性是很繁瑣的。</span><span class="sxs-lookup"><span data-stu-id="91245-128">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="91245-129">此外，您也會引發錯誤的邊際。</span><span class="sxs-lookup"><span data-stu-id="91245-129">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="91245-130">如果您可以將圖形分組，然後設定整個群組的屬性，就會比較好。</span><span class="sxs-lookup"><span data-stu-id="91245-130">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="91245-131">在 VML 中，您可以使用專案 `<group>` 將許多圖形群組在一起，讓它們可以轉換成一個單位。</span><span class="sxs-lookup"><span data-stu-id="91245-131">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="91245-132">例如，如下列 VML 標記法所示，您可以輕鬆地將兩個圖形群組在一起。</span><span class="sxs-lookup"><span data-stu-id="91245-132">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="91245-133">當將圖形分組時，它們會使用群組的 [區域座標空間](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) 。</span><span class="sxs-lookup"><span data-stu-id="91245-133">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="91245-134">因此，群組內的圖形可以進行調整，並一起移動。</span><span class="sxs-lookup"><span data-stu-id="91245-134">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="91245-135">您將會在 [使用本機座標空間] 主題中看到更多範例。</span><span class="sxs-lookup"><span data-stu-id="91245-135">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="91245-136">在群組內，您可以依需要擁有任意數量的圖形或群組。</span><span class="sxs-lookup"><span data-stu-id="91245-136">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="91245-137">當群組位於另一個群組內時，它稱為「嵌套群組」。</span><span class="sxs-lookup"><span data-stu-id="91245-137">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="91245-138">嵌套層級沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="91245-138">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="91245-139">例如，下列程式程式碼會示範3層級的嵌套群組。</span><span class="sxs-lookup"><span data-stu-id="91245-139">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="91245-140">Shape3 和 Shape4 在 GroupC 中。</span><span class="sxs-lookup"><span data-stu-id="91245-140">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="91245-141">Shape2 和 GroupC 在 GroupB 中。</span><span class="sxs-lookup"><span data-stu-id="91245-141">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="91245-142">Shape1 和 GroupB 在 GroupA 中。</span><span class="sxs-lookup"><span data-stu-id="91245-142">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="91245-143">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858388) 。</span><span class="sxs-lookup"><span data-stu-id="91245-143">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="91245-144">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="91245-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="91245-145">總結</span><span class="sxs-lookup"><span data-stu-id="91245-145">Summary</span></span>

<span data-ttu-id="91245-146">您可以使用專案 `<group>` 將許多圖形群組在一起，讓它們可以轉換成一個單位。</span><span class="sxs-lookup"><span data-stu-id="91245-146">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 