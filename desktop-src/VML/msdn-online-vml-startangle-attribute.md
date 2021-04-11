---
title: VML >startangle 屬性
description: VML >startangle 屬性
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023721"
---
# <a name="vml-startangle-attribute"></a><span data-ttu-id="4f41b-103">VML >startangle 屬性</span><span class="sxs-lookup"><span data-stu-id="4f41b-103">VML StartAngle Attribute</span></span>

<span data-ttu-id="4f41b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="4f41b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4f41b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="4f41b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4f41b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="4f41b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4f41b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="4f41b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4f41b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="4f41b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4f41b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="4f41b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4f41b-110">定義弧線的起點。讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="4f41b-110">Defines the starting point of the arc. Read/write.</span></span> <span data-ttu-id="4f41b-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="4f41b-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="4f41b-112">**適用於**</span><span class="sxs-lookup"><span data-stu-id="4f41b-112">**Applies To**</span></span>

[<span data-ttu-id="4f41b-113">Arc</span><span class="sxs-lookup"><span data-stu-id="4f41b-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="4f41b-114">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="4f41b-114">**Tag Syntax**</span></span>

<span data-ttu-id="4f41b-115"><v： *element* endangle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="4f41b-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="4f41b-116">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="4f41b-116">**Script Syntax**</span></span>

<span data-ttu-id="4f41b-117"> endAngle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="4f41b-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="4f41b-118">*運算式* =\*\* endAngle</span><span class="sxs-lookup"><span data-stu-id="4f41b-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="4f41b-119">**備註**</span><span class="sxs-lookup"><span data-stu-id="4f41b-119">**Remarks**</span></span>

<span data-ttu-id="4f41b-120">弧線定義為沿著圖形的 **樣式** 屬性所系結的橢圓所繪製的筆劃。</span><span class="sxs-lookup"><span data-stu-id="4f41b-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="4f41b-121">筆劃的開頭是由從垂直向上 (12 點鐘) 順時針測量的角度來定義。</span><span class="sxs-lookup"><span data-stu-id="4f41b-121">The start of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="4f41b-122">預設值為0度。</span><span class="sxs-lookup"><span data-stu-id="4f41b-122">The default value is 0 degrees.</span></span>

<span data-ttu-id="4f41b-123">VML 標準屬性</span><span class="sxs-lookup"><span data-stu-id="4f41b-123">VML Standard Attribute</span></span>

<span data-ttu-id="4f41b-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="4f41b-124">**Example**</span></span>

<span data-ttu-id="4f41b-125">弧線是微笑的。</span><span class="sxs-lookup"><span data-stu-id="4f41b-125">The arc is smiling.</span></span> <span data-ttu-id="4f41b-126">起點是在圖形周框方塊內的橢圓的90度點。</span><span class="sxs-lookup"><span data-stu-id="4f41b-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="4f41b-127">端點位於橢圓的270度點。</span><span class="sxs-lookup"><span data-stu-id="4f41b-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 