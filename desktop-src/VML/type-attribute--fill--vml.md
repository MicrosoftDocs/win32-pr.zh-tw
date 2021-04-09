---
title: 'Type 屬性 (Fill)  (VML) '
description: 'Type 屬性 (Fill)  (VML) '
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682734"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="8be22-103">Type 屬性 (Fill)  (VML) </span><span class="sxs-lookup"><span data-stu-id="8be22-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8be22-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8be22-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8be22-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8be22-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8be22-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8be22-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8be22-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8be22-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8be22-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8be22-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8be22-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8be22-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8be22-110">決定填滿的型別。</span><span class="sxs-lookup"><span data-stu-id="8be22-110">Determines the type of fill.</span></span> <span data-ttu-id="8be22-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8be22-111">Read/write.</span></span> <span data-ttu-id="8be22-112">**VgFillType**。</span><span class="sxs-lookup"><span data-stu-id="8be22-112">**VgFillType**.</span></span>

<span data-ttu-id="8be22-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8be22-113">**Applies To**</span></span>

[<span data-ttu-id="8be22-114">填滿</span><span class="sxs-lookup"><span data-stu-id="8be22-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8be22-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8be22-115">**Tag Syntax**</span></span>

<span data-ttu-id="8be22-116"><v： *element* type = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8be22-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="8be22-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8be22-117">**Script Syntax**</span></span>

<span data-ttu-id="8be22-118">*element* 。 type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8be22-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="8be22-119">*運算式* =*元素*。類型</span><span class="sxs-lookup"><span data-stu-id="8be22-119">*expression*=*element*.type</span></span>

<span data-ttu-id="8be22-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8be22-120">**Remarks**</span></span>

<span data-ttu-id="8be22-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="8be22-121">Values include:</span></span>



| <span data-ttu-id="8be22-122">類型</span><span class="sxs-lookup"><span data-stu-id="8be22-122">Type</span></span>           | <span data-ttu-id="8be22-123">Description</span><span class="sxs-lookup"><span data-stu-id="8be22-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8be22-124">固體</span><span class="sxs-lookup"><span data-stu-id="8be22-124">solid</span></span>          | <span data-ttu-id="8be22-125">填滿模式是實心。</span><span class="sxs-lookup"><span data-stu-id="8be22-125">The fill pattern is solid.</span></span> <span data-ttu-id="8be22-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="8be22-126">Default.</span></span>                                     |
| <span data-ttu-id="8be22-127">漸層</span><span class="sxs-lookup"><span data-stu-id="8be22-127">gradient</span></span>       | <span data-ttu-id="8be22-128">填滿色彩會以線性漸層（從下到上）混合在一起。</span><span class="sxs-lookup"><span data-stu-id="8be22-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="8be22-129">gradientradial</span><span class="sxs-lookup"><span data-stu-id="8be22-129">gradientradial</span></span> | <span data-ttu-id="8be22-130">填滿色彩會在放射狀漸層中一起混合。</span><span class="sxs-lookup"><span data-stu-id="8be22-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="8be22-131">磚</span><span class="sxs-lookup"><span data-stu-id="8be22-131">tile</span></span>           | <span data-ttu-id="8be22-132">填滿影像會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="8be22-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="8be22-133">模式</span><span class="sxs-lookup"><span data-stu-id="8be22-133">pattern</span></span>        | <span data-ttu-id="8be22-134">影像可用來建立使用填滿色彩的模式。</span><span class="sxs-lookup"><span data-stu-id="8be22-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="8be22-135">框架</span><span class="sxs-lookup"><span data-stu-id="8be22-135">frame</span></span>          | <span data-ttu-id="8be22-136">影像會伸展以填滿形狀。</span><span class="sxs-lookup"><span data-stu-id="8be22-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="8be22-137">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="8be22-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="8be22-138">**範例**</span><span class="sxs-lookup"><span data-stu-id="8be22-138">**Example**</span></span>

<span data-ttu-id="8be22-139">紅色的前景和藍色背景填滿是使用影像 myimage.gif 的模式所建立。</span><span class="sxs-lookup"><span data-stu-id="8be22-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 