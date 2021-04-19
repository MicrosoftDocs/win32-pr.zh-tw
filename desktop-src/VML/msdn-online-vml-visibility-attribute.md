---
title: VML 可見度屬性
description: VML 可見度屬性
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967674"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="a295e-103">VML 可見度屬性</span><span class="sxs-lookup"><span data-stu-id="a295e-103">VML Visibility Attribute</span></span>

<span data-ttu-id="a295e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a295e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a295e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a295e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a295e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a295e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a295e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a295e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a295e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a295e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a295e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a295e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a295e-110">決定是否要顯示圖形。</span><span class="sxs-lookup"><span data-stu-id="a295e-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="a295e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a295e-111">Read/write.</span></span> <span data-ttu-id="a295e-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="a295e-112">**String**.</span></span>

<span data-ttu-id="a295e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a295e-113">**Applies To**</span></span>

[<span data-ttu-id="a295e-114">形狀</span><span class="sxs-lookup"><span data-stu-id="a295e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a295e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a295e-115">**Tag Syntax**</span></span>

<span data-ttu-id="a295e-116"><v： *element* style = "可見度： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a295e-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="a295e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a295e-117">**Script Syntax**</span></span>

<span data-ttu-id="a295e-118">style *. visibility* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a295e-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="a295e-119">*運算式* =*element*。 visibility</span><span class="sxs-lookup"><span data-stu-id="a295e-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="a295e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a295e-120">**Remarks**</span></span>

<span data-ttu-id="a295e-121">**可見度** 屬性類似于樣式的標準 HTML **可見度** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a295e-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="a295e-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="a295e-122">Values include:</span></span>



| <span data-ttu-id="a295e-123">值</span><span class="sxs-lookup"><span data-stu-id="a295e-123">Value</span></span>    | <span data-ttu-id="a295e-124">描述</span><span class="sxs-lookup"><span data-stu-id="a295e-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a295e-125">可見</span><span class="sxs-lookup"><span data-stu-id="a295e-125">visible</span></span>  | <span data-ttu-id="a295e-126">圖形是可見的。</span><span class="sxs-lookup"><span data-stu-id="a295e-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a295e-127">隱藏</span><span class="sxs-lookup"><span data-stu-id="a295e-127">hidden</span></span>   | <span data-ttu-id="a295e-128">圖形是不可見的，但仍是瀏覽器中物件流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="a295e-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="a295e-129">系統不會處理滑鼠事件。</span><span class="sxs-lookup"><span data-stu-id="a295e-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="a295e-130">inherit</span><span class="sxs-lookup"><span data-stu-id="a295e-130">inherit</span></span>  | <span data-ttu-id="a295e-131">預設值。</span><span class="sxs-lookup"><span data-stu-id="a295e-131">Default.</span></span> <span data-ttu-id="a295e-132">可見度狀態是繼承自圖形的父系。</span><span class="sxs-lookup"><span data-stu-id="a295e-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="a295e-133">Microsoft Office 的應用程式只會使用 **繼承** 和 **隱藏**;任何其他值都會對應到 **inherit**。</span><span class="sxs-lookup"><span data-stu-id="a295e-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="a295e-134">摺疊</span><span class="sxs-lookup"><span data-stu-id="a295e-134">collapse</span></span> | <span data-ttu-id="a295e-135">用於可折迭圖形群組的圖形編輯應用程式;例如，outliners。</span><span class="sxs-lookup"><span data-stu-id="a295e-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="a295e-136">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a295e-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="a295e-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="a295e-137">**Example**</span></span>

<span data-ttu-id="a295e-138">下列程式碼會建立一個圖形，但讓它隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="a295e-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="a295e-139">檔中的其他物件會在其周圍流動，讓空間的大小與圖形相同。</span><span class="sxs-lookup"><span data-stu-id="a295e-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="a295e-140">[可見度屬性範例](/previous-versions/bb264100(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a295e-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="a295e-141"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="a295e-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 