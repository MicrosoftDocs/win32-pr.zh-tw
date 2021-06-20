---
title: 使用預先定義的圖形
description: 本文說明如何在 VML 中使用預先定義的圖形，這項功能已在 Windows Internet Explorer 9 淘汰。
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- 網路研討會，預先定義的圖形
- 設計網頁、預先定義的圖形
- Vector Markup Language (VML) 、預先定義的圖形
- VML (Vector Markup Language) 、預先定義的圖形
- 向量圖形，預先定義的圖形
- 已預先定義的 VML 圖形
- 預先定義的圖形
- Vector Markup Language (VML) 、rect 元素
- VML (Vector Markup Language) ，rect 元素
- 向量圖形、rect 元素
- rect 元素
- VML 元素、rect
- Vector Markup Language (VML) 、roundrect 元素
- VML (Vector Markup Language) ，roundrect 元素
- 向量圖形，roundrect 元素
- roundrect 元素
- VML 元素，roundrect
- Vector Markup Language (VML) ，line 元素
- VML (Vector Markup Language) ，line 元素
- 向量圖形、線條元素
- line 元素
- VML 元素，行
- Vector Markup Language (VML) 、聚合線條元素
- VML (Vector Markup Language) 、聚合線條元素
- 向量圖形、折線元素
- 聚合線條元素
- VML 元素，折線
- Vector Markup Language (VML) 、曲線元素
- VML (Vector Markup Language) ，曲線元素
- 向量圖形、曲線元素
- 曲線元素
- VML 元素、曲線
- Vector Markup Language (VML) 、arc 元素
- VML (Vector Markup Language) ，arc 元素
- 向量圖形、弧線元素
- 弧線元素
- VML 元素、弧線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407681"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="bb37d-140">使用預先定義的圖形</span><span class="sxs-lookup"><span data-stu-id="bb37d-140">Using Predefined Shapes</span></span>

<span data-ttu-id="bb37d-141">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bb37d-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bb37d-142">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bb37d-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bb37d-143">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bb37d-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bb37d-144">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bb37d-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bb37d-145">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bb37d-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bb37d-146">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bb37d-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bb37d-147">如您所學到的，您可以使用 `<oval>` VML 的元素來建立簡單的橢圓形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="bb37d-148">VML 提供數個其他預先定義的元素。</span><span class="sxs-lookup"><span data-stu-id="bb37d-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="bb37d-149">在本主題中，我們將說明如何使用這些元素繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="bb37d-150">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="bb37d-150">In this topic:</span></span>

