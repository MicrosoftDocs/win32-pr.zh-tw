---
title: 著色圖形
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- 網路研討會，著色圖形
- 設計網頁、著色圖形
- Vector Markup Language (VML) 、著色圖形
- VML (Vector Markup Language) 、著色圖形
- 向量圖形，著色圖形
- VML 圖形，著色
- 著色圖形
- Vector Markup Language (VML) 、關鍵字色彩名稱
- VML (Vector Markup Language) ，關鍵字色彩名稱
- 向量圖形，關鍵字色彩名稱
- 關鍵字色彩名稱
- Vector Markup Language (VML) 、RGB triplet
- VML (Vector Markup Language) ，RGB triplet
- 向量圖形、RGB triplet
- RGB triplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023779"
---
# <a name="coloring-shapes"></a><span data-ttu-id="292b3-119">著色圖形</span><span class="sxs-lookup"><span data-stu-id="292b3-119">Coloring Shapes</span></span>

<span data-ttu-id="292b3-120">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="292b3-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="292b3-121">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="292b3-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="292b3-122">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="292b3-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="292b3-123">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="292b3-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="292b3-124">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="292b3-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="292b3-125">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="292b3-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="292b3-126">如先前幾節中所述，您可以使用 "red" 來代表紅色的色彩 "blue" 代表藍色的色彩，依此類推。</span><span class="sxs-lookup"><span data-stu-id="292b3-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="292b3-127">在本主題中，我們將說明如何以任何您想要的色彩繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="292b3-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="292b3-128">VML 延伸 HTML 和 CSS 色彩語法。</span><span class="sxs-lookup"><span data-stu-id="292b3-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="292b3-129">當 VML 專案的屬性型別為 color 時（例如 **fillcolor** 和 **strokecolor** ），您可以使用 [關鍵字色彩名稱](#keyword-color-name) 或 [RGB 三](#rgb-triplet)型來表示色彩。</span><span class="sxs-lookup"><span data-stu-id="292b3-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="292b3-130">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="292b3-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="292b3-131">關鍵字色彩名稱</span><span class="sxs-lookup"><span data-stu-id="292b3-131">Keyword Color Name</span></span>

<span data-ttu-id="292b3-132">HTML 4.0 定義關鍵字色彩名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="292b3-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="292b3-133">它們是淺綠色、黑色、藍色、fuchsia、灰色、綠色、橙色、暗灰色、navy、橄欖色、紫色、紅色、銀級、青色、白色和黃色。</span><span class="sxs-lookup"><span data-stu-id="292b3-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="292b3-134">這16種色彩的 RGB 值會以 [HTML 4.0 規格](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) 來定義。</span><span class="sxs-lookup"><span data-stu-id="292b3-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="292b3-135">例如，您可以藉由指定來繪製填滿黃色的矩形 `fillcolor="yellow"` ，並藉由指定來提供藍色外框 `strokecolor="blue"` ，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="292b3-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 個位元組) ](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="292b3-137">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="292b3-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="292b3-138">RGB 三</span><span class="sxs-lookup"><span data-stu-id="292b3-138">RGB Triplet</span></span>

<span data-ttu-id="292b3-139">如果色彩不是 [關鍵字色彩名稱](#keyword-color-name)，您可以將色彩表示為 rgb 十進位數或 rgb 十六進位三個十六進位。</span><span class="sxs-lookup"><span data-stu-id="292b3-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="292b3-140">使用 RGB triplet，您可以指定色彩的紅色、綠色和藍色元件的值，將每個元件設定為值範圍從0到255（十進位）或00到 FF （十六進位）。</span><span class="sxs-lookup"><span data-stu-id="292b3-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="292b3-141">例如，您可以在指定或的情況下，使用十進位值253、249、186的自訂色彩來建立填滿矩形的矩形 `fillcolor="rgb(253,249, 186)"` ， `fillcolor="#FDF9BA"` 如下列 VML 標記法所示。</span><span class="sxs-lookup"><span data-stu-id="292b3-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="292b3-142">在十六進位中，值253會變成 FD、249變成 F9，而186會變成 BA。</span><span class="sxs-lookup"><span data-stu-id="292b3-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 個位元組) ](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="292b3-144">如果 RGB 在十六進位中有像是 XXYYZZ 的模式，您可以將它縮寫為 XYZ。</span><span class="sxs-lookup"><span data-stu-id="292b3-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="292b3-145">例如，" \# 66FF99" 可以寫出為 " \# 6F9"。</span><span class="sxs-lookup"><span data-stu-id="292b3-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="292b3-146">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="292b3-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="292b3-147">總結</span><span class="sxs-lookup"><span data-stu-id="292b3-147">Summary</span></span>

<span data-ttu-id="292b3-148">在 VML 中，您可以使用下列其中一種格式來表示色彩：</span><span class="sxs-lookup"><span data-stu-id="292b3-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="292b3-149">fillcolor = "blue"</span><span class="sxs-lookup"><span data-stu-id="292b3-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="292b3-150">fillcolor = "rgb (0，0255) "</span><span class="sxs-lookup"><span data-stu-id="292b3-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="292b3-151">fillcolor = " \# 0000ff"</span><span class="sxs-lookup"><span data-stu-id="292b3-151">fillcolor="\#0000ff"</span></span>

 

 