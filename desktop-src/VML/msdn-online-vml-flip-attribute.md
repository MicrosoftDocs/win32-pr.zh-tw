---
title: VML Flip 屬性
description: VML Flip 屬性
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683069"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="8a82e-103">VML Flip 屬性</span><span class="sxs-lookup"><span data-stu-id="8a82e-103">VML Flip Attribute</span></span>

<span data-ttu-id="8a82e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8a82e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8a82e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8a82e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8a82e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8a82e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8a82e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8a82e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8a82e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8a82e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8a82e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8a82e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8a82e-110">切換圖形的方向。</span><span class="sxs-lookup"><span data-stu-id="8a82e-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="8a82e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8a82e-111">Read/write.</span></span> <span data-ttu-id="8a82e-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="8a82e-112">**String**.</span></span>

<span data-ttu-id="8a82e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8a82e-113">**Applies To**</span></span>

[<span data-ttu-id="8a82e-114">形狀</span><span class="sxs-lookup"><span data-stu-id="8a82e-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8a82e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8a82e-115">**Tag Syntax**</span></span>

<span data-ttu-id="8a82e-116"><v： *element* style = "flip： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8a82e-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="8a82e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8a82e-117">**Script Syntax**</span></span>

<span data-ttu-id="8a82e-118">*element* 。 style. flip = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8a82e-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="8a82e-119">*運算式* =*element*. style. flip</span><span class="sxs-lookup"><span data-stu-id="8a82e-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="8a82e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8a82e-120">**Remarks**</span></span>

<span data-ttu-id="8a82e-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="8a82e-121">Values include:</span></span>



| <span data-ttu-id="8a82e-122">值</span><span class="sxs-lookup"><span data-stu-id="8a82e-122">Value</span></span> | <span data-ttu-id="8a82e-123">描述</span><span class="sxs-lookup"><span data-stu-id="8a82e-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="8a82e-124">x</span><span class="sxs-lookup"><span data-stu-id="8a82e-124">x</span></span>     | <span data-ttu-id="8a82e-125">沿著 y 軸翻轉，反轉 *x* 座標。</span><span class="sxs-lookup"><span data-stu-id="8a82e-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="8a82e-126">y</span><span class="sxs-lookup"><span data-stu-id="8a82e-126">y</span></span>     | <span data-ttu-id="8a82e-127">沿著 *x* 軸翻轉，反轉 y 座標。</span><span class="sxs-lookup"><span data-stu-id="8a82e-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="8a82e-128">xy</span><span class="sxs-lookup"><span data-stu-id="8a82e-128">xy</span></span>    | <span data-ttu-id="8a82e-129">沿著 y 軸和 *x* 軸翻轉。</span><span class="sxs-lookup"><span data-stu-id="8a82e-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="8a82e-130">yx</span><span class="sxs-lookup"><span data-stu-id="8a82e-130">yx</span></span>    | <span data-ttu-id="8a82e-131">沿著 *x* 軸和 *y* 軸翻轉。</span><span class="sxs-lookup"><span data-stu-id="8a82e-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="8a82e-132">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="8a82e-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="8a82e-133">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="8a82e-133">**See Also**</span></span>

[<span data-ttu-id="8a82e-134">VgFlipOrientation</span><span class="sxs-lookup"><span data-stu-id="8a82e-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="8a82e-135">**範例**</span><span class="sxs-lookup"><span data-stu-id="8a82e-135">**Example**</span></span>

<span data-ttu-id="8a82e-136">圖形會反轉 *x* 座標，沿著 *y* 軸翻轉。</span><span class="sxs-lookup"><span data-stu-id="8a82e-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="8a82e-137">[Flip 屬性範例](/previous-versions/bb229670(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8a82e-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="8a82e-138"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="8a82e-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 