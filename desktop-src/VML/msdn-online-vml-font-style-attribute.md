---
title: VML Font-Style 屬性
description: VML Font-Style 屬性
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f4fc2f299d78c3ccd8b194b8506cfce07abceb7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023550"
---
# <a name="vml-font-style-attribute"></a><span data-ttu-id="bff49-103">VML Font-Style 屬性</span><span class="sxs-lookup"><span data-stu-id="bff49-103">VML Font-Style Attribute</span></span>

<span data-ttu-id="bff49-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="bff49-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bff49-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="bff49-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bff49-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="bff49-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bff49-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="bff49-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bff49-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="bff49-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bff49-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="bff49-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bff49-110">定義字型的斜線量。</span><span class="sxs-lookup"><span data-stu-id="bff49-110">Defines the amount of slant for a font.</span></span> <span data-ttu-id="bff49-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bff49-111">Read/write.</span></span> <span data-ttu-id="bff49-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="bff49-112">**String**.</span></span>

<span data-ttu-id="bff49-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="bff49-113">**Applies To**</span></span>

[<span data-ttu-id="bff49-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="bff49-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="bff49-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="bff49-115">**Tag Syntax**</span></span>

<span data-ttu-id="bff49-116"><v： *element* style = "字型樣式： *運算式* " ></span><span class="sxs-lookup"><span data-stu-id="bff49-116"><v: *element* style="font-style: *expression* "></span></span>

<span data-ttu-id="bff49-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="bff49-117">**Script Syntax**</span></span>

<span data-ttu-id="bff49-118"> fontstyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="bff49-118">*element* .style.fontstyle="*expression*"</span></span>

<span data-ttu-id="bff49-119">*運算式* =\*\* fontstyle</span><span class="sxs-lookup"><span data-stu-id="bff49-119">*expression*=*element*.style.fontstyle</span></span>

<span data-ttu-id="bff49-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="bff49-120">**Remarks**</span></span>

<span data-ttu-id="bff49-121">值如下：</span><span class="sxs-lookup"><span data-stu-id="bff49-121">The values are:</span></span>

-   <span data-ttu-id="bff49-122">一般 (預設) </span><span class="sxs-lookup"><span data-stu-id="bff49-122">normal (default)</span></span>
-   <span data-ttu-id="bff49-123">斜</span><span class="sxs-lookup"><span data-stu-id="bff49-123">oblique</span></span>
-   <span data-ttu-id="bff49-124">斜體</span><span class="sxs-lookup"><span data-stu-id="bff49-124">italic</span></span>

<span data-ttu-id="bff49-125">大部分的瀏覽器會以斜體呈現傾斜。</span><span class="sxs-lookup"><span data-stu-id="bff49-125">Most browsers render oblique as italic.</span></span> <span data-ttu-id="bff49-126">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="bff49-126">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="bff49-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="bff49-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="bff49-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="bff49-128">**Example**</span></span>

<span data-ttu-id="bff49-129">字型為斜體 (傾斜) 。</span><span class="sxs-lookup"><span data-stu-id="bff49-129">The font is italic (slanted).</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 