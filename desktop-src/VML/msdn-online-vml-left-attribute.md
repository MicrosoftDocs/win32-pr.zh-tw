---
title: VML 左方屬性
description: VML 左方屬性
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463600"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="a9f59-103">VML 左方屬性</span><span class="sxs-lookup"><span data-stu-id="a9f59-103">VML Left Attribute</span></span>

<span data-ttu-id="a9f59-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a9f59-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9f59-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a9f59-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9f59-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a9f59-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9f59-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a9f59-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9f59-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a9f59-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9f59-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a9f59-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9f59-110">決定圖形相對於檔流程中其左邊的元素位置。</span><span class="sxs-lookup"><span data-stu-id="a9f59-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="a9f59-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a9f59-111">Read/write.</span></span> <span data-ttu-id="a9f59-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="a9f59-112">**String**.</span></span>

<span data-ttu-id="a9f59-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a9f59-113">**Applies To**</span></span>

[<span data-ttu-id="a9f59-114">形狀</span><span class="sxs-lookup"><span data-stu-id="a9f59-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a9f59-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a9f59-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9f59-116"><v： *element* style = "left： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a9f59-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="a9f59-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a9f59-117">**Script Syntax**</span></span>

<span data-ttu-id="a9f59-118">style *. left* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a9f59-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="a9f59-119">*運算式* =*element*。 left</span><span class="sxs-lookup"><span data-stu-id="a9f59-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="a9f59-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a9f59-120">**Remarks**</span></span>

<span data-ttu-id="a9f59-121">**左邊** 的屬性類似于樣式的標準 HTML **Left** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a9f59-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="a9f59-122">單位可以對應至父元素，或可能是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="a9f59-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="a9f59-123">系統不會針對錨定的內嵌圖形來寫出這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a9f59-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="a9f59-124">數值包括：</span><span class="sxs-lookup"><span data-stu-id="a9f59-124">Values include:</span></span>



| <span data-ttu-id="a9f59-125">值</span><span class="sxs-lookup"><span data-stu-id="a9f59-125">Value</span></span>      | <span data-ttu-id="a9f59-126">描述</span><span class="sxs-lookup"><span data-stu-id="a9f59-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f59-127">自動</span><span class="sxs-lookup"><span data-stu-id="a9f59-127">Auto</span></span>       | <span data-ttu-id="a9f59-128">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="a9f59-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="a9f59-129">units</span><span class="sxs-lookup"><span data-stu-id="a9f59-129">units</span></span>      | <span data-ttu-id="a9f59-130">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="a9f59-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="a9f59-131">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="a9f59-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="a9f59-132">percentage</span><span class="sxs-lookup"><span data-stu-id="a9f59-132">percentage</span></span> | <span data-ttu-id="a9f59-133">以父物件寬度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="a9f59-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="a9f59-134">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a9f59-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="a9f59-135">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="a9f59-135">**See Also**</span></span>

[<span data-ttu-id="a9f59-136">單位</span><span class="sxs-lookup"><span data-stu-id="a9f59-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="a9f59-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="a9f59-137">**Example**</span></span>

<span data-ttu-id="a9f59-138">在下列範例中，圖形的左邊值設定為1。</span><span class="sxs-lookup"><span data-stu-id="a9f59-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="a9f59-139">[Left 屬性範例](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md)。</span><span class="sxs-lookup"><span data-stu-id="a9f59-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="a9f59-140"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="a9f59-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 