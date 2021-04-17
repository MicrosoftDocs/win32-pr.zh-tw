---
title: VML EndAngle 屬性
description: VML EndAngle 屬性
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316360"
---
# <a name="vml-endangle-attribute"></a><span data-ttu-id="68a09-103">VML EndAngle 屬性</span><span class="sxs-lookup"><span data-stu-id="68a09-103">VML EndAngle Attribute</span></span>

<span data-ttu-id="68a09-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="68a09-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="68a09-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="68a09-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="68a09-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="68a09-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="68a09-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="68a09-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="68a09-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="68a09-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="68a09-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="68a09-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="68a09-110">定義弧線的端點。讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="68a09-110">Defines the endpoint of the arc. Read/write.</span></span> <span data-ttu-id="68a09-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="68a09-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="68a09-112">**適用於**</span><span class="sxs-lookup"><span data-stu-id="68a09-112">**Applies To**</span></span>

[<span data-ttu-id="68a09-113">Arc</span><span class="sxs-lookup"><span data-stu-id="68a09-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="68a09-114">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="68a09-114">**Tag Syntax**</span></span>

<span data-ttu-id="68a09-115"><v： *element* endangle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="68a09-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="68a09-116">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="68a09-116">**Script Syntax**</span></span>

<span data-ttu-id="68a09-117"> endAngle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="68a09-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="68a09-118">*運算式* =\*\* endAngle</span><span class="sxs-lookup"><span data-stu-id="68a09-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="68a09-119">**備註**</span><span class="sxs-lookup"><span data-stu-id="68a09-119">**Remarks**</span></span>

<span data-ttu-id="68a09-120">弧線定義為沿著圖形的 **樣式** 屬性所系結的橢圓所繪製的筆劃。</span><span class="sxs-lookup"><span data-stu-id="68a09-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="68a09-121">筆劃末端的定義是以水準向上 (12 點鐘) 順時針測量的角度來定義。</span><span class="sxs-lookup"><span data-stu-id="68a09-121">The end of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="68a09-122">預設值為90度。</span><span class="sxs-lookup"><span data-stu-id="68a09-122">The default value is 90 degrees.</span></span>

<span data-ttu-id="68a09-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="68a09-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="68a09-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="68a09-124">**Example**</span></span>

<span data-ttu-id="68a09-125">弧線是微笑的。</span><span class="sxs-lookup"><span data-stu-id="68a09-125">The arc is smiling.</span></span> <span data-ttu-id="68a09-126">起點是在圖形周框方塊內的橢圓的90度點。</span><span class="sxs-lookup"><span data-stu-id="68a09-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="68a09-127">端點位於橢圓的270度點。</span><span class="sxs-lookup"><span data-stu-id="68a09-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 