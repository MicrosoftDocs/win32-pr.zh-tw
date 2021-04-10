---
title: '若要 (行的屬性)  (VML) '
description: '若要 (行的屬性)  (VML) '
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683065"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="4e5e8-103">若要 (行的屬性)  (VML) </span><span class="sxs-lookup"><span data-stu-id="4e5e8-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="4e5e8-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4e5e8-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4e5e8-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4e5e8-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4e5e8-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4e5e8-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4e5e8-110">定義線條的結束點。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-110">Defines the ending point of a line.</span></span> <span data-ttu-id="4e5e8-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="4e5e8-111">Read/write.</span></span> <span data-ttu-id="4e5e8-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-112">**VgVector2D**.</span></span>

<span data-ttu-id="4e5e8-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-113">**Applies To**</span></span>

[<span data-ttu-id="4e5e8-114">線條</span><span class="sxs-lookup"><span data-stu-id="4e5e8-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="4e5e8-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-115">**Tag Syntax**</span></span>

<span data-ttu-id="4e5e8-116"><v： *element* to = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4e5e8-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="4e5e8-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-117">**Script Syntax**</span></span>

<span data-ttu-id="4e5e8-118">*element* 。 to = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4e5e8-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="4e5e8-119">*運算式* =*元素*。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-119">*expression*=*element*.to</span></span>

<span data-ttu-id="4e5e8-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-120">**Remarks**</span></span>

<span data-ttu-id="4e5e8-121">在父元素的座標空間中，定義線條的結束點。如果父系不是 VML 元素，預設 [單位](msdn-online-vml-units.md) 為圖元 (但在中，cm、mm、pt、pc 也可以指定) 。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="4e5e8-122">預設值為10、10。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-122">Default is 10,10.</span></span>

<span data-ttu-id="4e5e8-123">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="4e5e8-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="4e5e8-124">**Example**</span></span>

<span data-ttu-id="4e5e8-125">該行會以位置100點向下和100指向父空間左上角的右邊。</span><span class="sxs-lookup"><span data-stu-id="4e5e8-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 