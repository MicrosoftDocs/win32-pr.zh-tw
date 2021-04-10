---
title: 使用 Textpath 元素
description: 使用 Textpath 元素
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- 網路研討會，textpath 元素
- 設計網頁、textpath 元素
- Vector Markup Language (VML) 、textpath 元素
- VML (Vector Markup Language) ，textpath 元素
- 向量圖形，textpath 元素
- textpath 元素
- VML 元素，textpath
- VML 圖形，textpath 元素
- Vector Markup Language (VML) 、繪製文字
- VML (Vector Markup Language) 、繪製文字
- 向量圖形，繪製 VML 文字
- 繪製文字
- VML 圖形，繪製文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093223"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="a932b-116">使用 Textpath 元素</span><span class="sxs-lookup"><span data-stu-id="a932b-116">Using the Textpath Element</span></span>

<span data-ttu-id="a932b-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a932b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a932b-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a932b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a932b-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a932b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a932b-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a932b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a932b-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a932b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a932b-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a932b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a932b-123">在本主題中，我們將說明如何使用專案 `<textpath>` 來繪製具有各種樣式的文字。</span><span class="sxs-lookup"><span data-stu-id="a932b-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="a932b-124">您可以將子專案放 `<textpath>` 在內部 `<shape>` 或 `<shapetype>` 繪製文字。</span><span class="sxs-lookup"><span data-stu-id="a932b-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="a932b-125">然後，您可以使用子項目的屬性屬性 `<textpath>` 來自訂文字。</span><span class="sxs-lookup"><span data-stu-id="a932b-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="a932b-126">您也可以使用 `<formulas>` 子項目來定義文字的大綱。</span><span class="sxs-lookup"><span data-stu-id="a932b-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="a932b-127">例如，若要建立下圖中顯示的文字，您可以在下方輸入 VML 標記法。</span><span class="sxs-lookup"><span data-stu-id="a932b-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="a932b-128">請注意，我們使用 `<shapetype>` 元素來定義文字外框的原型。</span><span class="sxs-lookup"><span data-stu-id="a932b-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="a932b-129">然後，從相同的 shapetype 具現化兩個圖形。</span><span class="sxs-lookup"><span data-stu-id="a932b-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="a932b-130">您可以直接變更 **字串** 屬性屬性，以顯示不同的文字。</span><span class="sxs-lookup"><span data-stu-id="a932b-130">You can simply change the **string** property attribute to display different text.</span></span>

![shape1 \-1.gif (4898 個位元組) ](images/shape1-1t.gif)

![shape1 \-2.gif (2789 個位元組) ](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="a932b-133">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858398) 。</span><span class="sxs-lookup"><span data-stu-id="a932b-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 