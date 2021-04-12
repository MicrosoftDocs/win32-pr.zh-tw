---
title: VML Font-Variant 屬性
description: VML Font-Variant 屬性
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375449"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="22201-103">VML Font-Variant 屬性</span><span class="sxs-lookup"><span data-stu-id="22201-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="22201-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="22201-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="22201-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="22201-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="22201-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="22201-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="22201-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="22201-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="22201-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="22201-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="22201-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="22201-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="22201-110">定義字型的 variant 樣式。</span><span class="sxs-lookup"><span data-stu-id="22201-110">Defines the variant style of a font.</span></span> <span data-ttu-id="22201-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="22201-111">Read/write.</span></span> <span data-ttu-id="22201-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="22201-112">**String**.</span></span>

<span data-ttu-id="22201-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="22201-113">**Applies To**</span></span>

[<span data-ttu-id="22201-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="22201-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="22201-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="22201-115">**Tag Syntax**</span></span>

<span data-ttu-id="22201-116"><v： *element* style = "字型-variant： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="22201-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="22201-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="22201-117">**Script Syntax**</span></span>

<span data-ttu-id="22201-118"> fontvariant = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="22201-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="22201-119">*運算式* =\*\* fontvariant</span><span class="sxs-lookup"><span data-stu-id="22201-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="22201-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="22201-120">**Remarks**</span></span>

<span data-ttu-id="22201-121">值如下：</span><span class="sxs-lookup"><span data-stu-id="22201-121">The values are:</span></span>

-   <span data-ttu-id="22201-122">一般 (預設) </span><span class="sxs-lookup"><span data-stu-id="22201-122">normal (default)</span></span>
-   <span data-ttu-id="22201-123">small 大寫字母</span><span class="sxs-lookup"><span data-stu-id="22201-123">small-caps</span></span>

<span data-ttu-id="22201-124">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="22201-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="22201-125">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="22201-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="22201-126">**範例**</span><span class="sxs-lookup"><span data-stu-id="22201-126">**Example**</span></span>

<span data-ttu-id="22201-127">字型會轉譯為小型大寫字母。</span><span class="sxs-lookup"><span data-stu-id="22201-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 