---
title: VML StrokeColor 屬性
description: VML StrokeColor 屬性
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023636"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="def7f-103">VML StrokeColor 屬性</span><span class="sxs-lookup"><span data-stu-id="def7f-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="def7f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="def7f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="def7f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="def7f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="def7f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="def7f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="def7f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="def7f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="def7f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="def7f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="def7f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="def7f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="def7f-110">定義筆觸形狀路徑的筆刷色彩。</span><span class="sxs-lookup"><span data-stu-id="def7f-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="def7f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="def7f-111">Read/write.</span></span> <span data-ttu-id="def7f-112">[IVgColor](msdn-online-vml-ivgcolor.md)。</span><span class="sxs-lookup"><span data-stu-id="def7f-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="def7f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="def7f-113">**Applies To**</span></span>

[<span data-ttu-id="def7f-114">形狀</span><span class="sxs-lookup"><span data-stu-id="def7f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="def7f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="def7f-115">**Tag Syntax**</span></span>

<span data-ttu-id="def7f-116"><v： *element* strokecolor = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="def7f-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="def7f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="def7f-117">**Script Syntax**</span></span>

<span data-ttu-id="def7f-118"> strokecolor = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="def7f-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="def7f-119">*運算式* =\*\* strokecolor</span><span class="sxs-lookup"><span data-stu-id="def7f-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="def7f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="def7f-120">**Remarks**</span></span>

<span data-ttu-id="def7f-121">此值會從 [Stroke](msdn-online-vml-stroke-element.md)元素的 **Color** 屬性複製。</span><span class="sxs-lookup"><span data-stu-id="def7f-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="def7f-122">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="def7f-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="def7f-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="def7f-123">**Example**</span></span>

<span data-ttu-id="def7f-124">矩形筆劃的色彩為紅色。</span><span class="sxs-lookup"><span data-stu-id="def7f-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="def7f-125">[StrokeColor 屬性範例](/previous-versions/bb264093(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="def7f-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="def7f-126"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="def7f-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 