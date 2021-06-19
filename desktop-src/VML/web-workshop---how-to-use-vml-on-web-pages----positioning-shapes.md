---
title: 定點陣圖形
description: 本文描述如何在 VML 中定點陣圖形，這是 Windows Internet Explorer 9 淘汰的功能。
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- 網路研討會，定點陣圖形
- 設計網頁，定點陣圖形
- Vector Markup Language (VML) ，定點陣圖形
- VML (Vector Markup Language) ，定點陣圖形
- 向量圖形，定點陣圖形
- VML 圖形，定位
- 定點陣圖形
- Vector Markup Language (VML) 、靜態位置樣式
- VML (Vector Markup Language) 、靜態位置樣式
- 向量圖形，靜態位置樣式
- 靜態位置樣式
- Vector Markup Language (VML) 、相對位置樣式
- VML (Vector Markup Language) 、相對位置樣式
- 向量圖形、相對位置樣式
- 相對位置樣式
- Vector Markup Language (VML) 、絕對位置樣式
- VML (Vector Markup Language) ，絕對位置樣式
- 向量圖形，絕對位置樣式
- 絕對位置樣式
- Vector Markup Language (VML) ，z 索引位置樣式
- VML (Vector Markup Language) ，z 索引位置樣式
- 向量圖形，z-索引位置樣式
- z-索引位置樣式
- Vector Markup Language (VML) 、旋轉位置樣式
- VML (Vector Markup Language) ，旋轉位置樣式
- 向量圖形，旋轉位置樣式
- 旋轉位置樣式
- Vector Markup Language (VML) 、翻轉位置樣式
- VML (Vector Markup Language) 、翻轉位置樣式
- 向量圖形，翻轉位置樣式
- 翻轉位置樣式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407711"
---
# <a name="positioning-shapes"></a><span data-ttu-id="45afa-134">定點陣圖形</span><span class="sxs-lookup"><span data-stu-id="45afa-134">Positioning Shapes</span></span>

