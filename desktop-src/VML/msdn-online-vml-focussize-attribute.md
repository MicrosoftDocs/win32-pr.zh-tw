---
title: VML FocusSize 屬性
description: VML FocusSize 屬性
ms.assetid: 6ca5af2c-3064-423f-a7bb-202f23bf95da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8149973932e9601be2caa0306eefcec08951b238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024069"
---
# <a name="vml-focussize-attribute"></a><span data-ttu-id="1c87f-103">VML FocusSize 屬性</span><span class="sxs-lookup"><span data-stu-id="1c87f-103">VML FocusSize Attribute</span></span>

<span data-ttu-id="1c87f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="1c87f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1c87f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="1c87f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1c87f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="1c87f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1c87f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="1c87f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1c87f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="1c87f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1c87f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="1c87f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1c87f-110">定義星形填滿的焦點大小。</span><span class="sxs-lookup"><span data-stu-id="1c87f-110">Defines the focus size for radial fills.</span></span> <span data-ttu-id="1c87f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c87f-111">Read/write.</span></span> <span data-ttu-id="1c87f-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="1c87f-112">**VgVector2D**.</span></span>

<span data-ttu-id="1c87f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="1c87f-113">**Applies To**</span></span>

[<span data-ttu-id="1c87f-114">填滿</span><span class="sxs-lookup"><span data-stu-id="1c87f-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1c87f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="1c87f-115">**Tag Syntax**</span></span>

<span data-ttu-id="1c87f-116"><v： *element* focussize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1c87f-116"><v: *element* focussize=" *expression* "></span></span>

<span data-ttu-id="1c87f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="1c87f-117">**Script Syntax**</span></span>

<span data-ttu-id="1c87f-118"> focussize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1c87f-118">*element* .focussize="*expression*"</span></span>

<span data-ttu-id="1c87f-119">*運算式* =\*\* focussize</span><span class="sxs-lookup"><span data-stu-id="1c87f-119">*expression*=*element*.focussize</span></span>

<span data-ttu-id="1c87f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="1c87f-120">**Remarks**</span></span>

<span data-ttu-id="1c87f-121">這些值是圖形寬度和高度的分數。</span><span class="sxs-lookup"><span data-stu-id="1c87f-121">The values are fractions of the width and height of the shape.</span></span> <span data-ttu-id="1c87f-122">第一個是圖形右邊緣填滿的百分比，而第二個則是圖形底部填滿的百分比。</span><span class="sxs-lookup"><span data-stu-id="1c87f-122">The first is a percentage of the fill to the right edge of the shape and the second is a percentage of the fill to the bottom of the shape.</span></span> <span data-ttu-id="1c87f-123">預設值為 0,0。</span><span class="sxs-lookup"><span data-stu-id="1c87f-123">The default value is 0,0.</span></span> <span data-ttu-id="1c87f-124">**FocusSize** 值為100%、100% 且 **FocusPosition** 為0，0會讓 Color2 完全在 blend 中佔據。</span><span class="sxs-lookup"><span data-stu-id="1c87f-124">A **FocusSize** value of 100%,100% and a **FocusPosition** of 0,0 would make Color2 dominate the blend completely.</span></span> <span data-ttu-id="1c87f-125">如果有大約10% 的小值，建議將10% 用於平衡的混合。</span><span class="sxs-lookup"><span data-stu-id="1c87f-125">Small values of around 10%,10% are recommended for balanced blends.</span></span>

<span data-ttu-id="1c87f-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="1c87f-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="1c87f-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="1c87f-127">**Example**</span></span>

<span data-ttu-id="1c87f-128">星形填滿會在中間以藍色開始建立 blend，並在所有四個邊緣變成紅色。</span><span class="sxs-lookup"><span data-stu-id="1c87f-128">The radial fill will create a blend starting in the center as blue and becoming red on all four edges.</span></span> <span data-ttu-id="1c87f-129">Blend 的中心是由 **FocusPosition** 所定義，而內部開始色彩的大小是由 **FocusSize** 所決定。</span><span class="sxs-lookup"><span data-stu-id="1c87f-129">The center of the blend is defined by **FocusPosition** and the size of the inner starting color is determined by **FocusSize**.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l1,200, 200,200, 200,1 x e">
   <v:fill type="gradientradial" color="red" color2="blue"
   focusposition=".5,.5" focussize=".1,.1"/>
   </v:shape>
```



 

 