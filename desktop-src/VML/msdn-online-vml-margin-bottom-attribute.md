---
title: VML Margin-Bottom 屬性
description: VML Margin-Bottom 屬性
ms.assetid: c1101430-f4fc-4fa5-8e02-7cee126c2c1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35712733179a3c03dc291c4d5efcf4fee68c2865
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682738"
---
# <a name="vml-margin-bottom-attribute"></a><span data-ttu-id="b1443-103">VML Margin-Bottom 屬性</span><span class="sxs-lookup"><span data-stu-id="b1443-103">VML Margin-Bottom Attribute</span></span>

<span data-ttu-id="b1443-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b1443-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1443-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b1443-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1443-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b1443-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1443-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b1443-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1443-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b1443-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1443-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b1443-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1443-110">指定相對於圖形錨點之圖形內含矩形的下邊緣。</span><span class="sxs-lookup"><span data-stu-id="b1443-110">Specifies the bottom edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="b1443-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b1443-111">Read/write.</span></span> <span data-ttu-id="b1443-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b1443-112">**String**.</span></span>

<span data-ttu-id="b1443-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b1443-113">**Applies To**</span></span>

[<span data-ttu-id="b1443-114">形狀</span><span class="sxs-lookup"><span data-stu-id="b1443-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b1443-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b1443-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1443-116"><v： *element* margin-下 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b1443-116"><v: *element* margin-bottom=" *expression* "></span></span>

<span data-ttu-id="b1443-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b1443-117">**Script Syntax**</span></span>

<span data-ttu-id="b1443-118"> marginbottom = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b1443-118">*element* .marginbottom="*expression*"</span></span>

<span data-ttu-id="b1443-119">*運算式* =\*\* marginbottom</span><span class="sxs-lookup"><span data-stu-id="b1443-119">*expression*=*element*.marginbottom</span></span>

<span data-ttu-id="b1443-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b1443-120">**Remarks**</span></span>

<span data-ttu-id="b1443-121">上 **邊界** 屬性類似于樣式表單所使用的標準 HTML **邊界-下** 一個屬性。</span><span class="sxs-lookup"><span data-stu-id="b1443-121">The **Margin-Bottom** attribute is similar to the standard HTML **Margin-Bottom** attribute used with style sheets.</span></span>

<span data-ttu-id="b1443-122">請注意，會使用 **marginbottom** ，而不是使用 **邊界** 來進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="b1443-122">Note that **marginbottom** is used instead of **margin-bottom** for scripting.</span></span> <span data-ttu-id="b1443-123">另請注意，如果 **位置** 是 **絕對** 的，則邊界不會變更。</span><span class="sxs-lookup"><span data-stu-id="b1443-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="b1443-124">數值包括：</span><span class="sxs-lookup"><span data-stu-id="b1443-124">Values include:</span></span>



| <span data-ttu-id="b1443-125">值</span><span class="sxs-lookup"><span data-stu-id="b1443-125">Value</span></span>      | <span data-ttu-id="b1443-126">描述</span><span class="sxs-lookup"><span data-stu-id="b1443-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1443-127">自動</span><span class="sxs-lookup"><span data-stu-id="b1443-127">Auto</span></span>       | <span data-ttu-id="b1443-128">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="b1443-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="b1443-129">units</span><span class="sxs-lookup"><span data-stu-id="b1443-129">units</span></span>      | <span data-ttu-id="b1443-130">預設值。</span><span class="sxs-lookup"><span data-stu-id="b1443-130">Default.</span></span> <span data-ttu-id="b1443-131">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="b1443-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="b1443-132">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="b1443-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="b1443-133">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="b1443-133">The default value is 0.</span></span> |
| <span data-ttu-id="b1443-134">percentage</span><span class="sxs-lookup"><span data-stu-id="b1443-134">percentage</span></span> | <span data-ttu-id="b1443-135">以父物件高度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="b1443-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="b1443-136">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b1443-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="b1443-137">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="b1443-137">**See Also**</span></span>

[<span data-ttu-id="b1443-138">單位</span><span class="sxs-lookup"><span data-stu-id="b1443-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="b1443-139">**範例**</span><span class="sxs-lookup"><span data-stu-id="b1443-139">**Example**</span></span>

<span data-ttu-id="b1443-140">下邊界設定為25圖元。</span><span class="sxs-lookup"><span data-stu-id="b1443-140">The bottom margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-bottom:25px">
   </v:rect>
```



<span data-ttu-id="b1443-141">[毛利率-底端屬性範例](/previous-versions/bb229675(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b1443-141">[Margin-Bottom Attribute Example](/previous-versions/bb229675(v=vs.85)).</span></span> <span data-ttu-id="b1443-142"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="b1443-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 