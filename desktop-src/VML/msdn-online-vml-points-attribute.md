---
title: VML 點屬性
description: VML 點屬性
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023571"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="b348d-103">VML 點屬性</span><span class="sxs-lookup"><span data-stu-id="b348d-103">VML Points Attribute</span></span>

<span data-ttu-id="b348d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b348d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b348d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b348d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b348d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b348d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b348d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b348d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b348d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b348d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b348d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b348d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b348d-110">定義組成折線的一組點。</span><span class="sxs-lookup"><span data-stu-id="b348d-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="b348d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b348d-111">Read/write.</span></span> <span data-ttu-id="b348d-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="b348d-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="b348d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b348d-113">**Applies To**</span></span>

[<span data-ttu-id="b348d-114">聚合線條</span><span class="sxs-lookup"><span data-stu-id="b348d-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="b348d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b348d-115">**Tag Syntax**</span></span>

<span data-ttu-id="b348d-116"><v： *element* points = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b348d-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="b348d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b348d-117">**Script Syntax**</span></span>

<span data-ttu-id="b348d-118">*元素* 。 points = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="b348d-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="b348d-119">*運算式* =*元素*。點</span><span class="sxs-lookup"><span data-stu-id="b348d-119">*expression*=*element*.points</span></span>

<span data-ttu-id="b348d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b348d-120">**Remarks**</span></span>

<span data-ttu-id="b348d-121">定義一組由一連串的點組成的直線線段。</span><span class="sxs-lookup"><span data-stu-id="b348d-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="b348d-122">如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。</span><span class="sxs-lookup"><span data-stu-id="b348d-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="b348d-123">預設值為 "0，0 10，10"。</span><span class="sxs-lookup"><span data-stu-id="b348d-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="b348d-124">請注意，逗號並非必要，但可讓您更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="b348d-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="b348d-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b348d-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="b348d-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="b348d-126">**Example**</span></span>

<span data-ttu-id="b348d-127">聚合線條從點10、10開始到100100，並以值點開始。</span><span class="sxs-lookup"><span data-stu-id="b348d-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 