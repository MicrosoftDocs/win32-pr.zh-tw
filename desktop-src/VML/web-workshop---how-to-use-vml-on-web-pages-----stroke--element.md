---
title: 使用 Stroke 元素
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- 網路研討會，筆劃元素
- 設計網頁，筆劃元素
- Vector Markup Language (VML) ，stroke 元素
- VML (Vector Markup Language) ，筆劃元素
- 向量圖形，筆劃元素
- stroke 元素
- VML 元素，筆劃
- VML 圖形，筆劃元素
- Vector Markup Language (VML) ，dashstyle 屬性屬性
- VML (Vector Markup Language) ，dashstyle 屬性屬性
- 向量圖形，dashstyle 屬性屬性
- dashstyle 屬性屬性
- Vector Markup Language (VML) 、不透明度屬性屬性
- VML (Vector Markup Language) ，不透明度屬性屬性
- 向量圖形、不透明度屬性屬性
- 不透明度屬性屬性
- Vector Markup Language (VML) ，linestyle 屬性屬性
- VML (Vector Markup Language) ，linestyle 屬性屬性
- 向量圖形，linestyle 屬性屬性
- linestyle 屬性屬性
- Vector Markup Language (VML) ，joinstyle 屬性屬性
- VML (Vector Markup Language) ，joinstyle 屬性屬性
- 向量圖形，joinstyle 屬性屬性
- joinstyle 屬性屬性
- Vector Markup Language (VML) ，filltype 屬性屬性
- VML (Vector Markup Language) ，filltype 屬性屬性
- 向量圖形，filltype 屬性屬性
- filltype 屬性屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316354"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="26158-132">使用 Stroke 元素</span><span class="sxs-lookup"><span data-stu-id="26158-132">Using the Stroke Element</span></span>

