---
title: VML V 文字對齊屬性
description: VML V 文字對齊屬性
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933358"
---
# <a name="vml-v-text-align-attribute"></a><span data-ttu-id="145a0-103">VML V 文字對齊屬性</span><span class="sxs-lookup"><span data-stu-id="145a0-103">VML V-Text-Align Attribute</span></span>

<span data-ttu-id="145a0-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="145a0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="145a0-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="145a0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="145a0-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="145a0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="145a0-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="145a0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="145a0-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="145a0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="145a0-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="145a0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="145a0-110">定義文字的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="145a0-110">Defines the alignment of text.</span></span> <span data-ttu-id="145a0-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="145a0-111">Read/write.</span></span> <span data-ttu-id="145a0-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="145a0-112">**String**.</span></span>

<span data-ttu-id="145a0-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="145a0-113">**Applies To**</span></span>

[<span data-ttu-id="145a0-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="145a0-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="145a0-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="145a0-115">**Tag Syntax**</span></span>

<span data-ttu-id="145a0-116"><v： *element* style = "v-text align： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="145a0-116"><v: *element* style="v-text-align: *expression* "></span></span>

<span data-ttu-id="145a0-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="145a0-117">**Script Syntax**</span></span>

<span data-ttu-id="145a0-118">*element* 。 v-text-align = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="145a0-118">*element* .style.v-text-align="*expression*"</span></span>

<span data-ttu-id="145a0-119">*運算式* =*元素*。 v-文字對齊</span><span class="sxs-lookup"><span data-stu-id="145a0-119">*expression*=*element*.style.v-text-align</span></span>

<span data-ttu-id="145a0-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="145a0-120">**Remarks**</span></span>

<span data-ttu-id="145a0-121">數值包括：</span><span class="sxs-lookup"><span data-stu-id="145a0-121">Values include:</span></span>

-   <span data-ttu-id="145a0-122">**左方** (預設) </span><span class="sxs-lookup"><span data-stu-id="145a0-122">**left** (default)</span></span>
-   <span data-ttu-id="145a0-123">**對**</span><span class="sxs-lookup"><span data-stu-id="145a0-123">**right**</span></span>
-   <span data-ttu-id="145a0-124">**中心**</span><span class="sxs-lookup"><span data-stu-id="145a0-124">**center**</span></span>
-   <span data-ttu-id="145a0-125">**證明**</span><span class="sxs-lookup"><span data-stu-id="145a0-125">**justify**</span></span>
-   <span data-ttu-id="145a0-126">**字母-調整**</span><span class="sxs-lookup"><span data-stu-id="145a0-126">**letter-justify**</span></span>
-   <span data-ttu-id="145a0-127">**延展-調整**</span><span class="sxs-lookup"><span data-stu-id="145a0-127">**stretch-justify**</span></span>

<span data-ttu-id="145a0-128">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="145a0-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="145a0-129">**範例**</span><span class="sxs-lookup"><span data-stu-id="145a0-129">**Example**</span></span>

<span data-ttu-id="145a0-130">系統會將文字縮小以符合路徑，但是會在每個字母之間放置額外的空間。</span><span class="sxs-lookup"><span data-stu-id="145a0-130">The text will be stretched out to fit the path, but the extra space will be put between each letter.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 