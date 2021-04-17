---
title: VML V-文字間距模式屬性
description: VML V-文字間距模式屬性
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463672"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="8f0b3-103">VML V-文字間距模式屬性</span><span class="sxs-lookup"><span data-stu-id="8f0b3-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="8f0b3-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8f0b3-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8f0b3-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8f0b3-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8f0b3-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8f0b3-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8f0b3-110">定義字母間距的模式。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="8f0b3-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8f0b3-111">Read/write.</span></span> <span data-ttu-id="8f0b3-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-112">**String**.</span></span>

<span data-ttu-id="8f0b3-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-113">**Applies To**</span></span>

[<span data-ttu-id="8f0b3-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="8f0b3-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="8f0b3-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-115">**Tag Syntax**</span></span>

<span data-ttu-id="8f0b3-116"><v： *element* style = "v-text-間距-mode： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8f0b3-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="8f0b3-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-117">**Script Syntax**</span></span>

<span data-ttu-id="8f0b3-118"> node.js-文字間距-模式 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8f0b3-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="8f0b3-119">*運算式* =*元素*. 樣式。 v-文字間距-模式</span><span class="sxs-lookup"><span data-stu-id="8f0b3-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="8f0b3-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-120">**Remarks**</span></span>

<span data-ttu-id="8f0b3-121">值包括</span><span class="sxs-lookup"><span data-stu-id="8f0b3-121">Values include</span></span>

-   <span data-ttu-id="8f0b3-122">**(預設**) </span><span class="sxs-lookup"><span data-stu-id="8f0b3-122">**tightening** (default)</span></span>
-   <span data-ttu-id="8f0b3-123">**跟蹤**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-123">**tracking**</span></span>

<span data-ttu-id="8f0b3-124">這個屬性會決定是否要在每個字母之間移除空間 (將) ，或在每個字母 (追蹤) 之間新增空間。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="8f0b3-125">字母間距變更的數量是由 [V 文字間距](msdn-online-vml-v-text-spacing-attribute.md) 屬性所定義。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="8f0b3-126">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="8f0b3-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="8f0b3-127">**範例**</span><span class="sxs-lookup"><span data-stu-id="8f0b3-127">**Example**</span></span>

<span data-ttu-id="8f0b3-128">每個字母的字母間距會增加200單位。</span><span class="sxs-lookup"><span data-stu-id="8f0b3-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 