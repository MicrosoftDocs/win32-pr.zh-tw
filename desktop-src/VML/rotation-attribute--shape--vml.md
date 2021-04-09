---
title: '旋轉屬性 (圖形)  (VML) '
description: '旋轉屬性 (圖形)  (VML) '
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024042"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="b851d-103">旋轉屬性 (圖形)  (VML) </span><span class="sxs-lookup"><span data-stu-id="b851d-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="b851d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b851d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b851d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b851d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b851d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b851d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b851d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b851d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b851d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b851d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b851d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b851d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b851d-110">定義形狀旋轉的角度。</span><span class="sxs-lookup"><span data-stu-id="b851d-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="b851d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b851d-111">Read/write.</span></span> <span data-ttu-id="b851d-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md)。</span><span class="sxs-lookup"><span data-stu-id="b851d-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="b851d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b851d-113">**Applies To**</span></span>

[<span data-ttu-id="b851d-114">形狀</span><span class="sxs-lookup"><span data-stu-id="b851d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b851d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b851d-115">**Tag Syntax**</span></span>

<span data-ttu-id="b851d-116"><v： *element* style = "旋轉： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b851d-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="b851d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b851d-117">**Script Syntax**</span></span>

<span data-ttu-id="b851d-118">*元素* 。旋轉 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b851d-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="b851d-119">*運算式* =*元素*。旋轉</span><span class="sxs-lookup"><span data-stu-id="b851d-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="b851d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b851d-120">**Remarks**</span></span>

<span data-ttu-id="b851d-121">以度為單位的值可以是正數或負數，而大於360的值則會被模組化至360度的圓形。</span><span class="sxs-lookup"><span data-stu-id="b851d-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="b851d-122">正面角度是順時針的。</span><span class="sxs-lookup"><span data-stu-id="b851d-122">Positive angles are clockwise.</span></span> <span data-ttu-id="b851d-123">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="b851d-123">The default value is 0.</span></span>

<span data-ttu-id="b851d-124">請注意，圖形會在旋轉之後重新置放，以反映新的周框方塊座標。</span><span class="sxs-lookup"><span data-stu-id="b851d-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="b851d-125">也請注意，在撰寫腳本時，不會使用 **樣式** 屬性，而會將 **旋轉** 視為圖形的直接屬性。</span><span class="sxs-lookup"><span data-stu-id="b851d-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="b851d-126">**旋轉** 屬性類似于樣式的標準 HTML **旋轉** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b851d-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="b851d-127">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b851d-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="b851d-128">**另請參閱**</span><span class="sxs-lookup"><span data-stu-id="b851d-128">**See Also**</span></span>

<span data-ttu-id="b851d-129">**範例**</span><span class="sxs-lookup"><span data-stu-id="b851d-129">**Example**</span></span>

<span data-ttu-id="b851d-130">矩形將會傾斜45度。</span><span class="sxs-lookup"><span data-stu-id="b851d-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="b851d-131">[旋轉屬性範例](/previous-versions/bb264091(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b851d-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="b851d-132"> (需要 Microsoft Internet Explorer 5 或更高版本。 ) </span><span class="sxs-lookup"><span data-stu-id="b851d-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 