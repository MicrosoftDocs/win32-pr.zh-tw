---
title: VML V 文字間距屬性
description: VML V 文字間距屬性
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933448"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="632dc-103">VML V 文字間距屬性</span><span class="sxs-lookup"><span data-stu-id="632dc-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="632dc-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="632dc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="632dc-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="632dc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="632dc-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="632dc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="632dc-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="632dc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="632dc-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="632dc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="632dc-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="632dc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="632dc-110">決定是否開啟字偶間距調整。</span><span class="sxs-lookup"><span data-stu-id="632dc-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="632dc-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="632dc-111">Read/write.</span></span> <span data-ttu-id="632dc-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="632dc-112">**VgTriState**.</span></span>

<span data-ttu-id="632dc-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="632dc-113">**Applies To**</span></span>

[<span data-ttu-id="632dc-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="632dc-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="632dc-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="632dc-115">**Tag Syntax**</span></span>

<span data-ttu-id="632dc-116"><v： *element* style = "v-text-字偶間距： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="632dc-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="632dc-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="632dc-117">**Script Syntax**</span></span>

<span data-ttu-id="632dc-118"> node.js-text-字偶間距 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="632dc-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="632dc-119">*運算式* =*元素*. 樣式。 v 文字間距</span><span class="sxs-lookup"><span data-stu-id="632dc-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="632dc-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="632dc-120">**Remarks**</span></span>

<span data-ttu-id="632dc-121">若 **為 True**，則會開啟字偶間距。</span><span class="sxs-lookup"><span data-stu-id="632dc-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="632dc-122">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="632dc-122">The default is **False**.</span></span> <span data-ttu-id="632dc-123">字偶間距會移除特定字母組之間的空格，以彌補不平均的 letterforms。</span><span class="sxs-lookup"><span data-stu-id="632dc-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="632dc-124">例如，如果開啟字偶間距調整，則會移除大寫 "T" 和小寫 "i" 之間的額外空間。</span><span class="sxs-lookup"><span data-stu-id="632dc-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="632dc-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="632dc-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="632dc-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="632dc-126">**Example**</span></span>

<span data-ttu-id="632dc-127">已開啟字偶間距。</span><span class="sxs-lookup"><span data-stu-id="632dc-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 