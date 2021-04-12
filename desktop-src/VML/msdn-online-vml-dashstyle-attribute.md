---
title: VML DashStyle 屬性
description: VML DashStyle 屬性
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315316"
---
# <a name="vml-dashstyle-attribute"></a><span data-ttu-id="5ab95-103">VML DashStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="5ab95-103">VML DashStyle Attribute</span></span>

<span data-ttu-id="5ab95-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="5ab95-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5ab95-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="5ab95-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5ab95-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="5ab95-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5ab95-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="5ab95-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5ab95-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="5ab95-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5ab95-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="5ab95-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5ab95-110">指定筆劃的點和虛線模式。</span><span class="sxs-lookup"><span data-stu-id="5ab95-110">Specifies the dot and dash pattern for a stroke.</span></span> <span data-ttu-id="5ab95-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5ab95-111">Read/write.</span></span> <span data-ttu-id="5ab95-112">**VgLineDashStyle**。</span><span class="sxs-lookup"><span data-stu-id="5ab95-112">**VgLineDashStyle**.</span></span>

<span data-ttu-id="5ab95-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="5ab95-113">**Applies To**</span></span>

[<span data-ttu-id="5ab95-114">中風</span><span class="sxs-lookup"><span data-stu-id="5ab95-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5ab95-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="5ab95-115">**Tag Syntax**</span></span>

<span data-ttu-id="5ab95-116"><v： *element* dashstyle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5ab95-116"><v: *element* dashstyle=" *expression* "></span></span>

<span data-ttu-id="5ab95-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="5ab95-117">**Script Syntax**</span></span>

<span data-ttu-id="5ab95-118"> dashstyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5ab95-118">*element* .dashstyle="*expression*"</span></span>

<span data-ttu-id="5ab95-119">*運算式* =\*\* dashstyle</span><span class="sxs-lookup"><span data-stu-id="5ab95-119">*expression*=*element*.dashstyle</span></span>

<span data-ttu-id="5ab95-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="5ab95-120">**Remarks**</span></span>

<span data-ttu-id="5ab95-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="5ab95-121">Values include:</span></span>

-   <span data-ttu-id="5ab95-122">Solid (預設值)</span><span class="sxs-lookup"><span data-stu-id="5ab95-122">Solid (default)</span></span>
-   <span data-ttu-id="5ab95-123">ShortDash</span><span class="sxs-lookup"><span data-stu-id="5ab95-123">ShortDash</span></span>
-   <span data-ttu-id="5ab95-124">ShortDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-124">ShortDot</span></span>
-   <span data-ttu-id="5ab95-125">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-125">ShortDashDot</span></span>
-   <span data-ttu-id="5ab95-126">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-126">ShortDashDotDot</span></span>
-   <span data-ttu-id="5ab95-127">點</span><span class="sxs-lookup"><span data-stu-id="5ab95-127">Dot</span></span>
-   <span data-ttu-id="5ab95-128">虛線</span><span class="sxs-lookup"><span data-stu-id="5ab95-128">Dash</span></span>
-   <span data-ttu-id="5ab95-129">LongDash</span><span class="sxs-lookup"><span data-stu-id="5ab95-129">LongDash</span></span>
-   <span data-ttu-id="5ab95-130">DashDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-130">DashDot</span></span>
-   <span data-ttu-id="5ab95-131">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-131">LongDashDot</span></span>
-   <span data-ttu-id="5ab95-132">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="5ab95-132">LongDashDotDot</span></span>

<span data-ttu-id="5ab95-133">**DashStyle** 屬性可讓使用者指定自訂定義的虛線模式。</span><span class="sxs-lookup"><span data-stu-id="5ab95-133">The **DashStyle** attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="5ab95-134">這是使用一連串的數位來完成。</span><span class="sxs-lookup"><span data-stu-id="5ab95-134">This is done using a series of numbers.</span></span> <span data-ttu-id="5ab95-135">虛線樣式是以虛線的長度來定義， (筆觸的繪製部分) 和虛線之間的空間長度。</span><span class="sxs-lookup"><span data-stu-id="5ab95-135">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="5ab95-136">長度是相對於線條寬度： "1" 的長度等於線條的寬度。</span><span class="sxs-lookup"><span data-stu-id="5ab95-136">The lengths are relative to the line width: a length of "1" is equal to the line width.</span></span> <span data-ttu-id="5ab95-137">**EndCap** 樣式會套用至每個虛線，而箭號樣式則不適用。</span><span class="sxs-lookup"><span data-stu-id="5ab95-137">The **EndCap** style is applied to each dash, the arrow style is not.</span></span> <span data-ttu-id="5ab95-138">字串會先定義虛線的長度，然後再定義空間的長度。</span><span class="sxs-lookup"><span data-stu-id="5ab95-138">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="5ab95-139">這可能會重複形成複雜的虛線樣式。</span><span class="sxs-lookup"><span data-stu-id="5ab95-139">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="5ab95-140">字串應該一律包含成對的數位;如果它包含奇數數目的數位，則可能會忽略最後一個。</span><span class="sxs-lookup"><span data-stu-id="5ab95-140">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span>

<span data-ttu-id="5ab95-141">下表列出一些一般值和預期效果的描述。</span><span class="sxs-lookup"><span data-stu-id="5ab95-141">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="5ab95-142">「0」意指點應該是 epirus 對稱 (使用「迴圈結束」端點，其應為圓形) 。</span><span class="sxs-lookup"><span data-stu-id="5ab95-142">"0" implies a dot that should be fourfold symmetrical (with round end caps it should be a circle).</span></span> <span data-ttu-id="5ab95-143">如果行尾端點是「平面」，則檢視器應該選擇內建的作業系統虛線，可能的 (換句話說。</span><span class="sxs-lookup"><span data-stu-id="5ab95-143">If the line end cap is "flat," a viewer should choose a built-in operating system dash where possible (in other words.</span></span> <span data-ttu-id="5ab95-144">快速繪製的東西。 ) 。</span><span class="sxs-lookup"><span data-stu-id="5ab95-144">something that is fast to draw.).</span></span> <span data-ttu-id="5ab95-145">下表顯示一些範例。</span><span class="sxs-lookup"><span data-stu-id="5ab95-145">The following table shows some examples.</span></span>



| <span data-ttu-id="5ab95-146">DashStyle</span><span class="sxs-lookup"><span data-stu-id="5ab95-146">DashStyle</span></span>     | <span data-ttu-id="5ab95-147">Description</span><span class="sxs-lookup"><span data-stu-id="5ab95-147">Description</span></span>                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab95-148">"2 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-148">"2 2"</span></span>         | <span data-ttu-id="5ab95-149">短破折號。</span><span class="sxs-lookup"><span data-stu-id="5ab95-149">Short-dashes.</span></span> <span data-ttu-id="5ab95-150">每個虛線和兩者之間的間距是線條寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="5ab95-150">Each dash and the space between is twice the width of the line.</span></span>                        |
| <span data-ttu-id="5ab95-151">"0 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-151">"0 2"</span></span>         | <span data-ttu-id="5ab95-152">點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-152">Dots.</span></span> <span data-ttu-id="5ab95-153">介於兩者之間的空格是線條寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="5ab95-153">Space between is twice the width of the line.</span></span>                                                  |
| <span data-ttu-id="5ab95-154">"2 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-154">"2 2 0 2"</span></span>     | <span data-ttu-id="5ab95-155">短虛線。</span><span class="sxs-lookup"><span data-stu-id="5ab95-155">Short dash dot.</span></span>                                                                                      |
| <span data-ttu-id="5ab95-156">"2 2 0 2 0 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-156">"2 2 0 2 0 2"</span></span> | <span data-ttu-id="5ab95-157">短虛線點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-157">Short dash dot dot.</span></span>                                                                                  |
| <span data-ttu-id="5ab95-158">"1 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-158">"1 2"</span></span>         | <span data-ttu-id="5ab95-159">點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-159">Dot.</span></span> <span data-ttu-id="5ab95-160">每個虛線都是線條的寬度，而每個空間都是線條寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="5ab95-160">Each dash is the width of the line, while each space is twice the width of the line.</span></span>            |
| <span data-ttu-id="5ab95-161">"4 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-161">"4 2"</span></span>         | <span data-ttu-id="5ab95-162">破折號。</span><span class="sxs-lookup"><span data-stu-id="5ab95-162">Dash.</span></span> <span data-ttu-id="5ab95-163">每個虛線都是線條寬度的四倍，而每個空格是線條寬度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="5ab95-163">Each dash is four times the width of the line while each space is twice the width of the line.</span></span> |
| <span data-ttu-id="5ab95-164">"8 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-164">"8 2"</span></span>         | <span data-ttu-id="5ab95-165">長虛線。</span><span class="sxs-lookup"><span data-stu-id="5ab95-165">Long dash.</span></span>                                                                                           |
| <span data-ttu-id="5ab95-166">"4 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-166">"4 2 1 2"</span></span>     | <span data-ttu-id="5ab95-167">虛線。</span><span class="sxs-lookup"><span data-stu-id="5ab95-167">Dash dot.</span></span>                                                                                            |
| <span data-ttu-id="5ab95-168">"8 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-168">"8 2 1 2"</span></span>     | <span data-ttu-id="5ab95-169">長虛線點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-169">Long dash dot.</span></span>                                                                                       |
| <span data-ttu-id="5ab95-170">"8 2 1 2 1 2"</span><span class="sxs-lookup"><span data-stu-id="5ab95-170">"8 2 1 2 1 2"</span></span> | <span data-ttu-id="5ab95-171">長虛線點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-171">Long dash dot dot.</span></span>                                                                                   |



 

<span data-ttu-id="5ab95-172">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="5ab95-172">*VML Standard Attribute*</span></span>

<span data-ttu-id="5ab95-173">**範例**</span><span class="sxs-lookup"><span data-stu-id="5ab95-173">**Example**</span></span>

<span data-ttu-id="5ab95-174">圖形具有虛線樣式的交替虛線和點。</span><span class="sxs-lookup"><span data-stu-id="5ab95-174">The shape has a dash style of alternating dashes and dots.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 