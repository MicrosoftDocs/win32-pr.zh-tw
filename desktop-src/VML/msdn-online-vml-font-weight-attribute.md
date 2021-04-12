---
title: VML Font-Weight 屬性
description: VML Font-Weight 屬性
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e4de8a1bb4132c75d4520dcacc661fbbc97eef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375741"
---
# <a name="vml-font-weight-attribute"></a><span data-ttu-id="035b7-103">VML Font-Weight 屬性</span><span class="sxs-lookup"><span data-stu-id="035b7-103">VML Font-Weight Attribute</span></span>

<span data-ttu-id="035b7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="035b7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="035b7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="035b7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="035b7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="035b7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="035b7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="035b7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="035b7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="035b7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="035b7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="035b7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="035b7-110">定義字型之字母的粗細。</span><span class="sxs-lookup"><span data-stu-id="035b7-110">Defines the thickness of the letters of the font.</span></span> <span data-ttu-id="035b7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="035b7-111">Read/write.</span></span> <span data-ttu-id="035b7-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="035b7-112">**String**.</span></span>

<span data-ttu-id="035b7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="035b7-113">**Applies To**</span></span>

[<span data-ttu-id="035b7-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="035b7-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="035b7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="035b7-115">**Tag Syntax**</span></span>

<span data-ttu-id="035b7-116"><v： *element* style = "font-size： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="035b7-116"><v: *element* style="font-weight: *expression* "></span></span>

<span data-ttu-id="035b7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="035b7-117">**Script Syntax**</span></span>

<span data-ttu-id="035b7-118"> fontweight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="035b7-118">*element* .style.fontweight="*expression*"</span></span>

<span data-ttu-id="035b7-119">*運算式* =\*\* fontweight</span><span class="sxs-lookup"><span data-stu-id="035b7-119">*expression*=*element*.style.fontweight</span></span>

<span data-ttu-id="035b7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="035b7-120">**Remarks**</span></span>

<span data-ttu-id="035b7-121">這些值與標準 HTML 樣式屬性相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-121">The values are the same as the standard HTML style attributes.</span></span> <span data-ttu-id="035b7-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="035b7-122">Values include:</span></span>



| <span data-ttu-id="035b7-123">值</span><span class="sxs-lookup"><span data-stu-id="035b7-123">Value</span></span>   | <span data-ttu-id="035b7-124">描述</span><span class="sxs-lookup"><span data-stu-id="035b7-124">Description</span></span>                                                                 |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="035b7-125">正常</span><span class="sxs-lookup"><span data-stu-id="035b7-125">normal</span></span>  | <span data-ttu-id="035b7-126">一般。</span><span class="sxs-lookup"><span data-stu-id="035b7-126">Normal.</span></span> <span data-ttu-id="035b7-127">預設值。</span><span class="sxs-lookup"><span data-stu-id="035b7-127">Default.</span></span>                                                            |
| <span data-ttu-id="035b7-128">粗體</span><span class="sxs-lookup"><span data-stu-id="035b7-128">bold</span></span>    | <span data-ttu-id="035b7-129">大膽。</span><span class="sxs-lookup"><span data-stu-id="035b7-129">Bold.</span></span>                                                                       |
| <span data-ttu-id="035b7-130">bolder</span><span class="sxs-lookup"><span data-stu-id="035b7-130">bolder</span></span>  | <span data-ttu-id="035b7-131">比一般一般。</span><span class="sxs-lookup"><span data-stu-id="035b7-131">Heavier than normal.</span></span>                                                        |
| <span data-ttu-id="035b7-132">lighter</span><span class="sxs-lookup"><span data-stu-id="035b7-132">lighter</span></span> | <span data-ttu-id="035b7-133">比平常更淺。</span><span class="sxs-lookup"><span data-stu-id="035b7-133">Lighter than normal.</span></span>                                                        |
| <span data-ttu-id="035b7-134">100</span><span class="sxs-lookup"><span data-stu-id="035b7-134">100</span></span>     | <span data-ttu-id="035b7-135">至少以最亮的200權數。</span><span class="sxs-lookup"><span data-stu-id="035b7-135">At least as light as the 200 weight.</span></span>                                        |
| <span data-ttu-id="035b7-136">200</span><span class="sxs-lookup"><span data-stu-id="035b7-136">200</span></span>     | <span data-ttu-id="035b7-137">至少以粗體顯示100權數，以及至少與300權數相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-137">At least as bold as the 100 weight and at least as light as the 300 weight.</span></span> |
| <span data-ttu-id="035b7-138">300</span><span class="sxs-lookup"><span data-stu-id="035b7-138">300</span></span>     | <span data-ttu-id="035b7-139">至少以粗體顯示200權數，以及至少與400權數相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-139">At least as bold as the 200 weight and at least as light as the 400 weight.</span></span> |
| <span data-ttu-id="035b7-140">400</span><span class="sxs-lookup"><span data-stu-id="035b7-140">400</span></span>     | <span data-ttu-id="035b7-141">一般。</span><span class="sxs-lookup"><span data-stu-id="035b7-141">Normal.</span></span>                                                                     |
| <span data-ttu-id="035b7-142">500</span><span class="sxs-lookup"><span data-stu-id="035b7-142">500</span></span>     | <span data-ttu-id="035b7-143">至少以粗體顯示400權數，以及至少與600權數相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-143">At least as bold as the 400 weight and at least as light as the 600 weight.</span></span> |
| <span data-ttu-id="035b7-144">600</span><span class="sxs-lookup"><span data-stu-id="035b7-144">600</span></span>     | <span data-ttu-id="035b7-145">至少以粗體顯示500權數，以及至少與700權數相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-145">At least as bold as the 500 weight and at least as light as the 700 weight.</span></span> |
| <span data-ttu-id="035b7-146">700</span><span class="sxs-lookup"><span data-stu-id="035b7-146">700</span></span>     | <span data-ttu-id="035b7-147">大膽。</span><span class="sxs-lookup"><span data-stu-id="035b7-147">Bold.</span></span>                                                                       |
| <span data-ttu-id="035b7-148">800</span><span class="sxs-lookup"><span data-stu-id="035b7-148">800</span></span>     | <span data-ttu-id="035b7-149">至少以粗體顯示700權數，以及至少與900權數相同。</span><span class="sxs-lookup"><span data-stu-id="035b7-149">At least as bold as the 700 weight and at least as light as the 900 weight.</span></span> |
| <span data-ttu-id="035b7-150">900</span><span class="sxs-lookup"><span data-stu-id="035b7-150">900</span></span>     | <span data-ttu-id="035b7-151">至少以粗體顯示800權數。</span><span class="sxs-lookup"><span data-stu-id="035b7-151">At least as bold as the 800 weight.</span></span>                                         |



 

<span data-ttu-id="035b7-152">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="035b7-152">*VML Standard Attribute*</span></span>

<span data-ttu-id="035b7-153">**範例**</span><span class="sxs-lookup"><span data-stu-id="035b7-153">**Example**</span></span>

<span data-ttu-id="035b7-154">字型粗細為粗體。</span><span class="sxs-lookup"><span data-stu-id="035b7-154">The font weight is bold.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 