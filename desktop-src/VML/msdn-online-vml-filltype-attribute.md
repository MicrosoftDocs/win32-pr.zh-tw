---
title: VML FillType 屬性
description: VML FillType 屬性
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933590"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="86eec-103">VML FillType 屬性</span><span class="sxs-lookup"><span data-stu-id="86eec-103">VML FillType Attribute</span></span>

<span data-ttu-id="86eec-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="86eec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86eec-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="86eec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86eec-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="86eec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86eec-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="86eec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86eec-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="86eec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86eec-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="86eec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86eec-110">定義用於筆劃背景的填滿類型。</span><span class="sxs-lookup"><span data-stu-id="86eec-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="86eec-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="86eec-111">Read/write.</span></span> <span data-ttu-id="86eec-112">**VgFillType**。</span><span class="sxs-lookup"><span data-stu-id="86eec-112">**VgFillType**.</span></span>

<span data-ttu-id="86eec-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="86eec-113">**Applies To**</span></span>

[<span data-ttu-id="86eec-114">中風</span><span class="sxs-lookup"><span data-stu-id="86eec-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="86eec-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="86eec-115">**Tag Syntax**</span></span>

<span data-ttu-id="86eec-116"><v： *element* filltype = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="86eec-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="86eec-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="86eec-117">**Script Syntax**</span></span>

<span data-ttu-id="86eec-118"> filltype = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="86eec-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="86eec-119">*運算式* =\*\* filltype</span><span class="sxs-lookup"><span data-stu-id="86eec-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="86eec-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="86eec-120">**Remarks**</span></span>

<span data-ttu-id="86eec-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="86eec-121">Values include:</span></span>



| <span data-ttu-id="86eec-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="86eec-122">DashStyle</span></span> | <span data-ttu-id="86eec-123">Description</span><span class="sxs-lookup"><span data-stu-id="86eec-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="86eec-124">實線</span><span class="sxs-lookup"><span data-stu-id="86eec-124">Solid</span></span>     | <span data-ttu-id="86eec-125">填滿模式是實心。</span><span class="sxs-lookup"><span data-stu-id="86eec-125">The fill pattern is solid.</span></span> <span data-ttu-id="86eec-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="86eec-126">Default value.</span></span>      |
| <span data-ttu-id="86eec-127">磚</span><span class="sxs-lookup"><span data-stu-id="86eec-127">Tile</span></span>      | <span data-ttu-id="86eec-128">填滿影像會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="86eec-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="86eec-129">模式</span><span class="sxs-lookup"><span data-stu-id="86eec-129">Pattern</span></span>   | <span data-ttu-id="86eec-130">填滿影像以形成一種模式。</span><span class="sxs-lookup"><span data-stu-id="86eec-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="86eec-131">Frame</span><span class="sxs-lookup"><span data-stu-id="86eec-131">Frame</span></span>     | <span data-ttu-id="86eec-132">填滿影像會變成圖形的框線。</span><span class="sxs-lookup"><span data-stu-id="86eec-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="86eec-133">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="86eec-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="86eec-134">**範例**</span><span class="sxs-lookup"><span data-stu-id="86eec-134">**Example**</span></span>

<span data-ttu-id="86eec-135">圖形的筆觸具有從 cylinder.gif 影像建立的磚材質。</span><span class="sxs-lookup"><span data-stu-id="86eec-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 