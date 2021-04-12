---
title: VML Margin-Left 屬性
description: VML Margin-Left 屬性
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315802"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="416e2-103">VML Margin-Left 屬性</span><span class="sxs-lookup"><span data-stu-id="416e2-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="416e2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="416e2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="416e2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="416e2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="416e2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="416e2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="416e2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="416e2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="416e2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="416e2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="416e2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="416e2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="416e2-110">指定相對於圖形錨點之圖形內含矩形的左邊緣。</span><span class="sxs-lookup"><span data-stu-id="416e2-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="416e2-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="416e2-111">Read/write.</span></span> <span data-ttu-id="416e2-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="416e2-112">**String**.</span></span>

<span data-ttu-id="416e2-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="416e2-113">**Applies To**</span></span>

[<span data-ttu-id="416e2-114">形狀</span><span class="sxs-lookup"><span data-stu-id="416e2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="416e2-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="416e2-115">**Tag Syntax**</span></span>

<span data-ttu-id="416e2-116"><v： *element* style = "margin-left： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="416e2-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="416e2-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="416e2-117">**Script Syntax**</span></span>

<span data-ttu-id="416e2-118"> marginleft = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="416e2-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="416e2-119">*運算式* =\*\* marginleft</span><span class="sxs-lookup"><span data-stu-id="416e2-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="416e2-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="416e2-120">**Remarks**</span></span>

<span data-ttu-id="416e2-121">**左邊界** 屬性類似于樣式表單所使用的標準 HTML **左邊界** 屬性。</span><span class="sxs-lookup"><span data-stu-id="416e2-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="416e2-122">請注意， **marginleft** 是用來取代腳本的 **左邊界** 。</span><span class="sxs-lookup"><span data-stu-id="416e2-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="416e2-123">另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。</span><span class="sxs-lookup"><span data-stu-id="416e2-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="416e2-124">這個屬性是針對 Microsoft Word 和 Microsoft Excel 中的圖形所使用，而不是 **左** 于相對於錨點的位置。</span><span class="sxs-lookup"><span data-stu-id="416e2-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="416e2-125">數值包括：</span><span class="sxs-lookup"><span data-stu-id="416e2-125">Values include:</span></span>



| <span data-ttu-id="416e2-126">值</span><span class="sxs-lookup"><span data-stu-id="416e2-126">Value</span></span>      | <span data-ttu-id="416e2-127">描述</span><span class="sxs-lookup"><span data-stu-id="416e2-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416e2-128">自動</span><span class="sxs-lookup"><span data-stu-id="416e2-128">Auto</span></span>       | <span data-ttu-id="416e2-129">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="416e2-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="416e2-130">units</span><span class="sxs-lookup"><span data-stu-id="416e2-130">units</span></span>      | <span data-ttu-id="416e2-131">預設值。</span><span class="sxs-lookup"><span data-stu-id="416e2-131">Default.</span></span> <span data-ttu-id="416e2-132">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="416e2-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="416e2-133">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="416e2-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="416e2-134">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="416e2-134">The default value is 0.</span></span> |
| <span data-ttu-id="416e2-135">percentage</span><span class="sxs-lookup"><span data-stu-id="416e2-135">percentage</span></span> | <span data-ttu-id="416e2-136">以父物件高度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="416e2-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="416e2-137">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="416e2-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="416e2-138">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="416e2-138">**See Also**</span></span>

[<span data-ttu-id="416e2-139">單位</span><span class="sxs-lookup"><span data-stu-id="416e2-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="416e2-140">**範例**</span><span class="sxs-lookup"><span data-stu-id="416e2-140">**Example**</span></span>

<span data-ttu-id="416e2-141">左邊界設定為25圖元。</span><span class="sxs-lookup"><span data-stu-id="416e2-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="416e2-142">[左邊界屬性範例](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples)。</span><span class="sxs-lookup"><span data-stu-id="416e2-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="416e2-143"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="416e2-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 