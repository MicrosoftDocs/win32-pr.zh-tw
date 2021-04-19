---
title: VML Control1 屬性
description: VML Control1 屬性
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967895"
---
# <a name="vml-control1-attribute"></a><span data-ttu-id="158dd-103">VML Control1 屬性</span><span class="sxs-lookup"><span data-stu-id="158dd-103">VML Control1 Attribute</span></span>

<span data-ttu-id="158dd-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="158dd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="158dd-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="158dd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="158dd-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="158dd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="158dd-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="158dd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="158dd-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="158dd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="158dd-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="158dd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="158dd-110">定義貝茲曲線的第一個控制點。</span><span class="sxs-lookup"><span data-stu-id="158dd-110">Defines the first control point of a bezier curve.</span></span> <span data-ttu-id="158dd-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="158dd-111">Read/write.</span></span> <span data-ttu-id="158dd-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="158dd-112">**VgVector2D**.</span></span>

<span data-ttu-id="158dd-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="158dd-113">**Applies To**</span></span>

[<span data-ttu-id="158dd-114">曲線</span><span class="sxs-lookup"><span data-stu-id="158dd-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="158dd-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="158dd-115">**Tag Syntax**</span></span>

<span data-ttu-id="158dd-116"><v： *element* control1 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="158dd-116"><v: *element* control1=" *expression* "></span></span>

<span data-ttu-id="158dd-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="158dd-117">**Script Syntax**</span></span>

<span data-ttu-id="158dd-118"> control1 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="158dd-118">*element* .control1="*expression*"</span></span>

<span data-ttu-id="158dd-119">*運算式* =\*\* control1</span><span class="sxs-lookup"><span data-stu-id="158dd-119">*expression*=*element*.control1</span></span>

<span data-ttu-id="158dd-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="158dd-120">**Remarks**</span></span>

<span data-ttu-id="158dd-121">在父元素的座標空間中，定義三次方貝茲曲線的第一個控制點。如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。</span><span class="sxs-lookup"><span data-stu-id="158dd-121">Defines the first control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="158dd-122">預設值為10、10。</span><span class="sxs-lookup"><span data-stu-id="158dd-122">Default is 10,10.</span></span>

<span data-ttu-id="158dd-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="158dd-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="158dd-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="158dd-124">**Example**</span></span>

<span data-ttu-id="158dd-125">曲線是微笑的。</span><span class="sxs-lookup"><span data-stu-id="158dd-125">The curve is smiling.</span></span> <span data-ttu-id="158dd-126">它會從左邊開始，並在右側結束。</span><span class="sxs-lookup"><span data-stu-id="158dd-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="158dd-127">這兩個控制點的位置是以拉下曲線來提供笑臉的外觀。</span><span class="sxs-lookup"><span data-stu-id="158dd-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 