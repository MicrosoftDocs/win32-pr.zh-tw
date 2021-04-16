---
title: 使用 Fill 元素
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- 網路研討會，填滿元素
- 設計網頁，填滿元素
- Vector Markup Language (VML) 、fill 元素
- VML (Vector Markup Language) ，fill 元素
- 向量圖形、填滿元素
- fill 元素
- VML 元素，填滿
- VML 圖形，填滿元素
- Vector Markup Language (VML) 、漸層填滿
- VML (Vector Markup Language) 、漸層填滿
- 向量圖形，漸層填滿
- VML 圖形，漸層填滿
- 漸層填滿形狀
- Vector Markup Language (VML) 、模式填滿
- VML (Vector Markup Language) ，模式填滿
- 向量圖形，模式填滿
- VML 圖形，模式填滿
- 模式填滿圖形
- Vector Markup Language (VML) 、圖片填滿
- VML (Vector Markup Language) ，圖片填滿
- 向量圖形，圖片填滿
- VML 圖形，圖片填滿
- 圖片填滿的形狀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104568419"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="7b829-127">使用 Fill 元素</span><span class="sxs-lookup"><span data-stu-id="7b829-127">Using the Fill Element</span></span>

<span data-ttu-id="7b829-128">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7b829-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7b829-129">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7b829-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7b829-130">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7b829-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7b829-131">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7b829-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7b829-132">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7b829-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7b829-133">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7b829-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7b829-134">如您所學到的，您可以使用預先定義之圖形元素的 **fillcolor** 屬性屬性（例如，、、、、、 `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` --）來指定用來填滿圖形的色彩。</span><span class="sxs-lookup"><span data-stu-id="7b829-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="7b829-135">在本主題中，我們將說明如何繪製填滿更先進效果的圖形。</span><span class="sxs-lookup"><span data-stu-id="7b829-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="7b829-136">您可以將子專案放在 `<fill>` `<shape>` 、或或 `<shapetype>` 任何預先定義的 shape 元素內，以描述如何填滿圖形。</span><span class="sxs-lookup"><span data-stu-id="7b829-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="7b829-137">然後，您可以使用子項目的屬性屬性 `<fill>` 來自訂填滿效果，例如漸層 [填滿](#gradient-fill)、 [圖樣填滿](#pattern-fill)、 [圖片填滿](#picture-fill)。</span><span class="sxs-lookup"><span data-stu-id="7b829-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="7b829-138">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="7b829-138">In this topic:</span></span>

-   [<span data-ttu-id="7b829-139">漸層填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="7b829-140">模式填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="7b829-141">圖片填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="7b829-142">漸層填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-142">Gradient Fill</span></span>

<span data-ttu-id="7b829-143">若要繪製漸層填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "漸層" 或 "gradientRadial"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **method**、 **color2**、 **focus** 和 **angle**。</span><span class="sxs-lookup"><span data-stu-id="7b829-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="7b829-144">**範例：**</span><span class="sxs-lookup"><span data-stu-id="7b829-144">**Examples:**</span></span>

<span data-ttu-id="7b829-145">若要建立水準漸層填滿的形狀，您可以將 **type** 屬性屬性（property）設定為「漸層」（property），如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 個位元組) ](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="7b829-147">如果您變更圖形的 **fillcolor** 屬性屬性，圖形就會以不同的色彩填滿。</span><span class="sxs-lookup"><span data-stu-id="7b829-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="7b829-148">您可以指定子項目的 **color2** 屬性屬性，以新增第二個色彩 `<fill>` 。</span><span class="sxs-lookup"><span data-stu-id="7b829-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="7b829-149">例如，若要建立以兩種色彩填滿的形狀，您可以指定子項目的 **color2** 屬性屬性來加入第二個色彩 `<fill>` ，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 個位元組) ](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="7b829-151">您可以將 **method** 屬性屬性（property）設定為 "線性" 或 "sigma" 或 "any" 或 "none"。</span><span class="sxs-lookup"><span data-stu-id="7b829-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="7b829-152">漸層的效果稍微不同。</span><span class="sxs-lookup"><span data-stu-id="7b829-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="7b829-153">此外，您也可以使用 **angle**、**focus**、**focussize** 或 **focusposition** 屬性屬性來變更漸層的效果。</span><span class="sxs-lookup"><span data-stu-id="7b829-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="7b829-154">**範例：**</span><span class="sxs-lookup"><span data-stu-id="7b829-154">**Examples:**</span></span>

 

<span data-ttu-id="7b829-155">若要建立垂直填滿漸層的圖形，您可以將 angle 屬性屬性設定為 angle = "-90"，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 個位元組) ](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="7b829-157">若要建立從對角移動的漸層填滿的形狀，您可以將 **angle** 屬性屬性設定為 angle = "-135"，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 個位元組) ](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="7b829-159">若要建立從對角線移動漸層填滿的圖形，您可以將 **angle** 屬性屬性設定為 angle = "-45"，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 個位元組) ](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="7b829-161">若要建立從中央填滿漸層的圖形，您可以指定 `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` ，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 個位元組) ](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="7b829-163">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="7b829-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="7b829-164">模式填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-164">Pattern Fill</span></span>

<span data-ttu-id="7b829-165">若要繪製模式填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "pattern"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **src** 和 **color2**。</span><span class="sxs-lookup"><span data-stu-id="7b829-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="7b829-166">**範例：**</span><span class="sxs-lookup"><span data-stu-id="7b829-166">**Examples:**</span></span>

<span data-ttu-id="7b829-167">若要建立填滿模式影像的圖形，您可以將 **type** 屬性屬性指定為 "pattern"，然後將 **src** 屬性屬性指向模式影像檔案的位置，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 個位元組) ](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="7b829-169">如果您將 **src** 屬性屬性指向不同的模式檔案，您可以建立以不同模式填滿的圖形。</span><span class="sxs-lookup"><span data-stu-id="7b829-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="7b829-170">此外，您可以為 **fillcolor** 或 **color2** 屬性屬性指定不同的值，以變更色彩，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 個位元組) ](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="7b829-172">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="7b829-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="7b829-173">圖片填滿</span><span class="sxs-lookup"><span data-stu-id="7b829-173">Picture Fill</span></span>

<span data-ttu-id="7b829-174">若要繪製圖片填滿圖形，您可以將子項目的 **type** 屬性屬性設定 `<fill>` 為 "frame"，然後指定子項目的其他屬性屬性 `<fill>` ，例如 **src** 和 **color2**。</span><span class="sxs-lookup"><span data-stu-id="7b829-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="7b829-175">**範例：**</span><span class="sxs-lookup"><span data-stu-id="7b829-175">**Examples:**</span></span>

<span data-ttu-id="7b829-176">若要建立填滿圖片檔案的圖形，您可以將 **type** 屬性屬性指定為「frame」，然後將 **src** 屬性屬性（attribute）指向圖片檔的位置，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="7b829-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 個位元組) ](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="7b829-178">您可以藉由將 **src** 屬性屬性指向另一個檔案，輕鬆地建立填滿不同圖片的圖形。</span><span class="sxs-lookup"><span data-stu-id="7b829-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="7b829-179">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858394) 。</span><span class="sxs-lookup"><span data-stu-id="7b829-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 