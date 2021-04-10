---
title: VML Height 屬性
description: VML Height 屬性
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092831"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="652d2-103">VML Height 屬性</span><span class="sxs-lookup"><span data-stu-id="652d2-103">VML Height Attribute</span></span>

<span data-ttu-id="652d2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="652d2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="652d2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="652d2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="652d2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="652d2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="652d2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="652d2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="652d2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="652d2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="652d2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="652d2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="652d2-110">指定圖形的高度。</span><span class="sxs-lookup"><span data-stu-id="652d2-110">Specifies the height of the shape.</span></span> <span data-ttu-id="652d2-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="652d2-111">Read/write.</span></span> <span data-ttu-id="652d2-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="652d2-112">**String**.</span></span>

<span data-ttu-id="652d2-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="652d2-113">**Applies To**</span></span>

[<span data-ttu-id="652d2-114">形狀</span><span class="sxs-lookup"><span data-stu-id="652d2-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="652d2-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="652d2-115">**Tag Syntax**</span></span>

<span data-ttu-id="652d2-116"><v： *element* style = "height： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="652d2-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="652d2-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="652d2-117">**Script Syntax**</span></span>

<span data-ttu-id="652d2-118">style *. height* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="652d2-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="652d2-119">*運算式* =style *. height*</span><span class="sxs-lookup"><span data-stu-id="652d2-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="652d2-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="652d2-120">**Remarks**</span></span>

<span data-ttu-id="652d2-121">**Height** 屬性類似于樣式的標準 HTML **Height** 屬性。</span><span class="sxs-lookup"><span data-stu-id="652d2-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="652d2-122">單位可以對應至父元素，或可能是絕對單位。</span><span class="sxs-lookup"><span data-stu-id="652d2-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="652d2-123">數值包括：</span><span class="sxs-lookup"><span data-stu-id="652d2-123">Values include:</span></span>



| <span data-ttu-id="652d2-124">值</span><span class="sxs-lookup"><span data-stu-id="652d2-124">Value</span></span>      | <span data-ttu-id="652d2-125">描述</span><span class="sxs-lookup"><span data-stu-id="652d2-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="652d2-126">自動</span><span class="sxs-lookup"><span data-stu-id="652d2-126">Auto</span></span>       | <span data-ttu-id="652d2-127">頁面流程中專案的預設位置。</span><span class="sxs-lookup"><span data-stu-id="652d2-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="652d2-128">units</span><span class="sxs-lookup"><span data-stu-id="652d2-128">units</span></span>      | <span data-ttu-id="652d2-129">具有絕對單位指示項的數位 (cm、mm、in、pt、pc 或 px) 或相對單位指示項 (em 或 ex) 。</span><span class="sxs-lookup"><span data-stu-id="652d2-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="652d2-130">如果未指定任何單位，則會假設為圖元 (px) 。</span><span class="sxs-lookup"><span data-stu-id="652d2-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="652d2-131">percentage</span><span class="sxs-lookup"><span data-stu-id="652d2-131">percentage</span></span> | <span data-ttu-id="652d2-132">以父物件高度的百分比表示的值。</span><span class="sxs-lookup"><span data-stu-id="652d2-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="652d2-133">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="652d2-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="652d2-134">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="652d2-134">**See Also**</span></span>

[<span data-ttu-id="652d2-135">單位</span><span class="sxs-lookup"><span data-stu-id="652d2-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="652d2-136">**範例**</span><span class="sxs-lookup"><span data-stu-id="652d2-136">**Example**</span></span>

<span data-ttu-id="652d2-137">圖形的高度設定為30。</span><span class="sxs-lookup"><span data-stu-id="652d2-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="652d2-138">[Height 屬性範例](/previous-versions/bb229671(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="652d2-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="652d2-139"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="652d2-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 