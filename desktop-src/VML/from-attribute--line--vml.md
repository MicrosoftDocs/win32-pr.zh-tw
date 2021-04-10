---
title: 'From 屬性 (行)  (VML) '
description: 'From 屬性 (行)  (VML) '
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683034"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="7a0f4-103">From 屬性 (行)  (VML) </span><span class="sxs-lookup"><span data-stu-id="7a0f4-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="7a0f4-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7a0f4-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7a0f4-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7a0f4-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7a0f4-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7a0f4-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7a0f4-110">定義線條的起點。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-110">Defines the starting point of a line.</span></span> <span data-ttu-id="7a0f4-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7a0f4-111">Read/write.</span></span> <span data-ttu-id="7a0f4-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-112">**VgVector2D**.</span></span>

<span data-ttu-id="7a0f4-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7a0f4-113">**Applies To**</span></span>

[<span data-ttu-id="7a0f4-114">線條</span><span class="sxs-lookup"><span data-stu-id="7a0f4-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="7a0f4-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7a0f4-115">**Tag Syntax**</span></span>

<span data-ttu-id="7a0f4-116"><v： *element* from = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7a0f4-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="7a0f4-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="7a0f4-117">**Script Syntax**</span></span>

<span data-ttu-id="7a0f4-118">*element* 。 from = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7a0f4-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="7a0f4-119">*運算式* =*元素*。從</span><span class="sxs-lookup"><span data-stu-id="7a0f4-119">*expression*=*element*.from</span></span>

<span data-ttu-id="7a0f4-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="7a0f4-120">**Remarks**</span></span>

<span data-ttu-id="7a0f4-121">在父元素的座標空間中，定義線條的起點。如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="7a0f4-122">預設值為0，0。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-122">Default is 0,0.</span></span>

<span data-ttu-id="7a0f4-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="7a0f4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7a0f4-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="7a0f4-124">**Example**</span></span>

<span data-ttu-id="7a0f4-125">該行從位置10點向下，而10指向父空間左上角的右邊。</span><span class="sxs-lookup"><span data-stu-id="7a0f4-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 