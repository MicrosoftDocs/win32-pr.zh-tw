---
title: VML EndArrowWidth 屬性
description: VML EndArrowWidth 屬性
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683071"
---
# <a name="vml-endarrowwidth-attribute"></a><span data-ttu-id="eba22-103">VML EndArrowWidth 屬性</span><span class="sxs-lookup"><span data-stu-id="eba22-103">VML EndArrowWidth Attribute</span></span>

<span data-ttu-id="eba22-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eba22-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eba22-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eba22-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eba22-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eba22-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eba22-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eba22-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eba22-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eba22-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eba22-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eba22-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eba22-110">定義線條結尾的箭頭寬度。</span><span class="sxs-lookup"><span data-stu-id="eba22-110">Defines an arrowhead width for the end of a line.</span></span> <span data-ttu-id="eba22-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eba22-111">Read/write.</span></span> <span data-ttu-id="eba22-112">**VgArrowheadWidth**。</span><span class="sxs-lookup"><span data-stu-id="eba22-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="eba22-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eba22-113">**Applies To**</span></span>

[<span data-ttu-id="eba22-114">中風</span><span class="sxs-lookup"><span data-stu-id="eba22-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="eba22-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eba22-115">**Tag Syntax**</span></span>

<span data-ttu-id="eba22-116"><v： *element* endarrowwidth = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eba22-116"><v: *element* endarrowwidth=" *expression* "></span></span>

<span data-ttu-id="eba22-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eba22-117">**Script Syntax**</span></span>

<span data-ttu-id="eba22-118"> endarrowwidth = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eba22-118">*element* .endarrowwidth="*expression*"</span></span>

<span data-ttu-id="eba22-119">*運算式* =\*\* endarrowwidth</span><span class="sxs-lookup"><span data-stu-id="eba22-119">*expression*=*element*.endarrowwidth</span></span>

<span data-ttu-id="eba22-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eba22-120">**Remarks**</span></span>

<span data-ttu-id="eba22-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="eba22-121">Values include:</span></span>

-   <span data-ttu-id="eba22-122">狹窄</span><span class="sxs-lookup"><span data-stu-id="eba22-122">Narrow</span></span>
-   <span data-ttu-id="eba22-123">中 (預設)</span><span class="sxs-lookup"><span data-stu-id="eba22-123">Medium (default)</span></span>
-   <span data-ttu-id="eba22-124">寬</span><span class="sxs-lookup"><span data-stu-id="eba22-124">Wide</span></span>

<span data-ttu-id="eba22-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="eba22-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="eba22-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="eba22-126">**Example**</span></span>

<span data-ttu-id="eba22-127">在筆劃末端以寬型的箭頭繪製線條。</span><span class="sxs-lookup"><span data-stu-id="eba22-127">A line is drawn with a wide classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 