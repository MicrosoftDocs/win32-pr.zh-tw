---
title: VML Z 索引屬性
description: VML Z 索引屬性
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933304"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="57751-103">VML Z 索引屬性</span><span class="sxs-lookup"><span data-stu-id="57751-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="57751-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="57751-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="57751-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="57751-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="57751-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="57751-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="57751-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="57751-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="57751-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="57751-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="57751-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="57751-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="57751-110">決定重迭圖形的顯示順序。</span><span class="sxs-lookup"><span data-stu-id="57751-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="57751-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="57751-111">Read/write.</span></span> <span data-ttu-id="57751-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="57751-112">**String**.</span></span>

<span data-ttu-id="57751-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="57751-113">**Applies To**</span></span>

[<span data-ttu-id="57751-114">形狀</span><span class="sxs-lookup"><span data-stu-id="57751-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="57751-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="57751-115">**Tag Syntax**</span></span>

<span data-ttu-id="57751-116"><v： *element* style = "z-index： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="57751-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="57751-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="57751-117">**Script Syntax**</span></span>

<span data-ttu-id="57751-118"> zindex = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="57751-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="57751-119">*運算式* =\*\* zindex</span><span class="sxs-lookup"><span data-stu-id="57751-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="57751-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="57751-120">**Remarks**</span></span>

<span data-ttu-id="57751-121">**Z 索引** 屬性類似于樣式的標準 HTML **Z 索引** 屬性。</span><span class="sxs-lookup"><span data-stu-id="57751-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="57751-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="57751-122">Values include:</span></span>



| <span data-ttu-id="57751-123">值</span><span class="sxs-lookup"><span data-stu-id="57751-123">Value</span></span> | <span data-ttu-id="57751-124">描述</span><span class="sxs-lookup"><span data-stu-id="57751-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57751-125">自動</span><span class="sxs-lookup"><span data-stu-id="57751-125">Auto</span></span>  | <span data-ttu-id="57751-126">圖形出現在 HTML 網頁中的順序將會使用，由下往上。</span><span class="sxs-lookup"><span data-stu-id="57751-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="57751-127">順序</span><span class="sxs-lookup"><span data-stu-id="57751-127">order</span></span> | <span data-ttu-id="57751-128">表示堆疊優先順序的數位。</span><span class="sxs-lookup"><span data-stu-id="57751-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="57751-129">具有較高數位的圖形會顯示為 wereoverlapping 在) 圖形的「前方」 (的數位較低的形狀。</span><span class="sxs-lookup"><span data-stu-id="57751-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="57751-130">您可以使用負數。</span><span class="sxs-lookup"><span data-stu-id="57751-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="57751-131">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="57751-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="57751-132">**範例**</span><span class="sxs-lookup"><span data-stu-id="57751-132">**Example**</span></span>

<span data-ttu-id="57751-133">紅色圖形將會顯示在藍色圖形的「前方」中，因為它的 Z 軸索引較高。</span><span class="sxs-lookup"><span data-stu-id="57751-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="57751-134">[Z-索引屬性範例](/previous-versions/ms530275(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="57751-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="57751-135"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="57751-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 