<span data-ttu-id="26158-133">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="26158-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="26158-134">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="26158-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="26158-135">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="26158-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="26158-136">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="26158-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="26158-137">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="26158-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="26158-138">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="26158-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="26158-139">使用 `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="26158-139">Using `<stroke>`</span></span>

<span data-ttu-id="26158-140">如您所學到的，您可以使用預先定義之圖形的 **strokecolor** 和 **strokeweight** 屬性屬性（例如，、、、、、 `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` --）來指定形狀輪廓的色彩和粗細。</span><span class="sxs-lookup"><span data-stu-id="26158-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="26158-141">在本主題中，我們將說明如何繪製具有更先進大綱的圖形。</span><span class="sxs-lookup"><span data-stu-id="26158-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="26158-142">您可以將子專案放在 `<stroke>` `<shape>` 、或或 `<shapetype>` 任何預先定義的 shape 元素內，以描述如何繪製圖案的外框。</span><span class="sxs-lookup"><span data-stu-id="26158-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="26158-143">然後，您可以使用子項目的屬性屬性（例如 [dashstyle](#dashstyle)、 [不透明度](#opacity)、 [linestyle](#linestyle)、 [joinstyle](#joinstyle)、 [filltype](#filltype) ） `<stroke>` 來自訂大綱。</span><span class="sxs-lookup"><span data-stu-id="26158-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="26158-144">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="26158-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="26158-145">dashstyle</span><span class="sxs-lookup"><span data-stu-id="26158-145">dashstyle</span></span>

<span data-ttu-id="26158-146">您可以使用子專案的 **dashstyle** 屬性屬性 `<stroke>` ，以各種虛線樣式來繪製大綱。</span><span class="sxs-lookup"><span data-stu-id="26158-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="26158-147">**範例：**</span><span class="sxs-lookup"><span data-stu-id="26158-147">**Examples:**</span></span>

<span data-ttu-id="26158-148">如果您在 `<v:stroke dashstyle="solid" />` 元素內指定 `<line>` ，您可以建立實線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 個位元組) ](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="26158-150">如果您將 **dashstyle** 屬性屬性變更為「點」，就可以建立虛線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 個位元組) ](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="26158-152">如果您將 **dashstyle** 屬性屬性變更為 "虛線"，就可以建立虛線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 個位元組) ](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="26158-154">如果您將 **dashstyle** 屬性屬性變更為 "點"，就可以建立具有虛線和虛線樣式的線條，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 個位元組) ](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="26158-156">如果您將 **dashstyle** 屬性屬性變更為 "longdash"，就可以建立具有長虛線樣式的行，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 個位元組) ](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="26158-158">如果您將 **dashstyle** 屬性屬性變更為 "longdashdot"，則可以使用長虛線和虛線樣式來建立一行，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 個位元組) ](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="26158-160">如果您在專案 `<v:stroke dashstyle="dashdot" />` 內放置 `<rect>` ，您可以建立具有虛線和點外框的矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 個位元組) ](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="26158-162">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="26158-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="26158-163">不透明度</span><span class="sxs-lookup"><span data-stu-id="26158-163">opacity</span></span>

<span data-ttu-id="26158-164">您可以使用子項目的 **不透明度** 屬性屬性 `<stroke>` ，以不同的不透明度樣式來繪製外框。</span><span class="sxs-lookup"><span data-stu-id="26158-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="26158-165">**不透明度** 屬性屬性的值可以是介於0到1之間的任何數位。</span><span class="sxs-lookup"><span data-stu-id="26158-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="26158-166">依預設，它是1，表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="26158-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="26158-167">**範例：**</span><span class="sxs-lookup"><span data-stu-id="26158-167">**Examples:**</span></span>

<span data-ttu-id="26158-168">下列 VML 表示會建立具有完整不透明度的行：</span><span class="sxs-lookup"><span data-stu-id="26158-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 個位元組) ](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="26158-170">如果您在專案 `<v:stroke opacity="0.5" />` 內加入 `<line>` ，您可以建立具有50% 不透明度的行，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 個位元組) ](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="26158-172">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="26158-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="26158-173">linestyle</span><span class="sxs-lookup"><span data-stu-id="26158-173">linestyle</span></span>

<span data-ttu-id="26158-174">您可以使用子項目的 **linestyle** 屬性屬性 `<stroke>` ，以各種線條樣式來繪製外框。</span><span class="sxs-lookup"><span data-stu-id="26158-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="26158-175">**範例：**</span><span class="sxs-lookup"><span data-stu-id="26158-175">**Examples:**</span></span>

<span data-ttu-id="26158-176">如果您在 `<v:stroke linestyle="single" />` 元素內指定 `<rect>` ，您可以使用單一大綱建立矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 個位元組) ](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="26158-178">如果您將 **linestyle** 屬性屬性變更為 "thinthin"，則可以使用 (1:1:1) 的大綱建立矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 個位元組) ](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="26158-180">如果您將 **linestyle** 屬性屬性變更為 "thinthick"，則可以使用 (1:1:2) 的大綱建立矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 個位元組) ](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="26158-182">如果您將 **linestyle** 屬性屬性變更為 "thickthin"，則可以使用 (2:1:1) 的大綱建立矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 個位元組) ](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="26158-184">如果您將 **linestyle** 屬性屬性變更為 "thickbetweenthin"，則可以使用 (1:1:2:1:1) 的大綱建立矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 個位元組) ](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="26158-186">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="26158-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="26158-187">joinstyle</span><span class="sxs-lookup"><span data-stu-id="26158-187">joinstyle</span></span>

<span data-ttu-id="26158-188">您可以使用子專案的 **joinstyle** 屬性 `<stroke>` ，來定義如何將線條聯結在一起。</span><span class="sxs-lookup"><span data-stu-id="26158-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="26158-189">例如，若要建立具有圓形聯結大綱的圖形（如下圖所示），您可以在專案中指定 `<v:stroke joinstyle="round" />` `<polyline>` ，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 個位元組) ](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="26158-191">如果您將 **joinstyle** 屬性屬性變更為「斜面」，則可以建立具有斜面聯結大綱的圖形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 個位元組) ](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="26158-193">如果您將 **joinstyle** 屬性屬性變更為「斜接角」，則可以建立具有「斜接聯結」大綱的圖形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 個位元組) ](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="26158-195">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="26158-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="26158-196">filltype</span><span class="sxs-lookup"><span data-stu-id="26158-196">filltype</span></span>

<span data-ttu-id="26158-197">您可以使用子項目的 **filltype** 屬性屬性 `<stroke>` 來繪製具有各種填滿效果的大綱。</span><span class="sxs-lookup"><span data-stu-id="26158-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="26158-198">**範例：**</span><span class="sxs-lookup"><span data-stu-id="26158-198">**Examples:**</span></span>

<span data-ttu-id="26158-199">如果您在專案 `<v:stroke filltype="solid" />` 內指定 `<roundrect>` ，您可以使用實心填滿輪廓來建立圓角矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 個位元組) ](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="26158-201">如果您將 **filltype** 屬性屬性變更為 "pattern"，請將 **src** 屬性屬性指向模式影像檔案的位置，並將 [ **color2** 屬性] 屬性設定為第二個模式色彩，您可以建立具有模式外框的圓角矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 個位元組) ](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="26158-203">如果您將 [ **filltype** 屬性] 屬性變更為 [磚]，並將 **src** 屬性屬性指向影像檔的位置，您就可以建立具有並排顯示的圓角矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 個位元組) ](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="26158-205">如果您將 [ **filltype** 屬性] 屬性變更為 [frame]，並將 **src** 屬性屬性指向影像檔的位置，則可以使用圖片大綱來建立圓角矩形，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="26158-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 個位元組) ](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="26158-207">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858395) 。</span><span class="sxs-lookup"><span data-stu-id="26158-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 