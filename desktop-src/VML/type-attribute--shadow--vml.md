---
title: 'Type 屬性 (Shadow)  (VML) '
description: 'Type 屬性 (Shadow)  (VML) '
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376012"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="cdfb8-103">Type 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="cdfb8-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="cdfb8-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cdfb8-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cdfb8-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cdfb8-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cdfb8-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cdfb8-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cdfb8-110">指定陰影的類型。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-110">Specifies the type of shadow.</span></span> <span data-ttu-id="cdfb8-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cdfb8-111">Read/write.</span></span> <span data-ttu-id="cdfb8-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-112">**String**.</span></span>

<span data-ttu-id="cdfb8-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-113">**Applies To**</span></span>

[<span data-ttu-id="cdfb8-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="cdfb8-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="cdfb8-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-115">**Tag Syntax**</span></span>

<span data-ttu-id="cdfb8-116"><v： *element* type = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cdfb8-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="cdfb8-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-117">**Script Syntax**</span></span>

<span data-ttu-id="cdfb8-118">*element* 。 type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cdfb8-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="cdfb8-119">*運算式* =*元素*。類型</span><span class="sxs-lookup"><span data-stu-id="cdfb8-119">*expression*=*element*.type</span></span>

<span data-ttu-id="cdfb8-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-120">**Remarks**</span></span>

<span data-ttu-id="cdfb8-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="cdfb8-121">Values include:</span></span>



| <span data-ttu-id="cdfb8-122">值</span><span class="sxs-lookup"><span data-stu-id="cdfb8-122">Value</span></span>           | <span data-ttu-id="cdfb8-123">描述</span><span class="sxs-lookup"><span data-stu-id="cdfb8-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdfb8-124">single</span><span class="sxs-lookup"><span data-stu-id="cdfb8-124">single</span></span>          | <span data-ttu-id="cdfb8-125">單一陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-125">Single shadow.</span></span> <span data-ttu-id="cdfb8-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="cdfb8-127">double</span><span class="sxs-lookup"><span data-stu-id="cdfb8-127">double</span></span>          | <span data-ttu-id="cdfb8-128">雙陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-128">A double shadow.</span></span> <span data-ttu-id="cdfb8-129">[Color2](color2-attribute--shadow--vml.md) 用於第二個陰影的色彩，而 [Offset2](msdn-online-vml-offset2-attribute.md) 則用於第二個陰影的位移。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="cdfb8-130">檢視方塊</span><span class="sxs-lookup"><span data-stu-id="cdfb8-130">perspective</span></span>     | <span data-ttu-id="cdfb8-131">觀點陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="cdfb8-132">shapeRelative</span><span class="sxs-lookup"><span data-stu-id="cdfb8-132">shapeRelative</span></span>   | <span data-ttu-id="cdfb8-133">相對於圖形，會建立陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="cdfb8-134">drawingRelative</span><span class="sxs-lookup"><span data-stu-id="cdfb8-134">drawingRelative</span></span> | <span data-ttu-id="cdfb8-135">相對於繪圖，會建立陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="cdfb8-136">浮雕</span><span class="sxs-lookup"><span data-stu-id="cdfb8-136">emboss</span></span>          | <span data-ttu-id="cdfb8-137">陰影具有浮凸外觀。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="cdfb8-138">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="cdfb8-139">**範例**</span><span class="sxs-lookup"><span data-stu-id="cdfb8-139">**Example**</span></span>

<span data-ttu-id="cdfb8-140">以第二個陰影綠色和位移5點向下和向右點建立雙重陰影。</span><span class="sxs-lookup"><span data-stu-id="cdfb8-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 