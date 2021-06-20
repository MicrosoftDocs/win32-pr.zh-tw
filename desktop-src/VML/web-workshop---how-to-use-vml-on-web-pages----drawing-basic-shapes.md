---
title: 繪製基本圖形
description: 本文說明如何在 VML 中繪製基本圖形，這項功能已在 Windows Internet Explorer 9 淘汰。
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- 網路研討會，繪製圖形
- 設計網頁、繪製圖案
- Vector Markup Language (VML) 、繪製圖案
- VML (Vector Markup Language) 、繪製圖案
- 向量圖形，繪製圖形
- 繪製圖案
- VML 圖形，繪圖
- Vector Markup Language (VML) 、XML
- VML (Vector Markup Language) 、XML
- 向量圖形，XML
- Vector Markup Language (VML) 、CSS2
- VML (Vector Markup Language) 、CSS2
- 向量圖形、CSS2
- Vector Markup Language (VML) 、元素
- VML (Vector Markup Language) 、元素
- 向量圖形，元素
- VML 元素，繪製圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407731"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="e791f-120">繪製基本圖形</span><span class="sxs-lookup"><span data-stu-id="e791f-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="e791f-121">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="e791f-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e791f-122">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="e791f-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e791f-123">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="e791f-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e791f-124">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="e791f-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e791f-125">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="e791f-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e791f-126">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="e791f-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e791f-127">在本主題中，我們將說明使用 VML 繪製圖形有多麼容易。</span><span class="sxs-lookup"><span data-stu-id="e791f-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="e791f-128">若要在網頁上建立紅色橢圓（如下圖所示），您可以使用圖形編輯工具繪製 oval、將繪圖儲存為點陣圖，然後將點陣圖插入網頁上：</span><span class="sxs-lookup"><span data-stu-id="e791f-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 個位元組) ](images/oval1.gif)

<span data-ttu-id="e791f-130">或者，您也可以使用 VML 來繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="e791f-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="e791f-131">在上述範例中，您可以在網頁的區域中輸入下列幾行， `<BODY>` 以繪製紅色橢圓形：</span><span class="sxs-lookup"><span data-stu-id="e791f-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="e791f-132">`<v:...>` 和 `</v:...>` 是 [XML 語法](#xml-structure)中的開始標記和結束標記。`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="e791f-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="e791f-133">提供 [CSS 資訊](#css-information)。</span><span class="sxs-lookup"><span data-stu-id="e791f-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="e791f-134">**oval** 和 **fillcolor**= "red" 為 [VML 元素](#vml-elements)。</span><span class="sxs-lookup"><span data-stu-id="e791f-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="e791f-135">您只要變更了 VML 中的屬性屬性，就可以改變圖形。</span><span class="sxs-lookup"><span data-stu-id="e791f-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="e791f-136">在上述範例中，如果您變更 `fillcolor="red"` 為 `fillcolor="blue"` ，如下列 VML 標記法所示，紅色橢圓將會變更為藍色：</span><span class="sxs-lookup"><span data-stu-id="e791f-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="e791f-137">支援 VML 的瀏覽器可以轉譯和顯示 VML 中表示的圖形，而不需要下載個別的影像檔案。</span><span class="sxs-lookup"><span data-stu-id="e791f-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="e791f-138">在多個瀏覽器中呈現的大部分圖形都能更快轉譯，而且需要較少的磁碟空間和下載時間。</span><span class="sxs-lookup"><span data-stu-id="e791f-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="e791f-139">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="e791f-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="e791f-140">XML 結構</span><span class="sxs-lookup"><span data-stu-id="e791f-140">XML Structure</span></span>

<span data-ttu-id="e791f-141">根據可延伸標記語言 (XML)  (XML) 的規則來格式化 VML。</span><span class="sxs-lookup"><span data-stu-id="e791f-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="e791f-142">任何標準 XML 剖析器都可以剖析 VML，並將產生的資料交給 VML 特定的處理器。</span><span class="sxs-lookup"><span data-stu-id="e791f-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="e791f-143">您必須輸入一些資訊，例如 [命名空間](web-workshop---how-to-use-vml-on-web-pages----appendix.md) 和 [內嵌的自訂物件](web-workshop---how-to-use-vml-on-web-pages----appendix.md)，才能讓瀏覽器知道如何將資料交給 VML 特定的處理器。</span><span class="sxs-lookup"><span data-stu-id="e791f-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="e791f-144">然後，您可以使用 VML 在區域中輸入圖形， `<BODY>` 就如同您在上述範例中所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="e791f-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="e791f-145">`"v:"`每個 XML 標記上的前置詞會將標記識別為 VML。</span><span class="sxs-lookup"><span data-stu-id="e791f-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="e791f-146">`"v:"`區域中的前置詞 `<BODY>` 應該與一致 `<html xmlns:v="...">` 。</span><span class="sxs-lookup"><span data-stu-id="e791f-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="e791f-147">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="e791f-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="e791f-148">CSS 資訊</span><span class="sxs-lookup"><span data-stu-id="e791f-148">CSS Information</span></span>

<span data-ttu-id="e791f-149">VML 使用 [階層式樣式表、層級 2 (CSS2) ](https://www.w3.org/TR/PR-CSS2/) 來判斷圖形的大小，以及在網頁上放置圖形。</span><span class="sxs-lookup"><span data-stu-id="e791f-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="e791f-150">在上述範例中，我們將 oval 的大小指定為100點 (寬度) 75 點 (高度)  (`style='width:100pt;height:75pt'` ) 。</span><span class="sxs-lookup"><span data-stu-id="e791f-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="e791f-151">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="e791f-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="e791f-152">VML 元素</span><span class="sxs-lookup"><span data-stu-id="e791f-152">VML Elements</span></span>

<span data-ttu-id="e791f-153">在上述範例中，我們使用了 VML 預先定義的專案 `<oval>` 來繪製橢圓形。</span><span class="sxs-lookup"><span data-stu-id="e791f-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="e791f-154">接著，我們使用專案的 **fillcolor** 屬性屬性 `<oval>` ，以紅色填滿橢圓。</span><span class="sxs-lookup"><span data-stu-id="e791f-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="e791f-155">根據[XML 1.0 規格](https://www.w3.org/TR/REC-xml)的[開始標記、結束標記和 Empty-Element 標記](https://www.w3.org/TR/REC-xml#sec-starttags)區段，空的元素標記可用於沒有內容的任何元素。</span><span class="sxs-lookup"><span data-stu-id="e791f-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="e791f-156">例如，如下列 VML 標記法所示，元素中沒有任何內容 (子項目) `<oval>` 。</span><span class="sxs-lookup"><span data-stu-id="e791f-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="e791f-157"> (請注意， **style** 和 **fillcolor** 是元素的屬性， `<oval>` 不是子項目。 ) </span><span class="sxs-lookup"><span data-stu-id="e791f-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="e791f-158">因此，您可以使用空白元素標記（如下列 VML 標記法所示）來表示與上述程式碼相同的內容。</span><span class="sxs-lookup"><span data-stu-id="e791f-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="e791f-159">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="e791f-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="e791f-160">總結</span><span class="sxs-lookup"><span data-stu-id="e791f-160">Summary</span></span>

<span data-ttu-id="e791f-161">您可以使用 VML 在網頁上繪製圖形，然後藉由直接變更其屬性屬性來自訂這些圖形。</span><span class="sxs-lookup"><span data-stu-id="e791f-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="e791f-162">此外，在多個瀏覽器中呈現的大部分圖形都會以較快的速度轉譯，並縮短下載時間和磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="e791f-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 