-   [<span data-ttu-id="bb37d-151">矩形</span><span class="sxs-lookup"><span data-stu-id="bb37d-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="bb37d-152">roundrect</span><span class="sxs-lookup"><span data-stu-id="bb37d-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="bb37d-153">line</span><span class="sxs-lookup"><span data-stu-id="bb37d-153">line</span></span>](#polyline)
-   [<span data-ttu-id="bb37d-154">折線</span><span class="sxs-lookup"><span data-stu-id="bb37d-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="bb37d-155">曲線</span><span class="sxs-lookup"><span data-stu-id="bb37d-155">curve</span></span>](#curve)
-   [<span data-ttu-id="bb37d-156">弧</span><span class="sxs-lookup"><span data-stu-id="bb37d-156">arc</span></span>](#arc)
-   [<span data-ttu-id="bb37d-157">總結</span><span class="sxs-lookup"><span data-stu-id="bb37d-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="bb37d-158">rect</span><span class="sxs-lookup"><span data-stu-id="bb37d-158">rect</span></span>

<span data-ttu-id="bb37d-159">您可以使用 `<rect>` 元素來繪製矩形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="bb37d-160">然後您可以藉由指定不同的屬性屬性來自訂矩形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="bb37d-161">例如，您可以藉由指定 **fillcolor**= "blue" 來繪製以藍色填滿的矩形，並指定 **strokecolor**= "red" **strokeweight**= "3.5 pt" 來提供其3.5 點紅色外框，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="bb37d-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 個位元組) ](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="bb37d-163">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="bb37d-164"> (附注： VML 規格沒有元素的書簽 `<rect>` 。 ) </span><span class="sxs-lookup"><span data-stu-id="bb37d-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="bb37d-165">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="bb37d-166">roundrect</span><span class="sxs-lookup"><span data-stu-id="bb37d-166">roundrect</span></span>

<span data-ttu-id="bb37d-167">您可以使用 `<roundrect>` 元素來繪製具有圓角的矩形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="bb37d-168">然後，您可以藉由指定不同的屬性屬性來自訂圓角矩形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="bb37d-169">例如，您可以藉由指定 **arcsize**= "0.3"、指定 **fillcolor**= "黃"，以黃色填滿矩形，然後指定 **strokecolor**= "red" **strokeweight**= "2pt"，為它提供雙點紅色外框，如下列 VML 標記法所示，繪製具有圓角的矩形：</span><span class="sxs-lookup"><span data-stu-id="bb37d-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 個位元組) ](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="bb37d-171">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="bb37d-172">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="bb37d-173">line</span><span class="sxs-lookup"><span data-stu-id="bb37d-173">line</span></span>

<span data-ttu-id="bb37d-174">您可以使用 `<line>` 元素來建立直線。</span><span class="sxs-lookup"><span data-stu-id="bb37d-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="bb37d-175">然後您可以藉由指定不同的屬性屬性來自訂這一行。</span><span class="sxs-lookup"><span data-stu-id="bb37d-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="bb37d-176">例如，您可以藉由指定 **from**= "20pt，20pt" to = "100pt，20pt" **來** 繪製水平線，然後藉由指定 **strokecolor**= "red" **strokeweight**= "2pt"，將其設為2點和紅色，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="bb37d-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 個位元組) ](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="bb37d-178">您可以只針對 **from** 和 **to** 屬性屬性指定不同的值，以繪製垂直或對角線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="bb37d-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 個位元組) ](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="bb37d-180">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="bb37d-181">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="bb37d-182">折線</span><span class="sxs-lookup"><span data-stu-id="bb37d-182">polyline</span></span>

<span data-ttu-id="bb37d-183">您可以使用 `<polyline>` 元素來定義從連接的線段建立的圖形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="bb37d-184">然後您可以藉由指定不同的屬性屬性來自訂圖形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="bb37d-185">例如，若要繪製下圖中顯示的圖形，您可以輸入下列 VML 標記法：</span><span class="sxs-lookup"><span data-stu-id="bb37d-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 個位元組) ](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="bb37d-187">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="bb37d-188">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="bb37d-189">曲線</span><span class="sxs-lookup"><span data-stu-id="bb37d-189">curve</span></span>

<span data-ttu-id="bb37d-190">您可以使用 `<curve>` 元素來繪製三次貝茲曲線。</span><span class="sxs-lookup"><span data-stu-id="bb37d-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="bb37d-191">然後您可以藉由指定不同的屬性屬性來自訂曲線。</span><span class="sxs-lookup"><span data-stu-id="bb37d-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="bb37d-192">例如，若要繪製如下圖所示的曲線，您可以輸入下列 VML 標記法：</span><span class="sxs-lookup"><span data-stu-id="bb37d-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 個位元組) ](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="bb37d-194">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="bb37d-195">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="bb37d-196">弧形</span><span class="sxs-lookup"><span data-stu-id="bb37d-196">arc</span></span>

<span data-ttu-id="bb37d-197">您可以使用專案 `<arc>` 來繪製定義為橢圓形區段的弧形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="bb37d-198">弧線是由 oval 的交集所定義，以及角度所指定的開始和結束半徑向量。</span><span class="sxs-lookup"><span data-stu-id="bb37d-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="bb37d-199">角度的計算方式是使用圓形的屬性， (寬度等於高度) ，然後將 anisotropically 調整為所需的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="bb37d-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="bb37d-200">例如，您可以藉由指定 **>startangle**= "0" **endangle**= "90"，繪製從0度開始並以90度結束的弧線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="bb37d-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 個位元組) ](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="bb37d-202">您可以藉由指定不同的 **>startangle** 和 **endangle** 值來變更弧線，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="bb37d-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 個位元組) ](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 個位元組) ](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="bb37d-205">如需此元素的詳細資訊，請參閱 [VML 規格](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) 。</span><span class="sxs-lookup"><span data-stu-id="bb37d-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="bb37d-206">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="bb37d-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="bb37d-207">總結</span><span class="sxs-lookup"><span data-stu-id="bb37d-207">Summary</span></span>

<span data-ttu-id="bb37d-208">您可以使用 VML 預先定義的專案（例如 `<oval>` 、 `<line>` 、 `<polyline>` 、 `<curve>` 、 `<rect>` 、和）， `<roundrect>` `<arc>` 輕鬆地在網頁上繪製圖形，然後藉由只變更屬性屬性來自訂這些圖形。</span><span class="sxs-lookup"><span data-stu-id="bb37d-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 