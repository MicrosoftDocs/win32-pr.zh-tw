---
title: VML Path 屬性
description: VML Path 屬性
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842695"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="19bd7-103">VML Path 屬性</span><span class="sxs-lookup"><span data-stu-id="19bd7-103">VML Path Attribute</span></span>

<span data-ttu-id="19bd7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="19bd7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="19bd7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="19bd7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="19bd7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="19bd7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="19bd7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="19bd7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="19bd7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="19bd7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="19bd7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="19bd7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="19bd7-110">指定組成圖形邊緣的線。</span><span class="sxs-lookup"><span data-stu-id="19bd7-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="19bd7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="19bd7-111">Read/write.</span></span> <span data-ttu-id="19bd7-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="19bd7-112">**String**.</span></span>

<span data-ttu-id="19bd7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="19bd7-113">**Applies To**</span></span>

[<span data-ttu-id="19bd7-114">形狀</span><span class="sxs-lookup"><span data-stu-id="19bd7-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="19bd7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="19bd7-115">**Tag Syntax**</span></span>

<span data-ttu-id="19bd7-116"><v： *element* path = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="19bd7-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="19bd7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="19bd7-117">**Script Syntax**</span></span>

<span data-ttu-id="19bd7-118">*元素* 。 path = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="19bd7-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="19bd7-119">*運算式* =*元素*。路徑</span><span class="sxs-lookup"><span data-stu-id="19bd7-119">*expression*=*element*.path</span></span>

<span data-ttu-id="19bd7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="19bd7-120">**Remarks**</span></span>

<span data-ttu-id="19bd7-121">如果圖形包含 [path](msdn-online-vml-path-element.md) 元素，path 元素的 path 命令會優先于 shape 屬性值。</span><span class="sxs-lookup"><span data-stu-id="19bd7-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="19bd7-122">如需路徑所用命令集的詳細資訊，請參閱 **Path** 元素主題。</span><span class="sxs-lookup"><span data-stu-id="19bd7-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="19bd7-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="19bd7-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="19bd7-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="19bd7-124">**Example**</span></span>

<span data-ttu-id="19bd7-125">封閉的正方形路徑是在 path 屬性的字串中定義。</span><span class="sxs-lookup"><span data-stu-id="19bd7-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="19bd7-126">初始點是使用用於 `m` **moveto** 命令的 () （1，1），並使用 `l` (字母 "L"，用於命令 **lineto**) 從起始位置 (1，1) 至其他三個點，順序 (： 1200; 200200;200、1。</span><span class="sxs-lookup"><span data-stu-id="19bd7-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="19bd7-127">行已關閉， `x` (**關閉**) ，並以 `e` (**end**) 結束。</span><span class="sxs-lookup"><span data-stu-id="19bd7-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="19bd7-128">請注意，座標是在相對座標空間中提供，而實際大小是由 **寬度** 和 **高度** 所決定。</span><span class="sxs-lookup"><span data-stu-id="19bd7-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="19bd7-129">[路徑屬性範例](/previous-versions/bb264089(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="19bd7-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="19bd7-130"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="19bd7-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 