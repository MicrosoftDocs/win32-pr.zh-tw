---
title: 使用 Shadow 元素
description: 使用 Shadow 元素
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- 網路研討會，影子項目
- 設計網頁，shadow 元素
- Vector Markup Language (VML) 、shadow 元素
- VML (Vector Markup Language) 、shadow 元素
- 向量圖形、陰影元素
- shadow 元素
- VML 元素，陰影
- VML 圖形，shadow 元素
- Vector Markup Language (VML) ，以陰影效果繪製
- VML (Vector Markup Language) ，以陰影效果繪製
- 向量圖形，具有陰影效果的繪圖
- VML 圖形，具有陰影效果的繪圖
- 具有陰影效果的繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382666"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="74ace-116">使用 Shadow 元素</span><span class="sxs-lookup"><span data-stu-id="74ace-116">Using the Shadow Element</span></span>

<span data-ttu-id="74ace-117">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="74ace-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74ace-118">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="74ace-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74ace-119">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="74ace-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74ace-120">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="74ace-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74ace-121">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="74ace-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74ace-122">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="74ace-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74ace-123">在本主題中，我們將說明如何使用 `<shadow>` 子項目繪製具有各種陰影效果的圖形。</span><span class="sxs-lookup"><span data-stu-id="74ace-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="74ace-124">您可以將子專案放在 `<shadow>` `<shape>` 、 `<shapetype>` 或任何預先定義的 shape 元素內，以繪製具有陰影的圖形。</span><span class="sxs-lookup"><span data-stu-id="74ace-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="74ace-125">然後，您可以使用子項目的屬性屬性 `<shadow>` 來自訂陰影。</span><span class="sxs-lookup"><span data-stu-id="74ace-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="74ace-126">例如，若要建立具有陰影的圖形（如下圖所示），您可以在網頁的區域中輸入下列幾行 `<BODY>` ：</span><span class="sxs-lookup"><span data-stu-id="74ace-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 個位元組) ](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="74ace-128">`on="t"` 並 `type="perspective"` 指出使用透檢視類型來開啟陰影。</span><span class="sxs-lookup"><span data-stu-id="74ace-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="74ace-129">[ **來源** ] 和 [ **位移** ] 會指出要在哪裡繪製陰影。</span><span class="sxs-lookup"><span data-stu-id="74ace-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="74ace-130">`matrix="..."` 指定透視圖的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="74ace-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="74ace-131">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858396) 。</span><span class="sxs-lookup"><span data-stu-id="74ace-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 