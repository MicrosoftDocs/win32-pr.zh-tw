---
title: VML StrokeWeight 屬性
description: VML StrokeWeight 屬性
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682550"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="63035-103">VML StrokeWeight 屬性</span><span class="sxs-lookup"><span data-stu-id="63035-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="63035-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="63035-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63035-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="63035-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63035-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="63035-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63035-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="63035-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63035-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="63035-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63035-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="63035-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63035-110">定義筆觸形狀路徑的筆刷厚度。</span><span class="sxs-lookup"><span data-stu-id="63035-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="63035-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="63035-111">Read/write.</span></span> <span data-ttu-id="63035-112">**VGLength**。</span><span class="sxs-lookup"><span data-stu-id="63035-112">**VGLength**.</span></span>

<span data-ttu-id="63035-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="63035-113">**Applies To**</span></span>

[<span data-ttu-id="63035-114">形狀</span><span class="sxs-lookup"><span data-stu-id="63035-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="63035-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="63035-115">**Tag Syntax**</span></span>

<span data-ttu-id="63035-116"><v： *element* strokeweight = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="63035-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="63035-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="63035-117">**Script Syntax**</span></span>

<span data-ttu-id="63035-118"> strokeweight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="63035-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="63035-119">*運算式* =\*\* strokeweight</span><span class="sxs-lookup"><span data-stu-id="63035-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="63035-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="63035-120">**Remarks**</span></span>

<span data-ttu-id="63035-121">此值會從 **Stroke** 元素的 **權數** 屬性複製。</span><span class="sxs-lookup"><span data-stu-id="63035-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="63035-122">如果指定了數位，但未加入任何單位，則預設度量單位是 Emu。</span><span class="sxs-lookup"><span data-stu-id="63035-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="63035-123">如果未指定任何值，預設值為1圖元 (1px) 。</span><span class="sxs-lookup"><span data-stu-id="63035-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="63035-124">不過，針對腳本，預設測量單位是以點為單位。</span><span class="sxs-lookup"><span data-stu-id="63035-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="63035-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="63035-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="63035-126">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="63035-126">**See Also**</span></span>

<span data-ttu-id="63035-127">[Stroke](msdn-online-vml-stroke-element.md)、 [IVgLength](msdn-online-vml-vglength.md)、 [單位](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="63035-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="63035-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="63035-128">**Example**</span></span>

<span data-ttu-id="63035-129">圖形的筆觸粗細為1點。</span><span class="sxs-lookup"><span data-stu-id="63035-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="63035-130">[StrokeWeight 屬性範例](/previous-versions/bb264095(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="63035-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="63035-131"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="63035-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 