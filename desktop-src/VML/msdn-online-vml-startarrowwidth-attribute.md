---
title: VML StartArrowWidth 屬性
description: VML StartArrowWidth 屬性
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682667"
---
# <a name="vml-startarrowwidth-attribute"></a><span data-ttu-id="ba59d-103">VML StartArrowWidth 屬性</span><span class="sxs-lookup"><span data-stu-id="ba59d-103">VML StartArrowWidth Attribute</span></span>

<span data-ttu-id="ba59d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ba59d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ba59d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ba59d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ba59d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ba59d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ba59d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ba59d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ba59d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ba59d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ba59d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ba59d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ba59d-110">定義線條開頭的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="ba59d-110">Defines the arrowhead width for the start of a line.</span></span> <span data-ttu-id="ba59d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ba59d-111">Read/write.</span></span> <span data-ttu-id="ba59d-112">**VgArrowheadWidth**。</span><span class="sxs-lookup"><span data-stu-id="ba59d-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="ba59d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ba59d-113">**Applies To**</span></span>

[<span data-ttu-id="ba59d-114">中風</span><span class="sxs-lookup"><span data-stu-id="ba59d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ba59d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ba59d-115">**Tag Syntax**</span></span>

<span data-ttu-id="ba59d-116"><v： *element* startarrowwidth = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ba59d-116"><v: *element* startarrowwidth=" *expression* "></span></span>

<span data-ttu-id="ba59d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ba59d-117">**Script Syntax**</span></span>

<span data-ttu-id="ba59d-118"> startarrowwidth = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ba59d-118">*element* .startarrowwidth="*expression*"</span></span>

<span data-ttu-id="ba59d-119">*運算式* =\*\* startarrowwidth</span><span class="sxs-lookup"><span data-stu-id="ba59d-119">*expression*=*element*.startarrowwidth</span></span>

<span data-ttu-id="ba59d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ba59d-120">**Remarks**</span></span>

<span data-ttu-id="ba59d-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="ba59d-121">Values include:</span></span>

-   <span data-ttu-id="ba59d-122">狹窄</span><span class="sxs-lookup"><span data-stu-id="ba59d-122">Narrow</span></span>
-   <span data-ttu-id="ba59d-123">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="ba59d-123">Medium (default)</span></span>
-   <span data-ttu-id="ba59d-124">寬</span><span class="sxs-lookup"><span data-stu-id="ba59d-124">Wide</span></span>

<span data-ttu-id="ba59d-125">VML 標準屬性</span><span class="sxs-lookup"><span data-stu-id="ba59d-125">VML Standard Attribute</span></span>

<span data-ttu-id="ba59d-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="ba59d-126">**Example**</span></span>

<span data-ttu-id="ba59d-127">在筆劃的開頭，以寬型的箭頭繪製線條。</span><span class="sxs-lookup"><span data-stu-id="ba59d-127">A line is drawn with a wide classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 