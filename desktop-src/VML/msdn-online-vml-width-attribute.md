---
title: VML 寬度屬性
description: VML 寬度屬性
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967264"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="b6f85-103">VML 寬度屬性</span><span class="sxs-lookup"><span data-stu-id="b6f85-103">VML Width Attribute</span></span>

<span data-ttu-id="b6f85-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b6f85-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b6f85-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b6f85-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b6f85-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b6f85-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b6f85-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b6f85-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b6f85-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b6f85-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b6f85-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b6f85-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b6f85-110">定義圖形的寬度。</span><span class="sxs-lookup"><span data-stu-id="b6f85-110">Defines the width of the shape.</span></span> <span data-ttu-id="b6f85-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b6f85-111">Read/write.</span></span> <span data-ttu-id="b6f85-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b6f85-112">**String**.</span></span>

<span data-ttu-id="b6f85-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b6f85-113">**Applies To**</span></span>

[<span data-ttu-id="b6f85-114">形狀</span><span class="sxs-lookup"><span data-stu-id="b6f85-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b6f85-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b6f85-115">**Tag Syntax**</span></span>

<span data-ttu-id="b6f85-116"><v： *element* style = "width： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b6f85-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="b6f85-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b6f85-117">**Script Syntax**</span></span>

<span data-ttu-id="b6f85-118">*元素* 。 style. width = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b6f85-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="b6f85-119">*運算式* =style *. width*</span><span class="sxs-lookup"><span data-stu-id="b6f85-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="b6f85-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b6f85-120">**Remarks**</span></span>

<span data-ttu-id="b6f85-121">**寬度** 屬性類似于樣式的標準 HTML **寬度** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b6f85-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="b6f85-122">單位可以對應至父元素，或可能是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="b6f85-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="b6f85-123">數值包括：</span><span class="sxs-lookup"><span data-stu-id="b6f85-123">Values include:</span></span>



| <span data-ttu-id="b6f85-124">值</span><span class="sxs-lookup"><span data-stu-id="b6f85-124">Value</span></span>      | <span data-ttu-id="b6f85-125">描述</span><span class="sxs-lookup"><span data-stu-id="b6f85-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f85-126">自動</span><span class="sxs-lookup"><span data-stu-id="b6f85-126">Auto</span></span>       | <span data-ttu-id="b6f85-127">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="b6f85-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="b6f85-128">units</span><span class="sxs-lookup"><span data-stu-id="b6f85-128">units</span></span>      | <span data-ttu-id="b6f85-129">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="b6f85-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="b6f85-130">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="b6f85-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="b6f85-131">percentage</span><span class="sxs-lookup"><span data-stu-id="b6f85-131">percentage</span></span> | <span data-ttu-id="b6f85-132">以父物件寬度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="b6f85-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="b6f85-133">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b6f85-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="b6f85-134">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="b6f85-134">**See Also**</span></span>

[<span data-ttu-id="b6f85-135">單位</span><span class="sxs-lookup"><span data-stu-id="b6f85-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="b6f85-136">**範例**</span><span class="sxs-lookup"><span data-stu-id="b6f85-136">**Example**</span></span>

<span data-ttu-id="b6f85-137">圖形的寬度為25。</span><span class="sxs-lookup"><span data-stu-id="b6f85-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="b6f85-138">[Width 屬性範例](/previous-versions/bb264101(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b6f85-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="b6f85-139"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="b6f85-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 