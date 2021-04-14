---
title: 'Position 屬性 (圖形)  (VML) '
description: 'Position 屬性 (圖形)  (VML) '
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382762"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="a88ef-103">Position 屬性 (圖形)  (VML) </span><span class="sxs-lookup"><span data-stu-id="a88ef-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="a88ef-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a88ef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a88ef-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a88ef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a88ef-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a88ef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a88ef-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a88ef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a88ef-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a88ef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a88ef-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a88ef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a88ef-110">定義用來放置元素的定位類型。</span><span class="sxs-lookup"><span data-stu-id="a88ef-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="a88ef-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a88ef-111">Read/write.</span></span> <span data-ttu-id="a88ef-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="a88ef-112">**String**.</span></span>

<span data-ttu-id="a88ef-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a88ef-113">**Applies To**</span></span>

[<span data-ttu-id="a88ef-114">形狀</span><span class="sxs-lookup"><span data-stu-id="a88ef-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a88ef-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a88ef-115">**Tag Syntax**</span></span>

<span data-ttu-id="a88ef-116"><v： *element* style = "position： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a88ef-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="a88ef-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="a88ef-117">**Script Syntax**</span></span>

<span data-ttu-id="a88ef-118">*element* . style. position = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a88ef-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="a88ef-119">*運算式* =*元素*。 style. position</span><span class="sxs-lookup"><span data-stu-id="a88ef-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="a88ef-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="a88ef-120">**Remarks**</span></span>

<span data-ttu-id="a88ef-121">**Position** 屬性類似于樣式表單所使用的標準 HTML **Position** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a88ef-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="a88ef-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="a88ef-122">Values include:</span></span>



| <span data-ttu-id="a88ef-123">值</span><span class="sxs-lookup"><span data-stu-id="a88ef-123">Value</span></span>    | <span data-ttu-id="a88ef-124">描述</span><span class="sxs-lookup"><span data-stu-id="a88ef-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88ef-125">static</span><span class="sxs-lookup"><span data-stu-id="a88ef-125">static</span></span>   | <span data-ttu-id="a88ef-126">預設值。</span><span class="sxs-lookup"><span data-stu-id="a88ef-126">Default.</span></span> <span data-ttu-id="a88ef-127">根據頁面的一般流程來定位元素。</span><span class="sxs-lookup"><span data-stu-id="a88ef-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="a88ef-128">**Top** 和 **Left** 屬性都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a88ef-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="a88ef-129">如果物件是錨定的，而這只會在 Microsoft Word 中發生，則會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a88ef-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="a88ef-130">絕對</span><span class="sxs-lookup"><span data-stu-id="a88ef-130">absolute</span></span> | <span data-ttu-id="a88ef-131">使用 **Top** 和 **Left** 屬性，以相對於父代的位置來定位元素。</span><span class="sxs-lookup"><span data-stu-id="a88ef-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="a88ef-132">Microsoft Word 和 Microsoft Excel 浮動物件和 Microsoft PowerPoint 投影片會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a88ef-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="a88ef-133">relative</span><span class="sxs-lookup"><span data-stu-id="a88ef-133">relative</span></span> | <span data-ttu-id="a88ef-134">根據頁面的一般流程來定位元素，但會使用 **Top** 和 **Left** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a88ef-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="a88ef-135">重迭的元素是由 **Z 索引** 屬性所控管。</span><span class="sxs-lookup"><span data-stu-id="a88ef-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="a88ef-136">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="a88ef-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="a88ef-137">**範例**</span><span class="sxs-lookup"><span data-stu-id="a88ef-137">**Example**</span></span>

<span data-ttu-id="a88ef-138">矩形的位置會使用 *相對* 樣式來顯示。</span><span class="sxs-lookup"><span data-stu-id="a88ef-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="a88ef-139">[Position 屬性範例](/previous-versions/bb264090(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="a88ef-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="a88ef-140"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="a88ef-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 