<span data-ttu-id="45afa-135">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="45afa-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="45afa-136">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="45afa-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="45afa-137">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="45afa-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="45afa-138">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="45afa-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="45afa-139">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="45afa-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="45afa-140">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="45afa-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="45afa-141">您已瞭解如何使用 VML 在網頁上繪製和上色圖形。</span><span class="sxs-lookup"><span data-stu-id="45afa-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="45afa-142">在本主題中，您將使用 VML 在網頁上精確地放置圖形。</span><span class="sxs-lookup"><span data-stu-id="45afa-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="45afa-143">VML 使用方塊[模型](https://www.w3.org/TR/PR-CSS2/box.mdl)中所定義的相同語法和以[CSS2](https://www.w3.org/TR/PR-CSS2/) [呈現的視覺呈現模型](https://www.w3.org/TR/PR-CSS2/visuren.mdl)區段，來將圖形放在網頁上。</span><span class="sxs-lookup"><span data-stu-id="45afa-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="45afa-144">您可以使用 [ [靜態](#static)]、[ [相對](#relative)] 或 [ [絕對](#absolute) ] 來判斷基底點在網頁上的所在位置。</span><span class="sxs-lookup"><span data-stu-id="45afa-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="45afa-145">然後，您可以使用 [ **上** ] 和 [ **左方** ] 樣式屬性來指定基底點的位移，該基底點會放置圖形的包含方塊。</span><span class="sxs-lookup"><span data-stu-id="45afa-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="45afa-146">您也可以使用 [z 索引](#z-index) 來指定網頁上圖形的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="45afa-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="45afa-147">此外，VML 還提供旋轉和[翻轉](#flip)[來旋轉或](#rotation)翻轉圖形。</span><span class="sxs-lookup"><span data-stu-id="45afa-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="45afa-148">本主題內容：</span><span class="sxs-lookup"><span data-stu-id="45afa-148">In this topic:</span></span>

-   [<span data-ttu-id="45afa-149">static</span><span class="sxs-lookup"><span data-stu-id="45afa-149">static</span></span>](#static)
-   [<span data-ttu-id="45afa-150">relative</span><span class="sxs-lookup"><span data-stu-id="45afa-150">relative</span></span>](#relative)
-   [<span data-ttu-id="45afa-151">absolute</span><span class="sxs-lookup"><span data-stu-id="45afa-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="45afa-152">z-索引</span><span class="sxs-lookup"><span data-stu-id="45afa-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="45afa-153">旋轉</span><span class="sxs-lookup"><span data-stu-id="45afa-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="45afa-154">flip</span><span class="sxs-lookup"><span data-stu-id="45afa-154">flip</span></span>](#flip)
-   [<span data-ttu-id="45afa-155">總結</span><span class="sxs-lookup"><span data-stu-id="45afa-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="45afa-156">static</span><span class="sxs-lookup"><span data-stu-id="45afa-156">static</span></span>

<span data-ttu-id="45afa-157">預設位置樣式是靜態的，它會指示瀏覽器將圖形放置在文字流程中 (基礎點) 的目前點，並忽略 **top** 和 **left** 樣式屬性中的設定。</span><span class="sxs-lookup"><span data-stu-id="45afa-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="45afa-158">例如，在下列的 VML 標記法中，紅色橢圓形會緊接在「圖形開頭：」的文字後面，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="45afa-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![shape1 \-ps.gif (2123 個位元組) ](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="45afa-160">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="45afa-161">relative</span><span class="sxs-lookup"><span data-stu-id="45afa-161">relative</span></span>

<span data-ttu-id="45afa-162">將 [位置樣式] 屬性設定為 [相對]，可讓您將包含的方塊與目前點之間的位移放 (文字流程中的基底點) 。</span><span class="sxs-lookup"><span data-stu-id="45afa-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="45afa-163">位移是由 **top** 和 **left** 樣式屬性中的設定所決定。</span><span class="sxs-lookup"><span data-stu-id="45afa-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="45afa-164">請注意，定位為相對的內含方塊會佔用文字流程中的空間。</span><span class="sxs-lookup"><span data-stu-id="45afa-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="45afa-165">例如，在下列的 VML 標記法中，紅色橢圓的位置是從左邊開始的20點，以及從頂端相對於文字流程中目前點的10點，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="45afa-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 個位元組) ](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="45afa-167">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="45afa-168">絕對</span><span class="sxs-lookup"><span data-stu-id="45afa-168">absolute</span></span>

<span data-ttu-id="45afa-169">將 [位置樣式] 屬性設定為 [絕對]，可讓您將包含的方塊放置於左上角， (其父元素的基底點) ， (包含) 圖形的定位元素。</span><span class="sxs-lookup"><span data-stu-id="45afa-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="45afa-170">請注意，定位為絕對的包含方塊並不會佔用文字流程的空間。</span><span class="sxs-lookup"><span data-stu-id="45afa-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="45afa-171">例如，在下列 VML 標記法中，紅色的橢圓會包含在 `<body>` 整個) 網頁 (的元素內，因此，基底點位於網頁的左上角。</span><span class="sxs-lookup"><span data-stu-id="45afa-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="45afa-172">Oval 的 [包含] 方塊是放置在從左上角到左上角（相對於網頁左上角）的最左邊20個點，如下圖所示：</span><span class="sxs-lookup"><span data-stu-id="45afa-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 個位元組) ](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="45afa-174">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="45afa-175">圖層索引</span><span class="sxs-lookup"><span data-stu-id="45afa-175">z-index</span></span>

<span data-ttu-id="45afa-176">您可以定位與另一個圖形重迭的圖形。</span><span class="sxs-lookup"><span data-stu-id="45afa-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="45afa-177">一般來說，HTML 程式碼中最後列出的圖形會顯示在最上方。</span><span class="sxs-lookup"><span data-stu-id="45afa-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="45afa-178">在 VML 中，您可以使用 **z 索引** 樣式屬性來控制迭置順序。</span><span class="sxs-lookup"><span data-stu-id="45afa-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="45afa-179">這個屬性的值可以是零、正整數或負整數。</span><span class="sxs-lookup"><span data-stu-id="45afa-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="45afa-180">具有較大 z 索引值的圖形會顯示在具有較小 z 索引值的圖形上方。</span><span class="sxs-lookup"><span data-stu-id="45afa-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="45afa-181">當兩個圖形都有相同的 Z 軸索引值時，HTML 程式碼中最後列出的圖形會出現在頂端。</span><span class="sxs-lookup"><span data-stu-id="45afa-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="45afa-182">例如，在下列 VML 標記法中，紅色橢圓形會顯示在藍色矩形的上方。</span><span class="sxs-lookup"><span data-stu-id="45afa-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="45afa-183">這是因為紅色橢圓形的 z-索引值大於藍色矩形的 z-索引值。</span><span class="sxs-lookup"><span data-stu-id="45afa-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 個位元組) ](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="45afa-185">如果您變更 z 索引（如下列 VML 標記法所示），紅色橢圓將會移到藍色矩形後方。</span><span class="sxs-lookup"><span data-stu-id="45afa-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 個位元組) ](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="45afa-187">如果您提供負整數，則可以使用 z 索引將圖形放置在一般文字流程後方，如下列 VML 標記法所示。</span><span class="sxs-lookup"><span data-stu-id="45afa-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 個位元組) ](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="45afa-189">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="45afa-190">旋轉</span><span class="sxs-lookup"><span data-stu-id="45afa-190">rotation</span></span>

<span data-ttu-id="45afa-191">您可以使用 [ **旋轉** 樣式] 屬性來指定要讓圖形開啟其軸的度數。</span><span class="sxs-lookup"><span data-stu-id="45afa-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="45afa-192">正值表示順時針旋轉;負數值表示逆時針旋轉。</span><span class="sxs-lookup"><span data-stu-id="45afa-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="45afa-193">例如，如果您指定 **style**= ' .。。旋轉： 90 '，您可以順時針旋轉形狀90度。</span><span class="sxs-lookup"><span data-stu-id="45afa-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="45afa-194">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="45afa-195">flip</span><span class="sxs-lookup"><span data-stu-id="45afa-195">flip</span></span>

<span data-ttu-id="45afa-196">您可以使用 [ **翻轉** 樣式] 屬性，根據下表，在其 x 或 y 軸上翻轉圖形：</span><span class="sxs-lookup"><span data-stu-id="45afa-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="45afa-197">值</span><span class="sxs-lookup"><span data-stu-id="45afa-197">Value</span></span> | <span data-ttu-id="45afa-198">描述</span><span class="sxs-lookup"><span data-stu-id="45afa-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="45afa-199">x</span><span class="sxs-lookup"><span data-stu-id="45afa-199">x</span></span>     | <span data-ttu-id="45afa-200">翻轉 y 軸的旋轉圖形 (反轉 x 座標) </span><span class="sxs-lookup"><span data-stu-id="45afa-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="45afa-201">y</span><span class="sxs-lookup"><span data-stu-id="45afa-201">y</span></span>     | <span data-ttu-id="45afa-202">翻轉 X 軸的旋轉圖形 (反轉 y 座標) </span><span class="sxs-lookup"><span data-stu-id="45afa-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="45afa-203">可以在 flip 屬性中指定 x 和 y。</span><span class="sxs-lookup"><span data-stu-id="45afa-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="45afa-204">例如，如果您輸入 **style**= ' .。。翻轉： x y '，您將會在其 x 和 y 軸上翻轉圖形。</span><span class="sxs-lookup"><span data-stu-id="45afa-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="45afa-205">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="45afa-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="45afa-206">總結</span><span class="sxs-lookup"><span data-stu-id="45afa-206">Summary</span></span>

<span data-ttu-id="45afa-207">根據您學到的內容，您可以依照下列步驟，精確地將圖形放在網頁上：</span><span class="sxs-lookup"><span data-stu-id="45afa-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="45afa-208">決定您希望圖形出現在網頁上的位置，以及圖形的大小。</span><span class="sxs-lookup"><span data-stu-id="45afa-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="45afa-209">請指定 **style**= ' position：相對 (或相對) '，以判斷基底點。</span><span class="sxs-lookup"><span data-stu-id="45afa-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="45afa-210">使用 **左邊** 和 **頂端** 來指定基底點的位移。</span><span class="sxs-lookup"><span data-stu-id="45afa-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="45afa-211">使用 [ **寬度** ] 和 [ **高度** ] 來指定圖形的包含方塊大小。</span><span class="sxs-lookup"><span data-stu-id="45afa-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="45afa-212">使用 **z-索引** 來指定圖形的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="45afa-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 