---
title: VML Text-Decoration 屬性
description: VML Text-Decoration 屬性
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933308"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="77cbe-103">VML Text-Decoration 屬性</span><span class="sxs-lookup"><span data-stu-id="77cbe-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="77cbe-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="77cbe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77cbe-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="77cbe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77cbe-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="77cbe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77cbe-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="77cbe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77cbe-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="77cbe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77cbe-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="77cbe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77cbe-110">定義文字裝飾的樣式。</span><span class="sxs-lookup"><span data-stu-id="77cbe-110">Defines the style of text decoration.</span></span> <span data-ttu-id="77cbe-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="77cbe-111">Read/write.</span></span> <span data-ttu-id="77cbe-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="77cbe-112">**String**.</span></span>

<span data-ttu-id="77cbe-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="77cbe-113">**Applies To**</span></span>

[<span data-ttu-id="77cbe-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="77cbe-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="77cbe-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="77cbe-115">**Tag Syntax**</span></span>

<span data-ttu-id="77cbe-116"><v： *element* style = "文字裝飾： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="77cbe-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="77cbe-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="77cbe-117">**Script Syntax**</span></span>

<span data-ttu-id="77cbe-118"> textdecoration = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="77cbe-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="77cbe-119">*運算式* =\*\* textdecoration</span><span class="sxs-lookup"><span data-stu-id="77cbe-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="77cbe-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="77cbe-120">**Remarks**</span></span>

<span data-ttu-id="77cbe-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="77cbe-121">Values include:</span></span>

-   <span data-ttu-id="77cbe-122">無 (預設) </span><span class="sxs-lookup"><span data-stu-id="77cbe-122">none (default)</span></span>
-   <span data-ttu-id="77cbe-123">底線</span><span class="sxs-lookup"><span data-stu-id="77cbe-123">underline</span></span>
-   <span data-ttu-id="77cbe-124">頂線</span><span class="sxs-lookup"><span data-stu-id="77cbe-124">overline</span></span>
-   <span data-ttu-id="77cbe-125">逐行</span><span class="sxs-lookup"><span data-stu-id="77cbe-125">line-through</span></span>
-   <span data-ttu-id="77cbe-126">blink</span><span class="sxs-lookup"><span data-stu-id="77cbe-126">blink</span></span>

<span data-ttu-id="77cbe-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="77cbe-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="77cbe-128">**範例**</span><span class="sxs-lookup"><span data-stu-id="77cbe-128">**Example**</span></span>

<span data-ttu-id="77cbe-129">文字會加上底線。</span><span class="sxs-lookup"><span data-stu-id="77cbe-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 