---
title: VML FocusPosition 屬性
description: VML FocusPosition 屬性
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093276"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="d8513-103">VML FocusPosition 屬性</span><span class="sxs-lookup"><span data-stu-id="d8513-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="d8513-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d8513-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d8513-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d8513-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d8513-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d8513-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d8513-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d8513-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d8513-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d8513-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d8513-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d8513-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d8513-110">定義放射狀漸層的中心。</span><span class="sxs-lookup"><span data-stu-id="d8513-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="d8513-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d8513-111">Read/write.</span></span> <span data-ttu-id="d8513-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="d8513-112">**VgVector2D**.</span></span>

<span data-ttu-id="d8513-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d8513-113">**Applies To**</span></span>

[<span data-ttu-id="d8513-114">填滿</span><span class="sxs-lookup"><span data-stu-id="d8513-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="d8513-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d8513-115">**Tag Syntax**</span></span>

<span data-ttu-id="d8513-116"><v： *element* focusposition = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d8513-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="d8513-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="d8513-117">**Script Syntax**</span></span>

<span data-ttu-id="d8513-118"> focusposition = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d8513-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="d8513-119">*運算式* =\*\* focusposition</span><span class="sxs-lookup"><span data-stu-id="d8513-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="d8513-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="d8513-120">**Remarks**</span></span>

<span data-ttu-id="d8513-121">指定中央 positionfor 放射狀漸層。</span><span class="sxs-lookup"><span data-stu-id="d8513-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="d8513-122">向量是圖形寬度和高度的一小部分。</span><span class="sxs-lookup"><span data-stu-id="d8513-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="d8513-123">第一個是左邊緣填滿的百分比;第二個是填滿至頂端的百分比。</span><span class="sxs-lookup"><span data-stu-id="d8513-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="d8513-124">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="d8513-124">The default value is 0,0.</span></span> <span data-ttu-id="d8513-125">若要在圖形中央放置星形填滿，請使用 50% 50% 的值。</span><span class="sxs-lookup"><span data-stu-id="d8513-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="d8513-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="d8513-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d8513-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="d8513-127">**Example**</span></span>

<span data-ttu-id="d8513-128">星形填滿將會置中，如此一來，藍色將會從中央開始，並從外進入，並在到達外緣和角落時逐漸變更為紅色。</span><span class="sxs-lookup"><span data-stu-id="d8513-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 