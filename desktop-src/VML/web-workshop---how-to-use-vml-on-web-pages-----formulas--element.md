---
title: 使用公式元素
description: 使用公式元素
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web 研討會，公式元素
- 設計網頁、公式元素
- Vector Markup Language (VML) 、公式元素
- VML (Vector Markup Language) ，公式元素
- 向量圖形，公式元素
- 公式元素
- VML 元素，公式
- VML 圖形，公式元素
- Vector Markup Language (VML) ，定義圖形的路徑
- VML (Vector Markup Language) ，定義圖形的路徑
- 向量圖形，定義圖形的路徑
- VML 圖形，定義路徑
- 定義圖形的路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023535"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="bc059-116">使用公式元素</span><span class="sxs-lookup"><span data-stu-id="bc059-116">Using the Formulas Element</span></span>

<span data-ttu-id="bc059-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bc059-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bc059-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bc059-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bc059-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bc059-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bc059-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bc059-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bc059-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bc059-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bc059-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bc059-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bc059-123">在本主題中，我們將說明如何使用 `<formulas>` 子項目來定義圖形的可調整路徑。</span><span class="sxs-lookup"><span data-stu-id="bc059-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="bc059-124">您可以將子專案放 <formulas> 在或中， `<shape>` `<shapetype>` 以定義可以改變圖形路徑的公式。</span><span class="sxs-lookup"><span data-stu-id="bc059-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="bc059-125">在 `<formulas>` 子項目內，一個 **f** 子項目會定義一個公式，因此會根據該公式來評估一個值。</span><span class="sxs-lookup"><span data-stu-id="bc059-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="bc059-126">例如，公式 `<v:f eqn="prod 10 4 5"/>` 會定義相當於 "10 x 4/5" 的值。</span><span class="sxs-lookup"><span data-stu-id="bc059-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="bc059-127">您可以在一個子項目內放置許多 **f** 子項目 `<formulas>` 。</span><span class="sxs-lookup"><span data-stu-id="bc059-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="bc059-128">公式可以參考先前在相同子項目內其他公式中定義的值 `<formulas>` 。</span><span class="sxs-lookup"><span data-stu-id="bc059-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="bc059-129">第一個公式中定義的值可以參考為 @0 ，第二個公式中定義的值可以稱為 @1 ，依此類推。</span><span class="sxs-lookup"><span data-stu-id="bc059-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="bc059-130">此外，您可以指定元素的 **[** 調整] 屬性屬性 `<shape>` ，例如 [形容詞 = "100，200，150"]。</span><span class="sxs-lookup"><span data-stu-id="bc059-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="bc059-131">在專案內 `<formulas>` ，您可以在重新調整清單中參考這些值。</span><span class="sxs-lookup"><span data-stu-id="bc059-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="bc059-132">您可以將 **形容詞** 清單中 (100) 的第一個值稱為 \# 0，第二個值 (200) 可稱為 \# 1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="bc059-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="bc059-133">例如，若要繪製微笑的臉部，您可以輸入下列 VML 標記法：</span><span class="sxs-lookup"><span data-stu-id="bc059-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 個位元組) ](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="bc059-135">`adj="17520"` 定義值 (= 17520) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="bc059-136">這個值可以參考為 \# 0。</span><span class="sxs-lookup"><span data-stu-id="bc059-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="bc059-137">第一個公式會 `<v:f eqn="sum 33030 0 #0"/>` 定義值 (= 33030 + 0- \# 0) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="bc059-138">這個值可以參考為 @0 。</span><span class="sxs-lookup"><span data-stu-id="bc059-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="bc059-139">第二個公式會 `<v:f eqn="prod #0 4 3"/>` 定義值 (= \# 0 \* 4/3) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="bc059-140">這個值可以參考為 @1 。</span><span class="sxs-lookup"><span data-stu-id="bc059-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="bc059-141">第三個公式會 `<v:f eqn="prod @0 1 3"/>` 定義值 (= @0 \* 1/3) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="bc059-142">這個值可以參考為 @2 。</span><span class="sxs-lookup"><span data-stu-id="bc059-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="bc059-143">第四個公式會 `<v:f eqn="sum @1 0 @2"/>` 定義值 (= @1 + 0 -@2) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="bc059-144">這個值可以參考為 @3 。</span><span class="sxs-lookup"><span data-stu-id="bc059-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="bc059-145">在專案內 `<path>` ，第一個 (@0) 和第四個 () 公式中定義的值 @3 會用來判斷圖形的外框。</span><span class="sxs-lookup"><span data-stu-id="bc059-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="bc059-146">如果您變更 **形容詞** 清單（例如），則 `adj="20000"` 參考 **形容詞** 清單的公式值也會變更，並影響微笑面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bc059-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 個位元組) ](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="bc059-148">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858392) 。</span><span class="sxs-lookup"><span data-stu-id="bc059-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 