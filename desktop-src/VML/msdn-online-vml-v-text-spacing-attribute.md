---
title: VML V 文字間距屬性
description: VML V 文字間距屬性
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376016"
---
# <a name="vml-v-text-spacing-attribute"></a><span data-ttu-id="3ab75-103">VML V 文字間距屬性</span><span class="sxs-lookup"><span data-stu-id="3ab75-103">VML V-Text-Spacing Attribute</span></span>

<span data-ttu-id="3ab75-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="3ab75-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ab75-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="3ab75-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ab75-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="3ab75-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ab75-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="3ab75-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ab75-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="3ab75-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ab75-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="3ab75-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ab75-110">定義文字的間距量。</span><span class="sxs-lookup"><span data-stu-id="3ab75-110">Defines the amount of spacing for text.</span></span> <span data-ttu-id="3ab75-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3ab75-111">Read/write.</span></span> <span data-ttu-id="3ab75-112">**VgNumber**。</span><span class="sxs-lookup"><span data-stu-id="3ab75-112">**VgNumber**.</span></span>

<span data-ttu-id="3ab75-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="3ab75-113">**Applies To**</span></span>

[<span data-ttu-id="3ab75-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="3ab75-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="3ab75-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="3ab75-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ab75-116"><v： *element* style = "v-text-間距： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3ab75-116"><v: *element* style="v-text-spacing: *expression* "></span></span>

<span data-ttu-id="3ab75-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="3ab75-117">**Script Syntax**</span></span>

<span data-ttu-id="3ab75-118">*元素* . style。 v-text-間距 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3ab75-118">*element* .style.v-text-spacing="*expression*"</span></span>

<span data-ttu-id="3ab75-119">*運算式* =*元素*. style. v-文字間距</span><span class="sxs-lookup"><span data-stu-id="3ab75-119">*expression*=*element*.style.v-text-spacing</span></span>

<span data-ttu-id="3ab75-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="3ab75-120">**Remarks**</span></span>

<span data-ttu-id="3ab75-121">預設值是 100。</span><span class="sxs-lookup"><span data-stu-id="3ab75-121">The default value is 100.</span></span> <span data-ttu-id="3ab75-122">如需文字間距的詳細資訊，請參閱 [V 文字間距模式](msdn-online-vml-v-text-spacing-mode-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="3ab75-122">See the [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) attribute for more information about text spacing.</span></span>

<span data-ttu-id="3ab75-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="3ab75-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3ab75-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="3ab75-124">**Example**</span></span>

<span data-ttu-id="3ab75-125">每個字母的字母間距會由200單位加強。</span><span class="sxs-lookup"><span data-stu-id="3ab75-125">The letterspacing between each letter is tightened by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 