---
title: VML Top 屬性
description: VML Top 屬性
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682593"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="4053f-103">VML Top 屬性</span><span class="sxs-lookup"><span data-stu-id="4053f-103">VML Top Attribute</span></span>

<span data-ttu-id="4053f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4053f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4053f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4053f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4053f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4053f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4053f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4053f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4053f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4053f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4053f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4053f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4053f-110">定義圖形相對於頁面流程中其上方元素的位置。</span><span class="sxs-lookup"><span data-stu-id="4053f-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="4053f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4053f-111">Read/write.</span></span> <span data-ttu-id="4053f-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="4053f-112">**String**.</span></span>

<span data-ttu-id="4053f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4053f-113">**Applies To**</span></span>

[<span data-ttu-id="4053f-114">形狀</span><span class="sxs-lookup"><span data-stu-id="4053f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4053f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4053f-115">**Tag Syntax**</span></span>

<span data-ttu-id="4053f-116"><v： *element* style = "top： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4053f-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="4053f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4053f-117">**Script Syntax**</span></span>

<span data-ttu-id="4053f-118"> style.top = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4053f-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="4053f-119">*運算式* =\*\* style.top</span><span class="sxs-lookup"><span data-stu-id="4053f-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="4053f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4053f-120">**Remarks**</span></span>

<span data-ttu-id="4053f-121">**Top** 屬性類似于樣式的標準 HTML **Top** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4053f-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="4053f-122">單位可以對應至父元素，或可能是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="4053f-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="4053f-123">這個屬性可能不會針對錨定的內嵌圖形寫出。</span><span class="sxs-lookup"><span data-stu-id="4053f-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="4053f-124">數值包括：</span><span class="sxs-lookup"><span data-stu-id="4053f-124">Values include:</span></span>



| <span data-ttu-id="4053f-125">值</span><span class="sxs-lookup"><span data-stu-id="4053f-125">Value</span></span>      | <span data-ttu-id="4053f-126">描述</span><span class="sxs-lookup"><span data-stu-id="4053f-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4053f-127">自動</span><span class="sxs-lookup"><span data-stu-id="4053f-127">Auto</span></span>       | <span data-ttu-id="4053f-128">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="4053f-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="4053f-129">units</span><span class="sxs-lookup"><span data-stu-id="4053f-129">units</span></span>      | <span data-ttu-id="4053f-130">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="4053f-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="4053f-131">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="4053f-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="4053f-132">percentage</span><span class="sxs-lookup"><span data-stu-id="4053f-132">percentage</span></span> | <span data-ttu-id="4053f-133">以父物件高度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="4053f-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="4053f-134">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="4053f-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="4053f-135">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="4053f-135">**See Also**</span></span>

[<span data-ttu-id="4053f-136">單位</span><span class="sxs-lookup"><span data-stu-id="4053f-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="4053f-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="4053f-137">**Example**</span></span>

<span data-ttu-id="4053f-138">圖形的上邊緣是在頁面的前緣的物件下方的5圖元。</span><span class="sxs-lookup"><span data-stu-id="4053f-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="4053f-139">[Top 屬性範例](/previous-versions/bb264098(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4053f-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="4053f-140"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="4053f-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 