---
title: VML Margin-Top 屬性
description: VML Margin-Top 屬性
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14b6f4743f04740fe3fdbac4cc1d03f7bbe0282
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316405"
---
# <a name="vml-margin-top-attribute"></a><span data-ttu-id="4525b-103">VML Margin-Top 屬性</span><span class="sxs-lookup"><span data-stu-id="4525b-103">VML Margin-Top Attribute</span></span>

<span data-ttu-id="4525b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4525b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4525b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4525b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4525b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4525b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4525b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4525b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4525b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4525b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4525b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4525b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4525b-110">指定相對於圖形錨點之圖形內含矩形的上邊緣。</span><span class="sxs-lookup"><span data-stu-id="4525b-110">Specifies the top edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="4525b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4525b-111">Read/write.</span></span> <span data-ttu-id="4525b-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="4525b-112">**String**.</span></span>

<span data-ttu-id="4525b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4525b-113">**Applies To**</span></span>

[<span data-ttu-id="4525b-114">形狀</span><span class="sxs-lookup"><span data-stu-id="4525b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="4525b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4525b-115">**Tag Syntax**</span></span>

<span data-ttu-id="4525b-116"><v： *element* margin-top = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4525b-116"><v: *element* margin-top=" *expression* "></span></span>

<span data-ttu-id="4525b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4525b-117">**Script Syntax**</span></span>

<span data-ttu-id="4525b-118">*元素* 。 margin-top = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4525b-118">*element* .margin-top="*expression*"</span></span>

<span data-ttu-id="4525b-119">*運算式* =*元素*。邊界-上方</span><span class="sxs-lookup"><span data-stu-id="4525b-119">*expression*=*element*.margin-top</span></span>

<span data-ttu-id="4525b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4525b-120">**Remarks**</span></span>

<span data-ttu-id="4525b-121">**上邊界** 屬性類似于標準 HTML 邊界-與樣式表單搭配使用的 **最上層** 屬性。</span><span class="sxs-lookup"><span data-stu-id="4525b-121">The **Margin-Top** attribute is similar to the standard HTML **Margin-Top** attribute used with style sheets.</span></span>

<span data-ttu-id="4525b-122">請注意， **margintop** 是用來取代 **最上層** 的腳本。</span><span class="sxs-lookup"><span data-stu-id="4525b-122">Note that **margintop** is used instead of **margin-top** for scripting.</span></span> <span data-ttu-id="4525b-123">另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。</span><span class="sxs-lookup"><span data-stu-id="4525b-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="4525b-124">針對 Microsoft Word 和 Microsoft Excel 中，在相對於錨點的位置浮動的圖形，會使用這個屬性，而不是 **上方** 。</span><span class="sxs-lookup"><span data-stu-id="4525b-124">This property is used instead of **Top** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="4525b-125">數值包括：</span><span class="sxs-lookup"><span data-stu-id="4525b-125">Values include:</span></span>



| <span data-ttu-id="4525b-126">值</span><span class="sxs-lookup"><span data-stu-id="4525b-126">Value</span></span>      | <span data-ttu-id="4525b-127">描述</span><span class="sxs-lookup"><span data-stu-id="4525b-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4525b-128">自動</span><span class="sxs-lookup"><span data-stu-id="4525b-128">Auto</span></span>       | <span data-ttu-id="4525b-129">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="4525b-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="4525b-130">units</span><span class="sxs-lookup"><span data-stu-id="4525b-130">units</span></span>      | <span data-ttu-id="4525b-131">預設值。</span><span class="sxs-lookup"><span data-stu-id="4525b-131">Default.</span></span> <span data-ttu-id="4525b-132">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="4525b-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="4525b-133">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="4525b-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="4525b-134">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="4525b-134">The default value is 0.</span></span> |
| <span data-ttu-id="4525b-135">percentage</span><span class="sxs-lookup"><span data-stu-id="4525b-135">percentage</span></span> | <span data-ttu-id="4525b-136">以父物件高度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="4525b-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="4525b-137">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="4525b-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="4525b-138">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="4525b-138">**See Also**</span></span>

[<span data-ttu-id="4525b-139">單位</span><span class="sxs-lookup"><span data-stu-id="4525b-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="4525b-140">**範例**</span><span class="sxs-lookup"><span data-stu-id="4525b-140">**Example**</span></span>

<span data-ttu-id="4525b-141">上邊界設定為25圖元。</span><span class="sxs-lookup"><span data-stu-id="4525b-141">The top margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



<span data-ttu-id="4525b-142">[Margin-Top 屬性範例](/previous-versions/bb264087(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4525b-142">[Margin-Top Attribute Example](/previous-versions/bb264087(v=vs.85)).</span></span> <span data-ttu-id="4525b-143"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="4525b-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 