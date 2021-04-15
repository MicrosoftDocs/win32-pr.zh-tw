---
title: 使用 Shapetype 元素
description: 使用 Shapetype 元素
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- 網路研討會，shapetype 元素
- 設計網頁、shapetype 元素
- Vector Markup Language (VML) 、shapetype 元素
- VML (Vector Markup Language) ，shapetype 元素
- 向量圖形，shapetype 元素
- shapetype 元素
- VML 元素，shapetype
- VML 圖形，shapetype 元素
- Vector Markup Language (VML) ，定義經常使用的圖形
- 使用 VML (Vector Markup Language) ，定義常用的圖形
- 向量圖形，定義常用的圖形
- 定義經常使用的圖形
- 使用定義常用的 VML 圖形
- Vector Markup Language (VML) ，具現化圖形的複本
- VML (Vector Markup Language) ，具現化圖形的複本
- 向量圖形，具現化圖形的複本
- 將圖形的複本具現化
- VML 圖形，具現化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463593"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="be962-121">使用 Shapetype 元素</span><span class="sxs-lookup"><span data-stu-id="be962-121">Using the Shapetype Element</span></span>

<span data-ttu-id="be962-122">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="be962-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be962-123">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="be962-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be962-124">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="be962-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be962-125">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="be962-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be962-126">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="be962-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be962-127">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="be962-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be962-128">在本主題中，我們將說明如何使用 `<shapetype>` 元素來定義您自己的常用圖形，然後從 shapetype 中具現化或建立圖形。</span><span class="sxs-lookup"><span data-stu-id="be962-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="be962-129">如果您想要繪製具有相同或類似屬性的許多圖形，如果您必須為每個圖形重複輸入相同的屬性屬性，就會很繁瑣。</span><span class="sxs-lookup"><span data-stu-id="be962-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="be962-130">VML 提供 `<shapetype>` 元素，讓您可以定義圖形的原型。</span><span class="sxs-lookup"><span data-stu-id="be962-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="be962-131">然後，您可以使用專案 `<shape>` ，從相同的 shapetype 具現化許多圖形複本。</span><span class="sxs-lookup"><span data-stu-id="be962-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="be962-132">您可以遵循下列三個步驟來定義 shapetype，然後從 shapetype 將圖形具現化：</span><span class="sxs-lookup"><span data-stu-id="be962-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="be962-133">輸入 `<shapetype>` 元素，並指定 id 屬性來為它命名。</span><span class="sxs-lookup"><span data-stu-id="be962-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="be962-134">使用屬性屬性或子項目來描述 shapetype。</span><span class="sxs-lookup"><span data-stu-id="be962-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="be962-135">藉由輸入元素將圖形具現化 `<shape>` ，並將圖形的型別屬性（attribute）參考到 shapetype 的 id 屬性（attribute）。</span><span class="sxs-lookup"><span data-stu-id="be962-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="be962-136">例如，您輸入下列幾行來建立名為 "MyShape" 的 shapetype：</span><span class="sxs-lookup"><span data-stu-id="be962-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="be962-137">然後，您可以藉由設定某些屬性屬性來改變 shapetype，例如 `fillcolor="red" strokecolor="blue"` 。</span><span class="sxs-lookup"><span data-stu-id="be962-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="be962-138">或者，您可以使用 shapetype 內的子項目，例如， `<path>` `<fill>` `<stroke>` (我們將在稍後的主題中討論這些子項目) 。</span><span class="sxs-lookup"><span data-stu-id="be962-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="be962-139">然後，您可以藉由指定將圖形從 shapetype "MyShape" 具現化， `type="#MyShape"` 如下列 VML 標記法所示。</span><span class="sxs-lookup"><span data-stu-id="be962-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="be962-140">此圖形會繼承 shapetype "MyShape" 的所有屬性，並顯示在其包含的方塊中，大小為 100 80。</span><span class="sxs-lookup"><span data-stu-id="be962-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="be962-141">您可以藉由指定 `type="#MyShape"` 和覆寫某些屬性（例如 `fillcolor="maroon"` ，如下列 VML 標記法所示），從 Shapetype "MyShape" 具現化另一個圖形。</span><span class="sxs-lookup"><span data-stu-id="be962-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="be962-142">此圖形會繼承 shapetype "MyShape" 中的所有屬性（除了 fillcolor 屬性以外），並顯示在其包含的方塊中，大小為 70 90。</span><span class="sxs-lookup"><span data-stu-id="be962-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="be962-143">以下是上述範例的完整 VML 標記法：</span><span class="sxs-lookup"><span data-stu-id="be962-143">Here is the complete VML representation for the preceding example:</span></span>

![type1 \-1.gif (477 個位元組) ](images/type1-1.gif)![type1 \-2.gif (471 個位元組) ](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="be962-146">如您所知，當圖形從 shapetype 具現化時，它會從 shapetype 繼承所有的屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="be962-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="be962-147">您可以藉由重新定義元素內的屬性來覆寫部分或全部繼承的屬性 `<shape>` 。</span><span class="sxs-lookup"><span data-stu-id="be962-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="be962-148">請注意，繼承只是一個層級。</span><span class="sxs-lookup"><span data-stu-id="be962-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="be962-149">這是因為只有 `<shape>` 元素可以參考專案 `<shapetype>` 。</span><span class="sxs-lookup"><span data-stu-id="be962-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="be962-150">`<shapetype>`元素無法參考另一個專案 `<shapetype>` 。</span><span class="sxs-lookup"><span data-stu-id="be962-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="be962-151">此外，shapetype 不屬於任何群組。</span><span class="sxs-lookup"><span data-stu-id="be962-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="be962-152">因此，專案 `<shapetype>` 可以本身或元素內出現 `<group>` 。</span><span class="sxs-lookup"><span data-stu-id="be962-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="be962-153">您可以在不同的群組中有許多參考相同 shapetype 的圖形。</span><span class="sxs-lookup"><span data-stu-id="be962-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="be962-154">如果 shapetype 出現在群組內，則在另一個群組中生活的圖形仍可參考此 shapetype。</span><span class="sxs-lookup"><span data-stu-id="be962-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="be962-155">例如，在下列 VML 表示中，Rect1 和 Rect2 是在 GroupA 中，而 Rect3 則是在 GroupB 中。</span><span class="sxs-lookup"><span data-stu-id="be962-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="be962-156">這三個矩形都會從 MyShape shapetype 具現化。</span><span class="sxs-lookup"><span data-stu-id="be962-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="be962-157">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858387) 。</span><span class="sxs-lookup"><span data-stu-id="be962-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 