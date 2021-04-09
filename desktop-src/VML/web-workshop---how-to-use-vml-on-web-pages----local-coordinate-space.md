---
title: 使用本機座標空間
description: 使用本機座標空間
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- 網路研討會，區域座標空間
- 設計網頁，區域座標空間
- Vector Markup Language (VML) 、本機座標空間
- VML (Vector Markup Language) ，區域座標空間
- 向量圖形，區域座標空間
- 本機座標空間
- VML 圖形，區域座標空間
- Vector Markup Language (VML) 、群組圖形
- VML (Vector Markup Language) 、群組圖案
- 向量圖形，群組圖形
- VML 圖形，群組
- 將圖形分組
- Vector Markup Language (VML) 、縮放圖形
- VML (Vector Markup Language) 、縮放形狀
- 向量圖形，縮放形狀
- VML 圖形，縮放比例
- 調整形狀
- Vector Markup Language (VML) ，調整大小圖形
- VML (Vector Markup Language) ，調整大小圖形
- 向量圖形，調整大小圖形
- VML 圖形，調整大小
- 調整大小圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682966"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="317db-125">使用本機座標空間</span><span class="sxs-lookup"><span data-stu-id="317db-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="317db-126">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="317db-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="317db-127">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="317db-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="317db-128">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="317db-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="317db-129">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="317db-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="317db-130">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="317db-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="317db-131">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="317db-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="317db-132">如您所學到的，您可以指定 **寬度** 和 **高度** 樣式屬性，來定義要在其中呈現圖形或群組內容之包含方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="317db-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="317db-133">在本主題中，我們將說明什麼是本機座標空間，以及如何在 VML 中使用它來調整圖形。</span><span class="sxs-lookup"><span data-stu-id="317db-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="317db-134">如果系統要求您在一段方格紙上繪製一部以二英寸為二的矩形，您要找的第一件事就是開始 (起始點) 的位置。</span><span class="sxs-lookup"><span data-stu-id="317db-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="317db-135">然後，您會找出如何將一英寸對應至方格紙的儲存格， (座標) 。</span><span class="sxs-lookup"><span data-stu-id="317db-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="317db-136">同樣地，當圖形或群組的內容呈現在網頁的包含方塊內部時，必須定義起始點和座標。</span><span class="sxs-lookup"><span data-stu-id="317db-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="317db-137">VML 提供本機座標空間，以允許每個圖形或群組定義自己的起點和座標。</span><span class="sxs-lookup"><span data-stu-id="317db-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="317db-138">如果您未指定座標空間，將會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="317db-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="317db-139">根據預設，來源會從內含方塊的左上角開始。</span><span class="sxs-lookup"><span data-stu-id="317db-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="317db-140">例如，如下所示紅色橢圓形的 VML 標記法不會指定 **coordsize** 和 **coordorigin** 屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="317db-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="317db-141">因此，會使用預設的本機座標空間。</span><span class="sxs-lookup"><span data-stu-id="317db-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="317db-142">Oval 的大小為100點 (寬度) 75 點 (高度) 。</span><span class="sxs-lookup"><span data-stu-id="317db-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="317db-143">您可以指定不同的寬度或高度來調整橢圓大小，如您在 [尺規圖形](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) 主題中所學到的一樣。</span><span class="sxs-lookup"><span data-stu-id="317db-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 個位元組) ](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="317db-145">當圖形變得更複雜時，或當您想要將數個圖案組合在一起時，您應該使用 VML 中提供的本機座標空間功能。</span><span class="sxs-lookup"><span data-stu-id="317db-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="317db-146">針對每個圖形或群組，您可以使用 **coordsize** 和 **coordorigin** 屬性屬性來定義圖形或群組的本機座標空間。</span><span class="sxs-lookup"><span data-stu-id="317db-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="317db-147">**Coordsize** 屬性會指定寬度的單位數目，以及包含方塊的高度。</span><span class="sxs-lookup"><span data-stu-id="317db-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="317db-148">**Coordorigin** 屬性會定義包含方塊左上角的座標。</span><span class="sxs-lookup"><span data-stu-id="317db-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="317db-149">所有位置相關資訊 (例如寬度、高度、左方、頂端、路徑等 ) 都會以本機座標空間中的單位表示。</span><span class="sxs-lookup"><span data-stu-id="317db-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="317db-150">例如，如下列 VML 標記法所示， `width: 100pt; height: 100pt;` 會將圖形的包含方塊大小定義為100點乘以100點。</span><span class="sxs-lookup"><span data-stu-id="317db-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 個位元組) ](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="317db-152">`coordsize="21600,21600"` 將圖形的本機座標空間大小定義為21600單位（依21600單位）。</span><span class="sxs-lookup"><span data-stu-id="317db-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="317db-153">因此，本機座標空間中的一個單位相當於1/216 點。</span><span class="sxs-lookup"><span data-stu-id="317db-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="317db-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` 將圖形的外框定義為菱形形狀。</span><span class="sxs-lookup"><span data-stu-id="317db-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="317db-155">如我們所學到的，所有位置相關資訊 (例如寬度、高度、左方、頂端、路徑等 ) 都會以本機座標空間中的單位表示。</span><span class="sxs-lookup"><span data-stu-id="317db-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="317db-156">因此，中的 10800 `<path>` 表示10800單位，這相當於50點。</span><span class="sxs-lookup"><span data-stu-id="317db-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="317db-157">當您想要調整此鑽石形狀的大小時，只要指定不同的寬度或高度即可，您不需要變更中的任何值 `<path>` 。</span><span class="sxs-lookup"><span data-stu-id="317db-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="317db-158">針對這個複雜的圖形，如果您未使用本機座標空間功能，則 `<path>` 每當您想要調整其大小時，都必須變更中的每個值。</span><span class="sxs-lookup"><span data-stu-id="317db-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="317db-159">例如，您可以只指定不同的寬度或高度來調整鑽石圖形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="317db-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 個位元組) ](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="317db-161">您也可以在專案中使用區域座標空間， `<group>` 讓群組中的所有圖形內容都能根據相同的座標進行調整。</span><span class="sxs-lookup"><span data-stu-id="317db-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="317db-162">然後，每當您想要調整或移動一組圖形時，只要變更群組的寬度和高度，或 **coordsize** 和 **coordorigin** 設定。</span><span class="sxs-lookup"><span data-stu-id="317db-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="317db-163">例如，在下列 VML 表示中， `<v:group style='... width:200pt;height:200pt;'>` 會將群組的大小定義為200點乘以200點。</span><span class="sxs-lookup"><span data-stu-id="317db-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 個位元組) ](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="317db-165">`coordsize="1000,1000"` 定義群組的本機座標空間大小，以1000單位乘以1000單位。</span><span class="sxs-lookup"><span data-stu-id="317db-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="317db-166">因此，本機座標空間中的1個單位相當於1/5 點。</span><span class="sxs-lookup"><span data-stu-id="317db-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="317db-167">`coordorigin="-500,-500"` 將內含方塊的左上角定義為 "-500，-500"。</span><span class="sxs-lookup"><span data-stu-id="317db-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="317db-168">因此，在包含方塊內的座標系統範圍是從-500 到500，沿著 X 軸，以及-500 到 y 軸的500。</span><span class="sxs-lookup"><span data-stu-id="317db-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="317db-169">換句話說，內含方塊的中心是「0，0」。</span><span class="sxs-lookup"><span data-stu-id="317db-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="317db-170">`<v:oval style='... width:400;height:300;'>` 將紅色橢圓的包含方塊大小定義為400單位 (寬度) 300 單位 (高度) 。</span><span class="sxs-lookup"><span data-stu-id="317db-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="317db-171">因為區域座標空間中的一個單位相當於1/5 點，所以紅色橢圓形的包含方塊大小是80點 (寬度) 由60點 (高度) 。</span><span class="sxs-lookup"><span data-stu-id="317db-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="317db-172">同樣地，綠色 roundrect 的內含方塊大小為50點 (寬度) 40 點 (高度) 。</span><span class="sxs-lookup"><span data-stu-id="317db-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="317db-173">當您想要調整紅色橢圓和綠色 roundrect 的大小時，只要變更 `<v:group style='... width:200pt;height:200pt;'>` 。</span><span class="sxs-lookup"><span data-stu-id="317db-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="317db-174">這就是-您不需要個別變更兩個圖形的大小。</span><span class="sxs-lookup"><span data-stu-id="317db-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="317db-175">例如，如果您變更 `<v:group style='... width:200pt;height:200pt;'>` 為 `<v:group style='... width:300pt;height:300pt;'>` ，圖形會變得更大，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="317db-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 個位元組) ](images/cord4.gif)



<span data-ttu-id="317db-177">您也會注意到圖形的位置不同。</span><span class="sxs-lookup"><span data-stu-id="317db-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="317db-178">這是因為圖形是從位於內含方塊中央的 "0，0" 繪製。</span><span class="sxs-lookup"><span data-stu-id="317db-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="317db-179">因為您將 [包含] 方塊放大，所以包含的方塊中央也會移動。</span><span class="sxs-lookup"><span data-stu-id="317db-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="317db-180">如果您變更 `coordorigin="-500,-500"` 為 `coordorigin="0,0"` （如下圖所示），您會注意到紅色橢圓和綠色 roundrect 都會向上移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="317db-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="317db-181">這是因為 "0，0" 現在會在內含方塊的左上角找到。</span><span class="sxs-lookup"><span data-stu-id="317db-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 個位元組) ](images/cord5.gif)



<span data-ttu-id="317db-183">也請務必注意，[包含] 方塊不會建立裁剪區域。</span><span class="sxs-lookup"><span data-stu-id="317db-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="317db-184">圖形可能會在內含方塊的界限之外繪製。</span><span class="sxs-lookup"><span data-stu-id="317db-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="317db-185">[包含] 方塊只是用來將本機座標空間對應到頁面空間。</span><span class="sxs-lookup"><span data-stu-id="317db-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="317db-186">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858382) 。</span><span class="sxs-lookup"><span data-stu-id="317db-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 